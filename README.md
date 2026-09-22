# agirkirala-gizlilik

AĞIRKİRALA'nın Google Play'e verilecek iki yasal sayfası: gizlilik politikası
ve hesap silme talimatı. Statik HTML — hiçbir bağımlılık yok, GitHub Pages ile
doğrudan yayınlanır.

## Yayına almadan önce

İki dosyada da `<!--DOLDUR-->` ile işaretli üç yer var, doldurulmadan
yayınlanmamalı:

- `index.html` — veri sorumlusu adı, adres, iletişim e-postası (iki yerde)
- `hesap-silme.html` — iletişim e-postası

Bu metinler hukuki taslaktır; yayından önce bir hukukçuya okutmanız önerilir.

## GitHub'a koyma ve Pages ile yayınlama

```bash
git init
git add .
git commit -m "Gizlilik politikası ve hesap silme sayfası"
git branch -M main
git remote add origin https://github.com/<kullanici-adiniz>/agirkirala-gizlilik.git
git push -u origin main
```

Sonra GitHub'da: **Settings → Pages → Branch: main / (root) → Save**.

Birkaç dakika içinde adresiniz hazır olur:

```
https://<kullanici-adiniz>.github.io/agirkirala-gizlilik/
https://<kullanici-adiniz>.github.io/agirkirala-gizlilik/hesap-silme.html
```

Bu iki adresi Play Console'a girin:
- **Gizlilik politikası** alanına ilk adres
- **Veri güvenliği → Hesap silme** alanına ikinci adres

## Kendi domaininizde yayınlamak isterseniz

`agirkirala.com` zaten sizde olduğu için isterseniz bu dosyaları
`agirkirala.com/gizlilik` ve `agirkirala.com/hesap-silme` altına da
koyabilirsiniz (Vercel projesine `public/gizlilik.html` gibi eklenir).
GitHub Pages daha hızlı başlangıç için burada.

## Güncelleme

Uygulama yeni bir veri türü toplamaya başlarsa (örn. konum izni eklenirse)
hem bu sayfalar hem Play Console'daki "Veri güvenliği" formu **birlikte**
güncellenmeli — ikisi arasında tutarsızlık Play incelemesinde reddedilir.
