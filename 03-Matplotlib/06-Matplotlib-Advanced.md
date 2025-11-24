# Matplotlib Gelişmiş Grafikler

Bu bölümde, Matplotlib ile daha karmaşık ve özelleştirilmiş görselleştirmeler oluşturmak için kullanılan ileri seviye teknikler ele alınmaktadır.
Amaç, grafiklerin profesyonel ve açıklayıcı hale getirilmesini sağlamaktır.

---

## 🎯 Öğrenme Hedefleri

* Birden fazla grafiği aynı figürde gösterebilmek (subplots)
* Grafik açıklamaları (annotations) eklemek
* Renk paletleri ve stilleri kullanmak
* Grafik boyutları, eksen sınırları ve yazı tiplerini özelleştirmek

---

## 🖼️ Birden Fazla Grafik (Subplots)

Matplotlib ile aynı figür üzerinde birden fazla grafik göstermek mümkündür. Bunun için `plt.subplots()` veya `plt.subplot()` fonksiyonu kullanılır.

```python
import matplotlib.pyplot as plt

aylar = ['Ocak', 'Şubat', 'Mart', 'Nisan', 'Mayıs']
satis_2023 = [120, 135, 160, 180, 200]
satis_2024 = [130, 140, 170, 195, 210]

fig, axs = plt.subplots(1, 2, figsize=(10, 4))

axs[0].plot(aylar, satis_2023, color='blue', marker='o')
axs[0].set_title('2023 Satışları')

axs[1].bar(aylar, satis_2024, color='orange')
axs[1].set_title('2024 Satışları')

plt.tight_layout()
plt.show()
```

> 💡 `figsize` parametresi ile grafik boyutlarını, `tight_layout()` ile boşluk ayarlarını düzenleyebilirsiniz.

---

## 📝 Grafiklere Açıklama (Annotation) Ekleme

Grafik üzerindeki belirli noktaları vurgulamak için açıklama metinleri eklemek oldukça faydalıdır.

```python
plt.plot(aylar, satis_2023, marker='o', color='green')
plt.title('Aylık Satışlar (2023)')
plt.xlabel('Ay')
plt.ylabel('Satış (bin adet)')

# Maksimum noktayı vurgula
max_value = max(satis_2023)
max_index = satis_2023.index(max_value)
plt.annotate(f'Maks: {max_value}', xy=(aylar[max_index], max_value),
             xytext=(aylar[max_index], max_value+10),
             arrowprops=dict(facecolor='black', shrink=0.05))

plt.show()
```

> Bu yöntem, veri içindeki önemli noktaları sunumlarda vurgulamak için idealdir.

---

## 🎨 Stil ve Tema Kullanımı

Matplotlib, önceden tanımlanmış birçok stil (tema) sunar. Stil değiştirmek için:

```python
plt.style.use('seaborn-v0_8-darkgrid')  # Mevcut stillerden birini seçin
```

Kullanılabilecek bazı stiller:

* `'ggplot'`
* `'seaborn-v0_8-darkgrid'`
* `'bmh'`
* `'classic'`
* `'Solarize_Light2'`

> Mevcut tüm stilleri görmek için: `plt.style.available`

---

## 🧩 Eksen Ayarları ve Grafik Boyutları

Eksen sınırlarını (`xlim`, `ylim`) ve grafik boyutlarını değiştirmek, görselleştirmeyi daha anlamlı hale getirir.

```python
plt.figure(figsize=(8, 5))
plt.plot(aylar, satis_2024, color='purple', linewidth=2, marker='s')
plt.title('2024 Satış Verileri')
plt.xlabel('Ay')
plt.ylabel('Satış (bin adet)')
plt.xlim(-0.5, 4.5)
plt.ylim(100, 250)
plt.grid(True, linestyle='--', alpha=0.6)
plt.show()
```

---

## 📊 Renk Paletleri ve Özelleştirme

Renk seçimleri, görselleştirmelerin okunabilirliğini doğrudan etkiler.
Aşağıdaki örnekte renk tonları ve stiller birleştirilmiştir.

```python
colors = ['#4e79a7', '#f28e2b', '#e15759', '#76b7b2', '#59a14f']

plt.bar(aylar, satis_2024, color=colors)
plt.title('Renk Paleti Örneği')
plt.show()
```

---

## 📈 Birleştirilmiş Grafikler (Overlay)

Aynı eksen üzerinde birden fazla veri serisini göstermek mümkündür.

```python
plt.plot(aylar, satis_2023, label='2023', marker='o')
plt.plot(aylar, satis_2024, label='2024', marker='s')
plt.title('Yıllık Satış Karşılaştırması')
plt.xlabel('Ay')
plt.ylabel('Satış (bin adet)')
plt.legend()
plt.show()
```

> `legend()` fonksiyonu, serileri etiketleyerek karşılaştırmayı kolaylaştırır.

---

## ⚠️ Dikkat Edilmesi Gerekenler

* Fazla bilgi içeren karmaşık grafiklerden kaçının.
* Stil ve renkleri tutarlı biçimde kullanın.
* Grafik açıklamaları ve etiketleri eksiksiz olmalıdır.

---

## 📚 Ek Kaynaklar

* [Matplotlib Subplots Kılavuzu](https://matplotlib.org/stable/gallery/subplots_axes_and_figures/subplots_demo.html)
* [Stil Seçenekleri](https://matplotlib.org/stable/gallery/style_sheets/style_sheets_reference.html)
* [Annotation Örnekleri](https://matplotlib.org/stable/gallery/annotations/annotation_basic.html)
