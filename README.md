# Mealie - Tarif Yonetim Sistemi

Mealie, kendi sunucunuzda barindirabilceginiz acik kaynakli bir tarif yonetim uygulamasidir.

[![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/emreenesyavuz/mealie)

---

## Kurulum

### Render ile Deploy

1. Yukaridaki **Deploy to Render** butonuna tiklayin
2. Render hesabiniza giris yapin
3. Blueprint'i onaylayin ve deploy edin
4. PostgreSQL veritabani ve Mealie servisi otomatik olusturulacak
5. `BASE_URL` degerini Render'in verdigi URL ile guncelleyin

### Docker Compose ile Yerel Kurulum

```bash
# Repoyu klonlayin
git clone https://github.com/emreenesyavuz/mealie.git
cd mealie

# Ortam degiskenlerini yapilandirin
cp .env.example .env
# .env dosyasini duzenleyin

# Servisleri baslatin
docker compose up -d
```

Tarayicinizdan `http://localhost:9925` adresine gidin.

### Varsayilan Giris Bilgileri

| Alan     | Deger              |
|----------|--------------------|
| Email    | changeme@email.com |
| Sifre    | MyPassword         |

> **Onemli:** Ilk giristen sonra sifreyi degistirin!

---

## Yapilandirma

Tum yapilandirma `.env` dosyasindan yapilir. Ornek icin `.env.example` dosyasina bakin.

| Degisken           | Aciklama                     | Varsayilan         |
|--------------------|------------------------------|--------------------|
| `BASE_URL`         | Uygulamanin URL'i            | http://localhost:9925 |
| `POSTGRES_PASSWORD`| PostgreSQL sifresi           | mealie             |
| `ALLOW_SIGNUP`     | Yeni kayit izni              | true               |
| `TZ`               | Saat dilimi                  | Europe/Istanbul    |
| `OPENAI_API_KEY`   | OpenAI API anahtari (opsiyonel) | -               |

---

## English

Mealie is a self-hosted recipe management application.

### Quick Start

1. Click the **Deploy to Render** button above
2. Or use Docker Compose locally:
   ```bash
   cp .env.example .env
   docker compose up -d
   ```
3. Open `http://localhost:9925`
4. Default login: `changeme@email.com` / `MyPassword`

### Links

- [Mealie Docs](https://docs.mealie.io)
- [Mealie GitHub](https://github.com/mealie-recipes/mealie)
