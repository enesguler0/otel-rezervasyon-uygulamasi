# Otel Rezervasyon Uygulamasını Kurma

Bu kılavuz, Otel Rezervasyon Uygulamasını yerel makinenize kurma sürecinde size rehberlik edecektir.

## Ön koşullar

Başlamadan önce, sisteminizde Node.js yüklü olduğundan emin olun.

## Depoyu Klonlama

Depoyu yerel makinenize klonlayarak başlayın:

```bash
git clone https://github.com/enesguler0/otel-rezervasyon-uygulamasi.git
cd mern-booking-app
```
## Backend Konfigürasyonu

1. **Ortam Dosyaları**: `backend` klasörüne gidin ve `.env` dosyası oluşturun. Bu dosyaya  aşağıdaki içeriği ekleyin:

    ```plaintext
    MONGODB_CONNECTION_STRING=

    JWT_SECRET_KEY=
    FRONTEND_URL=

    # Cloudinary Variables
    CLOUDINARY_CLOUD_NAME=
    CLOUDINARY_API_KEY=
    CLOUDINARY_API_SECRET=

    # Stripe
    STRIPE_API_KEY=
    ```

2. **MongoDB Kurulumu**:  
    - MongoDB Atlasta bir hesap oluşturun.
    -  Yeni bir küme oluşturun ve yeni bir veritabanı kurma  talimatlarını izleyin.
    - Kurulum tamamlandıktan sonra, MongoDB bağlantı dizgenizi elde edin ve .env dosyalarınızdaki MONGODB_CONNECTION_STRING değişkenine ekleyin.

3. **Cloudinary Kurulumu**:
    - [Cloudinary](https://cloudinary.com/) adresinde bir hesap oluşturun.
    - Kontrol panelinize giderek bulut adınızı, API anahtarınızı bulun.
    - Bu bilgileri `.env` dosyalarınızdaki ilgili `CLOUDINARY_*` değişkenlerine ekleyin.

4. **Stripe Kurulumu**:
    - [Stripe](https://stripe.com/) adresinde bir Stripe hesabı oluşturun..
    - Stripe kontrol panelinde API anahtarlarınızı bulun.
    - Stripe API anahtarınızı `.env` dosyalarındaki `STRIPE_API_KEY` değişkenine ekleyin.
  
5. **JWT_SECRET_KEY**:
    - Bu, uzun, rastgele bir dize olmalıdır.

7. **Frontend URL**:
    - `FRONTEND_URL` frontend uygulamanızın çalıştığı URL'yi işaret etmelidir (yerel olarak çalıştırıyorsanız genellikle http://localhost:3000).
  

## Frontend Konfigürasyonu

1. **Ortam Dosyaları**: `frontend` klasörüne gidin ve bir dosya oluşturun: `.env`:

    ```plaintext
    VITE_API_BASE_URL=
    VITE_STRIPE_PUB_KEY=
    ```

5. **VITE_API_BASE_URL**:
    - `VITE_API_BASE_URL` backend uygulamanızın çalıştığı URL yi işaret etmelidir (yerel olarak çalıştırıyorsanız genellikle http://localhost:7000).

## Uygulamayı Çalıştırma

1. **Backend**:
    - `backend` klasörüne git.
    - Bağımlılıkları yükle: `npm install`.
    - Serverı başlat: `nodemon`.

2. **Frontend**:
    - Yeni bir terminal aç ve `frontend` klasörüne git.
    - Bağımlılıkları yükle: `npm install`.
    - Frontend uygulamasını başlat: `npm run dev`.
    - Uygulama şimdi http://localhost:5174 üzerinde çalışıyor olmalı ancak bunu komut satırı terminalinizde doğrulayın. 


