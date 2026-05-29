# turing_machine_binarymultiplication
# Turing Makinesi ile İkili (Binary) Çarpma Simülasyonu

Bu proje, iki adet ikili (binary) sayıyı girdi olarak alan ve bir **Turing Makinesi (Turing Machine)** mantığıyla bu sayıların çarpma işlemini simüle eden bir Python programıdır. Final Proje 1 ödevi kapsamında geliştirilmiştir.

Program, işlem adımlarını, durum geçişlerini (state transitions) ve banta (tape) yazılan her karakteri anlık olarak ekrana yazdırarak makinenin çalışma mekanizmasını görselleştirir.

## 🚀 Özellikler

* **Girdi Doğrulama:** Girilen verilerin sadece `0` ve `1` karakterlerinden oluştuğunu kontrol eder.
* **Bant Formatı:** Girdileri `A*B=` formatında bir banta dönüştürür ve sonsuz bant simülasyonu için sağ tarafı boşluk karakteri (`_`) ile doldurur.
* **Durum Geçiş Logları:** Her adımda makinenin mevcut durumu (`durum`), okunan karakter, yazılan karakter, kafa hareket yönü (SAĞ/SOL) ve bandın o anki durumu `[ ]` işaretçisiyle gösterilir.
* **Shift-and-Add Algoritması:** Çarpma işlemi, formal Turing Makinesi mantığına uygun şekilde kaydırma ve ekleme operasyonlarıyla simüle edilir.

## 🛠️ Kullanılan Durumlar (States)

* `q_baslangic`: İlk operandı tarar ve ayırıcı `*` karakterini bulur.
* `q_carpan_tara`: İkinci operandı (çarpan) tarayarak eşittir (`=`) sembolüne ulaşır.
* `q_topla`: Kaydırma ve toplama (Shift-and-add) mantığıyla sonucu hesaplar.
* `q_sonuc_yaz`: Hesaplanan binary sonucu bandın sonuna yazar.
* `q_kabul`: İşlem başarıyla tamamlandığında makinenin durduğu kabul durumudur.
* `q_red`: Hatalı veya geçersiz bir formatla karşılaşıldığında makinenin durduğu ret durumudur.

## 💻 Nasıl Çalıştırılır?

Projenin çalışması için herhangi bir harici kütüphaneye ihtiyaç yoktur. Standart Python 3 sürümü yeterlidir.

1. Depoyu klonlayın veya kod dosyasını indirin.
2. Terminal veya komut satırından şu komutla çalıştırın:
   ```bash
   python turing_machine_binarymultiplication.py
