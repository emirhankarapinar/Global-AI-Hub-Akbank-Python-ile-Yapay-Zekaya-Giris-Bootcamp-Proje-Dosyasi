# Global-AI-Hub-Akbank-Python-ile-Yapay-Zekaya-Giris-Bootcamp-Proje-Dosyasi

1. Proje Başlığı ve Kısa Açıklama

Sürücüsüz Metro Simülasyonu (Rota Optimizasyonu)

Bu proje, bir metro ağında en az aktarmalı ve en hızlı rotayı bulan bir simülasyon geliştirmeyi amaçlamaktadır.

    En az aktarmalı rota için BFS (Breadth-First Search) algoritması kullanılmıştır.
    En hızlı rota için A (A-Star)* algoritması kullanılmıştır.
    Python dili ile geliştirilmiş olup heapq ve collections gibi kütüphanelerden yararlanılmıştır.

2. Kullanılan Teknolojiler ve Kütüphaneler
Kütüphane	Açıklama
collections	deque kullanarak BFS algoritmasını daha verimli hale getirmek için kullanılmıştır.
heapq	Öncelikli kuyruk (priority queue) yapısını kullanarak A* algoritmasını uygulamak için kullanılmıştır.
typing	Kodun daha okunabilir ve hata kontrolünü kolaylaştırmak için Dict, List, Tuple, Optional gibi veri tipleri belirtilmiştir.

3. Algoritmaların Çalışma Mantığı
BFS Algoritması (En Az Aktarmalı Rota)

Breadth-First Search (Genişlik Öncelikli Arama) algoritması kullanılarak bir noktadan diğerine en az istasyon değiştirerek ulaşmak hedeflenmiştir.
Adımlar:

    Başlangıç istasyonu bir kuyruğa eklenir.
    Her adımda ilk giren istasyon işlenir ve komşuları kuyruğa eklenir.
    Daha önce ziyaret edilen istasyonlar tekrar ziyaret edilmez.
    Hedef istasyona ulaşıldığında, en az aktarmayla geçilen istasyonlar listelenir.

A Algoritması (En Hızlı Rota)*

A* algoritması öncelikli kuyruk (priority queue) kullanarak en kısa sürede hedefe ulaşan rotayı hesaplar.
Adımlar:

    Başlangıç istasyonu öncelikli kuyruğa eklenir.
    En düşük süreye sahip olan istasyon işlenir.
    Komşu istasyonların toplam süresi hesaplanır ve en hızlı yol seçilir.
    Hedef istasyona ulaşıldığında, en hızlı rota ve toplam süre döndürülür.

4. Örnek Kullanım ve Test Sonuçları

Örnek test senaryolarında AŞTİ'den OSB'ye, Batıkent'ten Keçiören'e ve Keçiören'den AŞTİ'ye yolculuklar test edilmiştir.

Örnek Çıktı:
=== Test Senaryoları ===

1. AŞTİ'den OSB'ye:
En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
En hızlı rota (18 dakika): AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB

2. Batıkent'ten Keçiören'e:
En az aktarmalı rota: Batıkent -> Demetevler -> Gar -> Keçiören
En hızlı rota (21 dakika): Batıkent -> Demetevler -> Gar -> Keçiören

3. Keçiören'den AŞTİ'ye:
En az aktarmalı rota: Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ
En hızlı rota (16 dakika): Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ

5. Projeyi Geliştirme Fikirleri

    Grafiksel Arayüz: Kullanıcıların metro haritasını görerek rota seçmesini sağlayacak bir arayüz eklenebilir.
    Trafik Yoğunluğu: Günün farklı saatlerindeki yoğunluklara göre süre değişimi dinamik hale getirilebilir.
    Gerçek Metro Verisi: İstanbul, Ankara gibi şehirlerin metro hatları JSON dosyası ile programa entegre edilebilir.
    İstasyonlar Arasında Mesafe: Dijkstra algoritması kullanarak en kısa fiziksel mesafe hesaplanabilir.
