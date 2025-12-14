# genetik_optimizasyonu

# Genetik Algoritma ile Laboratuvar Numune Karışımı Optimizasyonu

Bu proje, bir biyoteknoloji laboratuvarında kullanılan test çözeltilerinin
en verimli karışım oranlarını bulmak amacıyla
**Genetik Algoritma (Genetic Algorithm - GA)** kullanılarak geliştirilmiştir.

Amaç, verilen **amaç fonksiyonunu maksimize eden**
reaktif oranlarını, belirli kısıtlar altında belirlemektir.

---

##  Problem Tanımı

Bir biyoteknoloji firması, laboratuvarda kullanılan test çözeltilerinin
hassasiyetini artırmak istemektedir.

Test hassasiyeti, aşağıdaki matematiksel amaç fonksiyonu ile ifade edilmektedir.

###  Amaç Fonksiyonu

\[
y = 3x_1 + 2x_2 + x_1x_2 - 0.5x_2^2
\]

- **y** : Test hassasiyeti puanı  
- **x₁** : Reaktif A oranı (%)  
- **x₂** : Reaktif B oranı (%)  

Amaç, **y değerini maksimize etmektir**.

---

##  Değişkenler ve Aralıklar

- **x₁ (Reaktif A)** : 10 ≤ x₁ ≤ 80  
- **x₂ (Reaktif B)** : 10 ≤ x₂ ≤ 80  

---

##  Kısıtlar

- x₁ + x₂ ≤ 100  
- x₁ ≥ 25  

Bu kısıtlar, çözelti karışımının laboratuvar koşullarına uygun olmasını sağlar.

---

##  Kullanılan Yöntem: Genetik Algoritma

Bu projede optimizasyon problemi **Genetik Algoritma** ile çözülmüştür.

### Algoritma Adımları

1. Rastgele ve kısıtları sağlayan başlangıç popülasyonunun oluşturulması  
2. Amaç fonksiyonuna göre uygunluk (fitness) hesaplanması  
3. Turnuva seçimi (Tournament Selection) ile ebeveyn seçimi  
4. Aritmetik çaprazlama (Crossover)  
5. Mutasyon işlemi  
6. Kısıtlara uymayan bireylerin elenmesi  
7. En iyi bireyin nesiller boyunca takip edilmesi  

---

##  Algoritma Parametreleri

| Parametre | Değer |
|---------|------|
| Popülasyon Boyutu | 40 |
| Jenerasyon Sayısı | 80 |
| Seçim Yöntemi | Turnuva Seçimi (k = 3) |
| Mutasyon Oranı | 0.1 |
| Çaprazlama | Aritmetik Crossover |

---

##  Kullanılan Teknolojiler

    - Python 3.x  
    - NumPy  
    - Random  
    - Matplotlib  
    - Jupyter Notebook  
