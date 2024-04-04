# gradient_descent
Bu metin, sıcaklığa bağlı olarak dondurma satışlarını tahmin eden basit bir doğrusal regresyon modelinin, gradient descent algoritması ile eğitilmiş Python kodunu içerir.

## Giriş
Dondurma satışları, çeşitli faktörlerden etkilenir, bunlardan biri de sıcaklıktır. Bu projede, sıcaklığa bağlı olarak dondurma satışlarını tahmin etmeyi amaçlıyoruz.

### Veri
Bu projede kullanılan veri seti "Ice Cream Sales - temperatures.csv" adını taşır. Bu veri seti "Temperature" ve "Ice Cream Profit" olmak üzere iki sütun içerir. Bağımsız değişken olarak sıcaklığı (X) ve bağımlı değişken olarak dondurma karını (y) kullanıyoruz.

## Yöntemler
### Fonksiyonlar
predict(x, w, b): Doğrusal regresyon formülünü kullanarak, sıcaklık (x), ağırlıklar (w) ve sapmayı (b) göz önünde bulundurarak dondurma karını tahmin eder.

compute_cost(X_train, y_train, w, b): Eğitim verisi (X_train, y_train), ağırlıklar (w) ve sapma (b) kullanılarak ortalama karesel hata maliyet fonksiyonunu hesaplar.

compute_gradient(X_train, y_train, w, b): Eğitim verisi (X_train, y_train) kullanılarak, maliyet fonksiyonunun ağırlıklar ve sapma üzerindeki gradyanlarını hesaplar.

gradient_descent(X_train, y_train, w, b, l_rate, num_iter, compute_cost, compute_gradient): Gradient descent optimizasyonunu gerçekleştirerek maliyet fonksiyonunu en aza indirir ve buna göre ağırlıkları ve sapmayı günceller.

### Değişkenler
X_train: Bağımsız değişken (Sıcaklık). 

y_train: Bağımlı değişken (Dondurma Karları).

w_init: Başlangıç ağırlıkları (rastgele oluşturulmuş).

b_init: Başlangıç sapması (0 olarak ayarlanmış).

l_rate: Gradient descent için öğrenme oranı.

num_iter: Gradient descent optimizasyonu için iterasyon sayısı.

## Sonuçlar
Gradient descent algoritması, ağırlıkları ve sapmayı maliyet fonksiyonunu minimize etmek için iteratif olarak günceller. 100 iterasyon sonunda, son ağırlıklar sıcaklığa bağlı olarak dondurma karını tahmin etmek için optimal değerlere yakınsar.

## Tartışma
Bu proje, sıcaklığa bağlı olarak dondurma satışlarını tahmin etmek için basit bir doğrusal regresyon modelinin, gradient descent algoritması ile nasıl eğitileceğini göstermektedir. Öğrenme oranı ve iterasyon sayısını ayarlayarak tahminlerin doğruluğunu artırabiliriz. Ancak gerçek dünya senaryolarında, daha karmaşık modeller ve ek özelliklerin tamamını yakalamak için daha fazla çaba gerekebilir.
