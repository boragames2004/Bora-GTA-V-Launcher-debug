# Bora GTA V Launcher

Bu proje, Android'de bir `.exe` dosyasını seçip cihazda kurulu EXE açabilen uygulamaya
(GameHub/Winlator gibi) gönderen basit bir launcher kabuğudur.

## Önemli
- GTA V dosyalarını içermez.
- Wine/Box64/DXVK içermez.
- OBB'yi otomatik açmaz veya çıkartmaz.
- Native Android port üretmez.
- Yalnızca kendi yasal oyun dosyalarınla kullanılmalıdır.

## APK oluşturma
1. Projeyi Android Studio veya AndroidIDE ile aç.
2. Gradle senkronizasyonunu bekle.
3. Build > Build APK(s) seç.
4. Çıktı: `app/build/outputs/apk/debug/app-debug.apk`

## Kullanım
1. Launcher'ı yükle.
2. `PlayGTAV.exe` dosyasını seç.
3. İstersen OBB dosyasını da seçip kaydet.
4. `OYUNU BAŞLAT` butonuna dokun.
5. Açılan uygulama listesinden GameHub/Winlator seç.

GameHub/Winlator, `.exe` için Android `ACTION_VIEW` kaydı yapmıyorsa otomatik açılmaz.
Bu durumda ilgili uygulamanın özel deep-link veya paket entegrasyonu gerekir.

## GitHub üzerinden otomatik APK oluşturma
1. GitHub'da yeni, boş bir repository oluştur.
2. Bu projenin içindeki dosyaların tamamını repository'nin ana dizinine yükle.
3. Repository içinde **Actions** sekmesine gir.
4. Soldan **Build Android APK** workflow'unu aç.
5. **Run workflow** düğmesine bas.
6. Derleme tamamlanınca workflow sayfasının altındaki **Artifacts** bölümünden
   `Bora-GTA-V-Launcher-APK` dosyasını indir.
7. İndirilen ZIP'in içindeki `Bora-GTA-V-Launcher-debug.apk` kurulabilir debug APK'dir.

Workflow ayrıca `main` veya `master` dalına kod gönderildiğinde otomatik çalışır.
