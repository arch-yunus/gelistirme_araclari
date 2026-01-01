# Teachable Machine with Google

Teachable Machine, Google tarafından geliştirilen, hiç kod yazmadan (no-code) hızlı ve kolay bir şekilde makine öğrenmesi modelleri eğitmenizi sağlayan web tabanlı bir araçtır. Özellikle yapay zeka ve makine öğrenmesi mantığını anlamak, hızlı prototipler üretmek veya eğitim projeleri hazırlamak için mükemmeldir.

## Neler Yapabilirsiniz?

Teachable Machine şu an için 3 ana proje türünü destekler:

### 1. Görüntü Projesi (Image Project)
Kameranızı kullanarak veya dosya yükleyerek nesneleri sınıflandırabilirsiniz.
- **Örnek:** Kameraya "Elma" gösterdiğinizde sistemin bunu tanıması, "Muz" gösterdiğinizde ayırt etmesi.
- **Kullanım:** Ürün tanıma, yüz tanıma prototipleri.

### 2. Ses Projesi (Audio Project)
Mikrofonu kullanarak farklı sesleri veya kelimeleri ayırt etmeyi öğretebilirsiniz.
- **Örnek:** Alkış sesi ile parmak şıklatma sesini ayırt eden bir model.
- **Kullanım:** Sesli komut sistemleri.

### 3. Poz Projesi (Pose Project)
Vücut duruşlarını (insan iskelet yapısını) algılar.
- **Örnek:** Kamer karşısında "Sağ el havada" veya "Kafa sola eğik" gibi durumları tespit etmesi.
- **Kullanım:** Egzersiz takip uygulamaları, jest kontrol sistemleri.

## Nasıl Kullanılır? (3 Adımda ML)

### Adım 1: Veri Topla (Gather)
Sınıflar (Class) oluşturun ve her sınıf için örnek veri toplayın.
*   *Örnek:* "Class 1" adını "Kitap" yapın ve kameraya kitap göstererek butona basılı tutun. Yüzlerce kare fotoğrafı saniyeler içinde çekecektir.

### Adım 2: Eğit (Train)
"Train Model" butonuna basın. Tarayıcınız, topladığınız verileri kullanarak bir sinir ağı (neural network) eğitir. Bu işlem genellikle birkaç saniye veya dakika sürer.

### Adım 3: Dışa Aktar (Export)
Modelinizi test ettikten sonra indirip kendi projelerinizde kullanabilirsiniz.
*   **TensorFlow.js:** Web sitelerinde kullanım için.
*   **TensorFlow Lite:** Mobil uygulamalar (Android/iOS) için.
*   **TensorFlow:** Python projeleri için.

## Entegrasyon Örnekleri

Eğittiğiniz modeli dışa aktardıktan sonra size verilen kod parçacığını web sitenize ekleyerek hemen kullanmaya başlayabilirsiniz.

```html
<!-- TensorFlow.js ile Model Kullanım Örneği -->
<div>Teachable Machine Image Model</div>
<button type="button" onclick="init()">Start</button>
<div id="webcam-container"></div>
<div id="label-container"></div>
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@latest/dist/tf.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@teachablemachine/image@latest/dist/teachablemachine-image.min.js"></script>
```

## Kaynaklar

*   [Resmi Web Sitesi](https://teachablemachine.withgoogle.com/)
*   [Proje Galerisi](https://teachablemachine.withgoogle.com/train) (İlham almak için örnek projeler)
