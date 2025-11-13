# Matplotlib Temelleri

Bu bölümde, Python’un en yaygın görselleştirme kütüphanelerinden biri olan **Matplotlib**’in temelleri ele alınmaktadır.
Matplotlib, veri görselleştirme sürecinde en çok kullanılan ve esnekliği yüksek bir araçtır.

---

## 🎯 Öğrenme Hedefleri

* Matplotlib kütüphanesini tanımak
* Temel grafik türlerini (çizgi, çubuk, dağılım) oluşturmak
* Başlık, eksen isimleri ve renk ayarlarını düzenlemek
* Grafik tasarımında özelleştirme yöntemlerini öğrenmek

---

## 📦 Matplotlib Nedir?

Matplotlib, Python’da veri görselleştirme için en temel kütüphanelerden biridir.
`matplotlib.pyplot` modülü genellikle **plt** kısaltmasıyla kullanılır ve grafik oluşturmak için yüksek seviyeli fonksiyonlar sağlar.

```python
import matplotlib.pyplot as plt
```

---

## 📈 Çizgi Grafiği Oluşturma

En basit grafik türlerinden biri çizgi grafiklerdir. Genellikle zaman serisi verileri veya eğilimleri göstermek için kullanılır.

```python
import matplotlib.pyplot as plt

aylar = ['Ocak', 'Şubat', 'Mart', 'Nisan', 'Mayıs']
satis = [120, 135, 160, 180, 200]

plt.plot(aylar, satis)
plt.title('Aylık Satış Grafiği')
plt.xlabel('Ay')
plt.ylabel('Satış (bin adet)')
plt.show()
```
![](05-01.png)  

> [!TIP]İpucu
> `marker='o'` parametresi ile veri noktalarına işaret ekleyebilirsiniz.

---

## 📊 Çubuk (Bar) Grafiği

Kategorik veriler arasındaki farkı göstermek için çubuk grafikleri kullanılır.

```python
departmanlar = ['Satış', 'Pazarlama', 'Üretim', 'AR-GE']
calisan_sayilari = [25, 18, 32, 15]

plt.bar(departmanlar, calisan_sayilari, color='#4e79a7')
plt.title('Departman Bazlı Çalışan Sayısı')
plt.ylabel('Kişi Sayısı')
plt.show()
```
![](05-02.png)  

> [!IMPORTANT]Önemli
> Dikey çubuk grafiği `plt.bar()`, yatay çubuk grafiği ise `plt.barh()` fonksiyonu ile oluşturulur.

---

## 🔵 Dağılım (Scatter) Grafiği

İki değişken arasındaki ilişkiyi görselleştirmek için kullanılır.

```python
x = [10, 20, 30, 40, 50]
y = [8, 15, 25, 35, 45]

plt.scatter(x, y, color='#e15759')
plt.title('Dağılım Grafiği')
plt.xlabel('Bağımsız Değişken')
plt.ylabel('Bağımlı Değişken')
plt.show()
```
![](05-03.png)  

---

## 🎨 Grafik Özelleştirme

Grafikleri daha okunabilir hale getirmek için çeşitli stil ayarları yapılabilir.

```python
plt.plot(aylar, satis, color='green', linestyle='--', marker='o', linewidth=2)
plt.title('Özelleştirilmiş Çizgi Grafiği', fontsize=14)
plt.xlabel('Ay', fontsize=12)
plt.ylabel('Satış (bin adet)', fontsize=12)
plt.grid(True, linestyle='--', alpha=0.6)
plt.show()
```
![](05-04.png)  

### Diğer Stil Özellikleri

* `color` → Renk (örneğin `'red'`, `'#4e79a7'`)
* `linestyle` → Çizgi tipi (`'-'`, `'--'`, `':'`)
* `marker` → Nokta işareti (`'o'`, `'s'`, `'d'`)
* `linewidth` → Çizgi kalınlığı

---

## 🧩 Birden Fazla Grafik (Subplots)

Birden fazla grafiği aynı figür üzerinde göstermek için `plt.subplot()` fonksiyonu kullanılabilir.

```python
plt.figure(figsize=(10, 4))

plt.subplot(1, 2, 1)
plt.plot(aylar, satis, color='blue')
plt.title('Çizgi Grafik')

plt.subplot(1, 2, 2)
plt.bar(aylar, satis, color='orange')
plt.title('Çubuk Grafik')

plt.tight_layout()
plt.show()
```
![](05-05.png)  

---

## ⚠️ Sık Yapılan Hatalar

* Eksensiz veya başlıksız grafik oluşturmak
* Renk kontrastlarını dikkate almamak
* Çok fazla veriyle karmaşık grafikler üretmek

---

## 📚 Ek Kaynaklar

* [Matplotlib Kullanım Kılavuzu](https://matplotlib.org/stable/users/getting_started/)
* [Matplotlib Stil Galerisi](https://matplotlib.org/stable/gallery/style_sheets/style_sheets_reference.html)
