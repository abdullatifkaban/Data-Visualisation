# 📊 Veri Görselleştirme

Bu kurs, elinizdeki ham veriyi anlamlı ve etkili grafiklere dönüştürme becerisini sıfırdan öğretir. Yolculuk görselleştirmenin neden önemli olduğu ve doğru grafik türünün nasıl seçileceği gibi kavramlarla başlar; Anaconda ve Jupyter ortamının kurulması, Python ve pandas ile veri hazırlığı, matplotlib ve seaborn ile statik grafikler, plotly ve folium ile etkileşimli görselleştirmeler üzerinden ilerler ve gerçek bir veri setiyle hazırlanan mini projeyle biter. Tüm dersler, kodu doğrudan çalıştırıp sonuçlarını hemen görebileceğiniz Jupyter defterleri biçimindedir.

## 👥 Hedef Kitle

Üniversite 1. sınıf düzeyinde, bölüm bağımsız bir derstir; programlama veya veri analizi ön bilgisi gerekmez. Kurulumdan Python temeline kadar her şey ders içinde adım adım anlatılır. Dersi bir eğitmen eşliğinde almayan, depoyu kendi başına keşfeden öğrenciler de aynı sırayla izleyebilir.

## 🗂️ İçerik

### 📖 Temel Kavramlar

- [Giriş: Veri Görselleştirme](Topics/01-Visualization-Intro.ipynb)  
*(Görselleştirmenin amacı, görsel algı, tasarım ilkeleri ve yanıltıcı grafikler)*
- [Grafik Türleri ve Doğru Seçim](Topics/02-Chart-Types.ipynb)  
*(Veri türüne ve amaca göre grafik seçimi, renk kullanımının temelleri)*

### 🧰 Ortam ve Veri Hazırlığı

- [Ortam Kurulumu: Anaconda ve Jupyter](Topics/03-Environment-Setup.ipynb)  
*(Anaconda kurulumu, Jupyter Notebook kullanımı ve sık karşılaşılan sorunlar)*
- [Python'a Yumuşak Giriş](Topics/04-Python-Basics.ipynb)  
*(Değişken, liste, fonksiyon çağrısı ve hata mesajı okuma)*
- [pandas DataFrame](Topics/05-Pandas-Dataframe.ipynb)  
*(CSV okuma, seçme, filtreleme, gruplama ve özetleme)*
- [Veri Temizleme ve Keşfedici Analiz](Topics/06-Data-Cleaning.ipynb)  
*(Eksik ve aykırı değerleri bulma, veri temizleme ve EDA akışı)*

### 📈 Matplotlib

- [Matplotlib Temelleri](Topics/07-Matplotlib-Basics.ipynb)  
*(Çizgi, çubuk ve dağılım grafikleri; başlık, eksen ve renk ayarları)*
- [Matplotlib İleri Düzey](Topics/08-Matplotlib-Advanced.ipynb)  
*(Çoklu grafikler, figure-axes yapısı, stiller ve grafiği dosyaya kaydetme)*

### 🎨 Seaborn

- [Seaborn Temelleri](Topics/09-Seaborn-Basics.ipynb)  
*(Histogram, boxplot ve barplot; tema ve palet kullanımı)*
- [Seaborn İleri Düzey](Topics/10-Seaborn-Advanced.ipynb)  
*(Heatmap, pairplot, jointplot, catplot ve facetgrid)*

### ✨ İleri Görselleştirme Teknikleri

- [Zaman Serileri Görselleştirme](Topics/11-Time-Series.ipynb)  
*(Tarih verisi, trendler, hareketli ortalama ve animasyonlar)*
- [Etkileşimli Grafikler: plotly](Topics/12-Interactive-Plots.ipynb)  
*(Etkileşimli çizgi, çubuk ve dağılım grafikleri; hover, zoom ve pan)*
- [Coğrafi Görselleştirme: folium](Topics/13-Geographical-Maps.ipynb)  
*(Harita üzerinde nokta ve daire işaretler)*
- [Üç Boyutlu Grafikler](Topics/14-Three-Dimensional-Plots.ipynb)  
*(3B dağılım ve yüzey grafikleri; 3B'nin uygun ve yanıltıcı kullanımı)*

### 🏁 Proje

- [Veriyle Hikâye Anlatımı](Topics/15-Data-Storytelling.ipynb)  
*(Mesaj, sıralama ve vurgu ile izleyiciye göre görselleştirme)*
- [Mini Proje](Topics/16-Mini-Project.ipynb)  
*(Gerçek bir veri setiyle sorudan sunuma uzanan bitirici çalışma)*

## 🧰 Yardımcı Araç: Grafik Atölyesi

Derslerde öğrendiklerini kendi verinle denemek için ayrı bir depoda küçük bir
Streamlit uygulaması var: **[Grafik Atölyesi](https://github.com/abdullatifkaban/Chart-Builder)**.
CSV ya da Excel dosyanı yüklediğinde sütunları tanır, çizilebilecek grafikleri
listeler ve aynı grafiği pandas, matplotlib ve seaborn ile ayrı ayrı çizip
**Python kodunu** gösterir.

## 💻 Gereksinimler

- Anaconda (Python 3 ile) — kurulumu 3. derste adım adım anlatılır
- Jupyter Notebook (Anaconda ile birlikte gelir; VS Code içinde de kullanılabilir)
- pandas, matplotlib, seaborn (Anaconda ile hazır gelir)
- plotly ve folium (kurulumları ilgili derslerde anlatılır)
- İnternet bağlantısı (kurulum ve bazı veri setleri için)

---
> Son Güncellenme Tarihi: **`7 Kasım 2026`**
