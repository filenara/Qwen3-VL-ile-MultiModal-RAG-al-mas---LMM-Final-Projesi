# Qwen3-VL-ile-MultiModal-RAG-al-mas---LMM-Final-Projesi

Bu proje, **PDF dosyaları** üzerinde çalışan **çok modlu (text–table–image)** bir RAG (Retrieval Augmented Generation) sistemidir.

Kullanıcıdan gelen soruya göre sistem:
- Metin (text)
- Tablo (table)
- Görsel / şekil (image – sayfa bazlı)

kanallarından **hangisinin daha uygun olduğuna karar verir** ve cevabı o içerik üzerinden üretir.

Proje **tek bir `.ipynb` dosyası** üzerinden çalışır, ek arayüz yoktur.

---

## Proje Ne Yapıyor?

1. PDF dosyasını parçalara ayırır:
   - Metin parçaları
   - Tablo benzeri içerikler
   - Sayfa bazlı görsel temsiller

2. Her içerik türü için ayrı arama index’i oluşturur (FAISS).

3. Kullanıcının sorusuna göre:
   - Hangi kanalın (text / table / image) daha uygun olduğunu belirler
   - En ilgili içeriği bulur
   - Model ile cevabı üretir

4. Sistem performansını ölçer:
   - Doğru kanal seçildi mi?
   - Doğru sayfa üst sıralarda mı?

---

## Neden Böyle Bir Sistem?

Akademik makalelerde:
- Tablolar genelde metinle açıklanır
- Şekiller yapıyı gösterir
- Her soru için tek bir içerik türü yeterli olmaz

Bu proje, **“her soruya aynı yerden bakmak” yerine**,  
**soruya göre içerik seçmeyi** amaçlar.

---

## Nasıl Çalıştırılır?

### Google Colab’da Aç

- `.ipynb` dosyasını Google Colab’a yükle
- Notebook’u aç

---

### Hücreleri Sırayla Çalıştır

- Kütüphane kurulum hücrelerini çalıştır
- PDF yükleme hücresinde PDF dosyanı yükle
- Index oluşturma hücrelerini çalıştır

> Hücre sırasını atlama

---

### Soru Sor

Notebook içinde:

```text
Sorunu yaz (çıkmak için 'q'):
şeklinde bir alan çıkar.
Buraya sorunu yaz ve Enter’a bas.
```
