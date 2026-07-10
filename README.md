# Yahya Doğan — Akademik CV Sitesi

İki dilli (TR/EN), yönetim panelli, statik akademik CV sitesi.
GitHub Pages üzerinde ücretsiz yayınlanmak üzere hazırlandı.

## Dosyalar

| Dosya | Açıklama |
|---|---|
| `index.html` | Ana CV sayfası. `data.json`'u okuyup sayfayı oluşturur. |
| `admin.html` | Parola korumalı yönetim paneli. İçeriği düzenler, güncel `data.json`'u indirir. |
| `data.json` | Tüm CV içeriği. Sitenin tek veri kaynağı. |
| `assets/profile.jpg` | Profil fotoğrafı. |

## Yayınlama (GitHub Pages)

Terminalde (Ubuntu / VS Code) sırasıyla:

```bash
# 1) Bu klasörü git deposu yap
cd AkademikWebSayfasi
git init
git add .
git commit -m "İlk sürüm: akademik CV sitesi"

# 2) GitHub'da 'yahyadogan72.github.io' adında BOŞ bir repo oluştur, sonra:
git branch -M main
git remote add origin https://github.com/yahyadogan72/yahyadogan72.github.io.git
git push -u origin main
```

Ardından GitHub'da repo → **Settings → Pages** → Source: `Deploy from a branch` →
Branch: `main` / `root` → **Save**.

Birkaç dakika içinde site şu adreste yayında olur:
**https://yahyadogan72.github.io**

## İçeriği güncelleme

1. `https://yahyadogan72.github.io/admin.html` adresine git.
2. Parolayı gir (varsayılan: `siirt2024` — `admin.html` içindeki `PASSWORD` satırından değiştir).
3. İlgili sekmede yayın/proje/tez ekle, düzenle, sil, sırala.
4. Üstteki **“data.json İndir”**e bas.
5. İnen `data.json`'u proje klasöründeki eskisiyle değiştir.
6. VS Code terminalinde:

```bash
git add .
git commit -m "CV güncelleme"
git push
```

Değişiklikler tarayıcında otomatik saklanır (sekmeyi kapatsan da kaybolmaz),
ama siteye yansıması için `data.json`'u indirip push etmen gerekir.

## Fotoğrafı değiştirme

Yeni fotoğrafı `assets/profile.jpg` olarak kaydet (aynı isimle), commit + push yap.
Farklı isim kullanırsan admin panelde **Profil → Fotoğraf yolu** alanını güncelle.

## Notlar

- Panel parolası statik sitede gerçek güvenlik sağlamaz; yalnızca gündelik gözlere karşıdır.
  Hassas bir şey yayınlamadığın için bu yeterlidir.
- Yayın başlıkları akademik standarda uygun olarak orijinal dillerinde bırakılmıştır;
  arayüz (menü, başlıklar) TR/EN olarak çevrilir.
- Google Scholar / ORCID bağlantılarını admin panelde **Profil** sekmesinden ekleyebilirsin;
  eklenince hero bölümünde otomatik görünür.
