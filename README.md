# 🚀 CPM Analyzer & Network Grapher

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Vis.js](https://img.shields.io/badge/Vis.js-Network_Graph-blue?style=for-the-badge)
![Industrial Engineering](https://img.shields.io/badge/Industrial_Engineering-Operations_Research-10b981?style=for-the-badge)

**CPM Analyzer**, proje yönetimi ve yöneylem araştırması (Operations Research) prensiplerine dayalı olarak geliştirilmiş interaktif bir Karar Destek Sistemidir (Decision Support System). Kullanıcı tarafından girilen aktivitelerin sürelerini ve bağımlılıklarını analiz ederek projenin **Kritik Yolunu (Critical Path)** hesaplar ve sonuçları Çizge Teorisi (Graph Theory) kurallarına göre ekrana çizer.

🔗 **[Canlı Simülasyonu İncele (Live Demo)](https://onurfgg.github.io/BU_KİSMA_REPO_ADINI_YAZ)**

## 📊 Matematiksel Altyapı ve Metodoloji

Bu araç, arka planda karmaşık ağ topolojilerini çözmek için özel bir JavaScript algoritması kullanır. Sistem şu aşamaları takip eder:

1. **İleri Geçiş (Forward Pass):** Her aktivitenin En Erken Başlama (ES) ve En Erken Bitiş (EF) sürelerini hesaplar.
2. **Geri Geçiş (Backward Pass):** Ağın sonundan başına doğru ilerleyerek En Geç Başlama (LS) ve En Geç Bitiş (LF) sürelerini bulur.
3. **Bolluk (Slack) Hesabı:** Aktivitelerin gecikme toleranslarını belirler. Slack değeri 0 olan düğümler **Kritik Yol** üzerinde kabul edilir.
4. **Döngü Koruması (Cyclic Graph Protection):** Algoritma, kullanıcının yanlışlıkla kısırdöngü yaratan öncüller (A -> B ve B -> A) girmesini engeller.

## 🌟 Öne Çıkan Özellikler (Features)

* **Dinamik Veri Girişi:** İstenilen sayıda aktivite (Node) eklenebilir, süre ve öncül (Predecessor) bağımlılıkları tanımlanabilir.
* **Özel SVG Düğüm Motoru:** Sektör standardı olan Vis.js kütüphanesi kullanılarak her bir düğüm için özel vektörel (SVG) kutular oluşturulur. Bu kutular tıpkı akademik kitaplardaki gibi aktivitenin 4 köşesinde ES, EF, LS ve LF değerlerini barındırır.
* **Görsel Kritik Yol Haritası:** Projenin darboğazını oluşturan kritik yol, ağ üzerinde kırmızı oklarla (Edge) ve kırmızı düğümlerle otomatik olarak vurgulanır.
* **Auto-Fit ve Pan-Zoom:** Büyük projelerde ağ haritası otomatik olarak ekrana sığdırılır (Auto-fit) ve kullanıcı farenin tekerleği ile harita üzerinde gezinebilir.
* **Detaylı Analiz Tablosu:** Tüm veriler okunabilir bir matris tablosuna dökülür.

## ⚙️ Kurulum ve Kullanım (How to Use)

Proje %100 "Client-Side" (İstemci Taraflı) çalışmaktadır. Herhangi bir sunucu kurulumuna gerek yoktur.

1. Repoyu bilgisayarınıza klonlayın:
   ```bash
   git clone [https://github.com/onurfgg/BU_KISMA_REPO_ADINI_YAZ.git](https://github.com/onurfgg/BU_KISMA_REPO_ADINI_YAZ.git)
