# gradient_descent
Bu metin, sıcaklığa bağlı olarak dondurma satışlarını tahmin eden basit bir doğrusal regresyon modelinin, gradient iniş algoritması ile eğitilmiş Python betiğini içerir.

## Giriş
Dondurma satışları, çeşitli faktörlerden etkilenir, bunlardan biri de sıcaklıktır. Bu projede, sıcaklığa bağlı olarak dondurma satışlarını tahmin etmeyi amaçlıyoruz.

### Veri
Bu projede kullanılan veri seti "Dondurma Satışları - sıcaklıklar.csv" adını taşır. Bu veri seti "Sıcaklık" ve "Dondurma Karları" olmak üzere iki sütun içerir. Bağımsız değişken olarak sıcaklığı (X) ve bağımlı değişken olarak dondurma karını (y) kullanıyoruz.

## Yöntemler
### Fonksiyonlar
predict(x, w, b): Doğrusal regresyon formülünü kullanarak, sıcaklık (x), ağırlıklar (w) ve sapmayı (b) göz önünde bulundurarak dondurma karını tahmin eder.
compute_cost(X_train, y_train, w, b): Eğitim verisi (X_train, y_train), ağırlıklar (w) ve sapma (b) kullanılarak ortalama karesel hata maliyet fonksiyonunu hesaplar.
compute_gradient(X_train, y_train, w, b): Eğitim verisi (X_train, y_train) kullanılarak, maliyet fonksiyonunun ağırlıklar ve sapma üzerindeki gradyanlarını hesaplar.
gradient_descent(X_train, y_train, w, b, l_rate, num_iter, compute_cost, compute_gradient): Gradient iniş optimizasyonunu gerçekleştirerek maliyet fonksiyonunu en aza indirir ve buna göre ağırlıkları ve sapmayı günceller.
### Değişkenler
X_train: Bağımsız değişken (Sıcaklık).
y_train: Bağımlı değişken (Dondurma Karları).
w_init: Başlangıç ağırlıkları (rastgele oluşturulmuş).
b_init: Başlangıç sapması (0 olarak ayarlanmış).
l_rate: Gradient iniş için öğrenme oranı.
num_iter: Gradient iniş optimizasyonu için iterasyon sayısı.
## Sonuçlar
Gradient iniş algoritması, ağırlıkları ve sapmayı maliyet fonksiyonunu minimize etmek için iteratif olarak günceller. 100 iterasyon sonunda, son ağırlıklar sıcaklığa bağlı olarak dondurma karını tahmin etmek için optimal değerlere yakınsar.

## Tartışma
Bu proje, sıcaklığa bağlı olarak dondurma satışlarını tahmin etmek için basit bir doğrusal regresyon modelinin, gradient iniş algoritması ile nasıl eğitileceğini göstermektedir. Öğrenme oranı ve iterasyon sayısını ayarlayarak tahminlerin doğruluğunu artırabiliriz. Ancak gerçek dünya senaryolarında, daha karmaşık modeller ve ek özelliklerin tamamını yakalamak için daha fazla çaba gerekebilir.
