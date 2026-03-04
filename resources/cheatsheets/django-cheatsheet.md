# 🐍 Django Cheatsheet — Django for Everyone

> Referensi cepat perintah dan pola Django yang paling sering dipakai.
> Bookmark halaman ini!

---

## ⚡ Perintah manage.py Paling Penting

```bash
# ── Project & App ──────────────────────────────────
django-admin startproject nama_project     # Buat project baru
python manage.py startapp nama_app         # Buat app baru

# ── Server ─────────────────────────────────────────
python manage.py runserver                 # Jalankan dev server (port 8000)
python manage.py runserver 8080            # Port custom

# ── Database ───────────────────────────────────────
python manage.py makemigrations            # Buat file migrasi
python manage.py migrate                   # Jalankan migrasi
python manage.py showmigrations            # Lihat status migrasi
python manage.py sqlmigrate app 0001       # Lihat SQL dari migrasi

# ── Shell ──────────────────────────────────────────
python manage.py shell                     # Python shell dengan context Django
python manage.py dbshell                   # Shell database langsung

# ── User ───────────────────────────────────────────
python manage.py createsuperuser           # Buat superuser admin

# ── Static Files ───────────────────────────────────
python manage.py collectstatic             # Kumpulkan static files

# ── Testing ────────────────────────────────────────
python manage.py test                      # Jalankan semua test
python manage.py test nama_app             # Test satu app saja
python manage.py test --verbosity=2        # Output detail

# ── Produksi ───────────────────────────────────────
python manage.py check --deploy            # Cek konfigurasi produksi
```

---

## 🗄️ ORM — QuerySet Cheatsheet

```python
from myapp.models import Artikel, Penulis

# ── Mengambil Data ─────────────────────────────────
Artikel.objects.all()                      # Semua artikel
Artikel.objects.get(id=1)                  # Satu artikel (error jika tidak ada)
Artikel.objects.filter(status='publish')   # Filter
Artikel.objects.exclude(status='draft')   # Kecualikan
Artikel.objects.first()                    # Artikel pertama
Artikel.objects.last()                     # Artikel terakhir
Artikel.objects.count()                    # Hitung jumlah

# ── Filter Lanjutan ────────────────────────────────
Artikel.objects.filter(judul__contains='Django')       # LIKE %Django%
Artikel.objects.filter(judul__icontains='django')      # Case-insensitive
Artikel.objects.filter(judul__startswith='Belajar')    # Dimulai dengan
Artikel.objects.filter(tanggal__year=2025)             # Filter tahun
Artikel.objects.filter(views__gte=100)                 # >= 100
Artikel.objects.filter(views__lte=50)                  # <= 50
Artikel.objects.filter(views__in=[10, 20, 30])         # IN

# ── Q Object (OR / AND kompleks) ───────────────────
from django.db.models import Q
Artikel.objects.filter(Q(status='publish') | Q(featured=True))
Artikel.objects.filter(Q(penulis=user) & Q(status='draft'))

# ── Sorting ────────────────────────────────────────
Artikel.objects.order_by('judul')          # ASC
Artikel.objects.order_by('-tanggal')       # DESC
Artikel.objects.order_by('?')             # Random

# ── Slicing ────────────────────────────────────────
Artikel.objects.all()[:10]               # 10 artikel pertama
Artikel.objects.all()[10:20]             # Artikel 11-20

# ── Create, Update, Delete ─────────────────────────
# CREATE
artikel = Artikel.objects.create(judul="Test", konten="Isi")
artikel = Artikel(judul="Test"); artikel.save()

# UPDATE
Artikel.objects.filter(id=1).update(status='publish')
artikel = Artikel.objects.get(id=1)
artikel.judul = "Judul Baru"; artikel.save()

# DELETE
Artikel.objects.get(id=1).delete()
Artikel.objects.filter(status='draft').delete()

# ── Optimasi ───────────────────────────────────────
# select_related: untuk ForeignKey (JOIN)
Artikel.objects.select_related('penulis').all()

# prefetch_related: untuk ManyToMany
Artikel.objects.prefetch_related('tags').all()

# values: hanya ambil field tertentu (lebih cepat)
Artikel.objects.values('id', 'judul')

# ── Aggregasi ──────────────────────────────────────
from django.db.models import Count, Sum, Avg, Max, Min
Artikel.objects.aggregate(total=Count('id'))
Artikel.objects.aggregate(rata_views=Avg('views'))
```

---

## 🗺️ URL Patterns

```python
# urls.py
from django.urls import path, include
from . import views

app_name = 'blog'  # Namespace — selalu tambahkan ini!

urlpatterns = [
    path('', views.beranda, name='beranda'),
    path('artikel/', views.daftar_artikel, name='daftar'),
    path('artikel/<int:pk>/', views.detail_artikel, name='detail'),
    path('artikel/<slug:slug>/', views.detail_by_slug, name='detail-slug'),
    path('artikel/<int:pk>/edit/', views.edit_artikel, name='edit'),
    path('api/', include('api.urls')),                    # Include URL lain
]

# Di template:
# {% url 'blog:detail' pk=artikel.pk %}
# {% url 'blog:daftar' %}

# Di Python:
# from django.urls import reverse
# reverse('blog:detail', kwargs={'pk': 1})
```

---

## 👁️ Views

```python
# ── Function-Based View ────────────────────────────
from django.shortcuts import render, get_object_or_404, redirect
from django.contrib.auth.decorators import login_required
from django.contrib import messages

def daftar_artikel(request):
    artikel = Artikel.objects.filter(status='publish').order_by('-tanggal')
    return render(request, 'blog/daftar.html', {'artikel': artikel})

@login_required
def buat_artikel(request):
    if request.method == 'POST':
        form = ArtikelForm(request.POST, request.FILES)
        if form.is_valid():
            artikel = form.save(commit=False)
            artikel.penulis = request.user
            artikel.save()
            messages.success(request, 'Artikel berhasil dibuat!')
            return redirect('blog:detail', pk=artikel.pk)
    else:
        form = ArtikelForm()
    return render(request, 'blog/form.html', {'form': form})

# ── Class-Based Views ──────────────────────────────
from django.views.generic import ListView, DetailView, CreateView
from django.contrib.auth.mixins import LoginRequiredMixin

class DaftarArtikelView(ListView):
    model = Artikel
    template_name = 'blog/daftar.html'
    context_object_name = 'artikel'
    paginate_by = 10

    def get_queryset(self):
        return Artikel.objects.filter(status='publish').order_by('-tanggal')

class BuatArtikelView(LoginRequiredMixin, CreateView):
    model = Artikel
    fields = ['judul', 'konten', 'kategori']
    template_name = 'blog/form.html'

    def form_valid(self, form):
        form.instance.penulis = self.request.user
        return super().form_valid(form)
```

---

## 📋 Models

```python
from django.db import models
from django.contrib.auth.models import User
from django.urls import reverse
from django.utils.text import slugify

class Kategori(models.Model):
    nama = models.CharField(max_length=100)
    slug = models.SlugField(unique=True)

    def __str__(self):
        return self.nama

    class Meta:
        verbose_name_plural = 'Kategori'
        ordering = ['nama']

class Artikel(models.Model):
    STATUS_CHOICES = [
        ('draft', 'Draft'),
        ('publish', 'Publish'),
    ]

    judul       = models.CharField(max_length=200, verbose_name='Judul')
    slug        = models.SlugField(unique=True, blank=True)
    konten      = models.TextField(verbose_name='Konten')
    gambar      = models.ImageField(upload_to='artikel/', blank=True, null=True)
    penulis     = models.ForeignKey(User, on_delete=models.CASCADE, related_name='artikel')
    kategori    = models.ForeignKey(Kategori, on_delete=models.SET_NULL, null=True)
    tags        = models.ManyToManyField('Tag', blank=True)
    status      = models.CharField(max_length=10, choices=STATUS_CHOICES, default='draft')
    dibuat_pada = models.DateTimeField(auto_now_add=True)
    diupdate    = models.DateTimeField(auto_now=True)
    views       = models.PositiveIntegerField(default=0)

    def save(self, *args, **kwargs):
        if not self.slug:
            self.slug = slugify(self.judul)
        super().save(*args, **kwargs)

    def get_absolute_url(self):
        return reverse('blog:detail', kwargs={'slug': self.slug})

    def __str__(self):
        return self.judul

    class Meta:
        ordering = ['-dibuat_pada']
        verbose_name_plural = 'Artikel'
```

---

## 🎨 Template — Tag & Filter Penting

```django
{# Komentar di template #}

{# Variable #}
{{ artikel.judul }}
{{ artikel.penulis.get_full_name }}

{# Filter #}
{{ judul|upper }}                    {# HURUF BESAR #}
{{ judul|lower }}                    {# huruf kecil #}
{{ judul|title }}                    {# Huruf Kapital Tiap Kata #}
{{ konten|truncatewords:30 }}        {# Potong 30 kata #}
{{ konten|truncatechars:200 }}       {# Potong 200 karakter #}
{{ konten|linebreaks }}              {# \n jadi <br> dan <p> #}
{{ konten|safe }}                    {# Render HTML (HATI-HATI XSS!) #}
{{ tanggal|date:"d M Y" }}          {# Format tanggal #}
{{ harga|floatformat:2 }}            {# 2 desimal #}
{{ list|length }}                    {# Panjang list #}
{{ nilai|default:"Tidak ada" }}      {# Default jika None/empty #}

{# Tag #}
{% if user.is_authenticated %}
    Halo, {{ user.username }}!
{% elif user.is_staff %}
    Halo Admin!
{% else %}
    Silakan login.
{% endif %}

{% for artikel in artikel_list %}
    {{ forloop.counter }}. {{ artikel.judul }}    {# 1, 2, 3... #}
    {{ forloop.counter0 }}                        {# 0, 1, 2... #}
    {{ forloop.first }}                           {# True jika pertama #}
    {{ forloop.last }}                            {# True jika terakhir #}
{% empty %}
    Tidak ada artikel.
{% endfor %}

{% url 'blog:detail' pk=artikel.pk %}
{% static 'css/style.css' %}
{% load static %}
{% block content %}{% endblock %}
{% include 'partials/navbar.html' %}
{% csrf_token %}
```

---

## ⚙️ Settings Penting

```python
# settings.py

# ── Keamanan ───────────────────────────────────────
from decouple import config

SECRET_KEY = config('SECRET_KEY')           # Dari .env
DEBUG = config('DEBUG', default=False, cast=bool)
ALLOWED_HOSTS = config('ALLOWED_HOSTS', default='').split(',')

# ── Database ───────────────────────────────────────
import dj_database_url
DATABASES = {
    'default': dj_database_url.config(
        default=config('DATABASE_URL', default='sqlite:///db.sqlite3')
    )
}

# ── Static & Media ─────────────────────────────────
STATIC_URL = '/static/'
STATICFILES_DIRS = [BASE_DIR / 'static']
STATIC_ROOT = BASE_DIR / 'staticfiles'

MEDIA_URL = '/media/'
MEDIA_ROOT = BASE_DIR / 'media'

# ── Auth ───────────────────────────────────────────
LOGIN_URL = '/login/'
LOGIN_REDIRECT_URL = '/'
LOGOUT_REDIRECT_URL = '/'
AUTH_USER_MODEL = 'accounts.User'          # Custom user model

# ── Email ──────────────────────────────────────────
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = config('EMAIL_HOST')
EMAIL_PORT = config('EMAIL_PORT', cast=int)
EMAIL_USE_TLS = True
EMAIL_HOST_USER = config('EMAIL_HOST_USER')
EMAIL_HOST_PASSWORD = config('EMAIL_HOST_PASSWORD')

# ── Cache (Redis) ──────────────────────────────────
CACHES = {
    "default": {
        "BACKEND": "django_redis.cache.RedisCache",
        "LOCATION": config('REDIS_URL', default='redis://127.0.0.1:6379/1'),
    }
}

# ── Celery ─────────────────────────────────────────
CELERY_BROKER_URL = config('REDIS_URL', default='redis://127.0.0.1:6379/0')
CELERY_RESULT_BACKEND = CELERY_BROKER_URL
```

---

## 🔐 Keamanan — Checklist

```python
# settings.py untuk PRODUCTION
SECURE_SSL_REDIRECT = True
SECURE_HSTS_SECONDS = 31536000
SECURE_HSTS_INCLUDE_SUBDOMAINS = True
SECURE_HSTS_PRELOAD = True
SESSION_COOKIE_SECURE = True
CSRF_COOKIE_SECURE = True
X_FRAME_OPTIONS = 'DENY'
SECURE_CONTENT_TYPE_NOSNIFF = True
```

---

_Cheatsheet ini bagian dari [Django for Everyone](../../README.md) oleh Ahmad Faqih_
