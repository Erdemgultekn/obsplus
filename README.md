# 🎓 OBS+ (v2.5 Pro) | Akıllı Ders Kayıt & Otomatik Program Motoru

**Canlı Demo (Live App):** [https://erdemgultekn.github.io/obsplus/](https://erdemgultekn.github.io/obsplus/)

Bu proje, üniversite ders kayıt (Course Registration) dönemlerinde öğrencilerin en sık karşılaştığı **şube çakışması, ani kota doluluğu, önkoşul zinciri takibi ve öğrenci statüsü (AKTS/Sınamalı) kısıtlarını** tek ekranda otonom olarak çözmek amacıyla geliştirilmiştir.

## 🚀 Çözdüğümüz 5 Temel Ders Kayıt Problemi

1. **⚡ Otomatik Program Kuran Filtre (Backtracking Auto-Scheduler):**
   * Öğrencinin seçtiği **Boş Gün (Day-Off)** ve **Saat Filtresi (Örn: Sabah 08:40 dersi olmasın)** tercihlerine göre tüm şube kombinasyonlarını tarar ve **0 çakışma** ile optimum haftalık programı saniyesinde kurar.
2. **📌 Şube Sabitleme (Pin / Lock):**
   * Öğrenci belirli bir şubeyi/akademisyeni sabitlediğinde (`📌 Sabitle`), algoritma o şubeyi koruyarak diğer dersleri etrafına yerleştirir.
3. **🔔 Akıllı Kota Bekleme Listesi (Auto-Swap Waitlist & B Planı):**
   * Kayıt anında kotası dolan (`30/30 DOLU`) şubeler için öğrenciyi bekleme listesine alır ve açıkta kalmaması için alternatif açık şubeyi **"B Planı"** olarak programa ekler. Kontenjan açıldığı anda otomatik geçiş (`Auto-Swap`) yapar.
4. **🛡️ Resmi ÖİM Kural Motoru & Önkoşul (Prerequisite) Denetçisi:**
   * **Normal (40 AKTS)**, **Sınamalı / Probation (GANO < 1.80, Max 32 AKTS & Üst sınıf ders kilidi)** ve **Çift Anadal / ÇAP (42 AKTS)** kurallarını canlı denetler.
   * Alttan kalan zorunlu tekrar (`FF`) dersleri seçilmeden kaydın kesinleştirilmesini engeller ve her dersin açtığı sonraki önkoşul dersini (`🕸️ Açtığı sonraki ders`) gösterir.
5. **📱 Tam Mobil Uyum (Mobile-First Daily Cards & Sticky Bar):**
   * Mobil cihazlar için özel **Günlük Kart Görünümü** ve masaüstü için **Haftalık Tablo Grid** modları arasında anlık geçiş sunar.

## 🛠️ Kullanılan Teknolojiler & Metodoloji
* **Kural & Veri Entegrasyonu:** Yaşar Üniversitesi Öğrenci İşleri Müdürlüğü (ÖİM) Ders Kayıt Yönergeleri ve Bologna Müfredat Önkoşul Matrisi (Chrome MCP yapısı referans alınarak modellenmiştir).
* **Algoritma:** Kısıt Tatmini (Constraint Satisfaction) ve Geri İzlemeli Arama (Backtracking Search).
* **Arayüz:** HTML5, Vanilla JavaScript (ES6+), Tailwind CSS (Zero-dependency, kurulumsuz mimari).
