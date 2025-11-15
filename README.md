# 🌍 GeoGame: Where Are We?
**GMT 458 – Web GIS - Assignment 2**

Bu proje, GMT 458 dersi kapsamında geliştirilmiş, OpenLayers, Chart.js ve GSAP kütüphanelerini kullanan etkileşimli bir coğrafi tahmin oyunudur.

[![Live Demo Button](https://img.shields.io/badge/Live_Demo-Play_Now!-brightgreen?style=for-the-badge&logo=github-pages)](https://gmt-458-web-gis.github.io/geogame-mustafabtw/)

---

### 🎮 Oyun Düzeni ve Arayüz (Layout)

Oyun, modern ve karanlık bir tema üzerine kurulmuştur. Kullanıcı arayüzü, oyuncuyu oyundan koparmayacak şekilde minimalist ve animasyonludur.

| Intro Ekranı | Ana Menü | Oyun Ekranı (İpucu ile) | Oyun Sonu (Skor) |
| :---: | :---: | :---: | :---: |
| *[Buraya Intro ekran görüntüsünü sürükle]* | *[Buraya Ana Menü ekran görüntüsünü sürükle]* | *[Buraya Oyun ekran görüntüsünü sürükle]* | *[Buraya Skor ekran görüntüsünü sürükle]* |

---

### 🎯 Proje Gereksinimleri ve Mekanikleri

Bu bölüm, ödev kapsamında istenen gereksinimleri ve oyunun ilerleyişini detaylandırmaktadır.

#### 1. Oyunun İlerleyişi (Game Progression)
Oyun, zamana ve cana dayalı bir meydan okumadır.
* **Süre:** Kullanıcı oyuna **2 dakika (120 saniye)** ile başlar.
* **Bonus Süre:** Her doğru tahmin, oyuncuya **+10 saniye** kazandırır.
* **Zorluk:** Sorular (`gameData` dizisinden) her oyun başında karıştırılır, bu sayede her oyun farklı bir deneyim sunar.
* **Puanlama:** Her doğru cevap +100 Puan ve +5 Jeton verir.

#### 2. Soru Sayısı
* Oyunun veri tabanında (oyun.js > `gameData`) toplam **25 adet** benzersiz başkent bulunmaktadır.

#### 3. Can Sayısı (Lives)
* Kullanıcı oyuna **3 can** (💛💛💛) ile başlar.
* Her yanlış tahminde 1 can kaybedilir.
* Canlar bittiğinde veya süre dolduğunda oyun sona erer.

#### 4. İpucu Sistemi (Hints)
* Oyuncular, doğru tahminlerden kazandıkları jetonları ipuçları için harcayabilirler.
* **Yemek İpucu (10 Jeton):** O şehre ait meşhur bir yemeğin görselini gösterir.
* **Bayrak Rengi İpucu (10 Jeton):** O ülkenin bayrağında bulunan ana renkleri gösterir.

---

### 🛠️ Kullanılan Teknolojiler ve Kütüphaneler

Bu proje, modern web teknolojileri kullanılarak oluşturulmuştur ve ödevde belirtilen gelişmiş kütüphaneleri (bonus) içermektedir.

![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

* **OpenLayers:**
    * Tüm harita altyapısı, katman yönetimi (Dark, Light, Satellite) ve görüntülenmesi için kullanılmıştır.
    * Doğru tahminden sonra uçağın bir sonraki hedefe uçuş animasyonu ve rotanın çizilmesi (Vector Layer, LineString) OpenLayers ile yapılmıştır.

* **Chart.js (Bonus Kütüphane):**
    * Oyun sonu özet ekranında (`summary-screen`) oyuncunun performansını görselleştirmek için kullanılmıştır.
    * Doğru tahmin sayısı ile yanlış deneme sayısını bir "Doughnut" (halka) grafikte gösterir.

* **GSAP (GreenSock Animation Platform):**
    * Oyunun "albenisini" artıran tüm akıcı arayüz animasyonları için kullanılmıştır.
    * Oyun introsu, ekran geçişleri (fade-in/out), pop-up pencereler ve uçuş animasyonunun zamanlaması GSAP tarafından yönetilmektedir.
