# Stable Diffusion

Stable Diffusion, Stability AI tarafından geliştirilen, metin tanımlarından yüksek kaliteli görseller üreten açık kaynaklı bir derin öğrenme modelidir. Midjourney veya DALL-E'den farkı, tamamen **ücretsiz**, **açık kaynaklı** ve **kendi bilgisayarınızda çalıştırılabilir** olmasıdır.

## Nasıl Çalışır? (Basitleştirilmiş)
Stable Diffusion, "Diffusion" (Yayılma) modelini kullanır. Eğitim sırasında görsellere yavaş yavaş gürültü (noise) ekleyerek onları anlamsız bir piksel yığınına dönüştürür. Daha sonra bu süreci tersine çevirerek, gürültüden net bir görüntü oluşturmayı öğrenir. Siz bir metin (prompt) girdiğinizde, model bu metni rehber alarak gürültüden anlamlı bir görsel "yontar".

## Kullanım Yöntemleri

### 1. Kendi Bilgisayarınızda (Lokal Kurulum)
En popüler ve güçlü kullanım yöntemidir. Güçlü bir ekran kartı (NVIDIA GPU) gerektirir.

#### Popüler Arayüzler (WebUI):
*   **Automatic1111:** En yaygın, eklenti desteği en geniş topluluk standardı arayüz.
*   **ComfyUI:** Düğüm (node) tabanlı, daha karmaşık ama sonsuz özelleştirme imkanı sunan arayüz.
*   **Fooocus:** Midjourney kadar basit, kurulum gerektirmeyen minimalist arayüz.

### 2. Bulut Tabanlı (Online)
Donanımınız yetersizse kullanabileceğiniz servisler:
*   **DreamStudio:** Stability AI'ın resmi platformu.
*   **Clipdrop:** Gelişmiş düzenleme araçları sunan platform.
*   **Google Colab:** Ücretsiz GPU kullanarak (kısıtlı süreyle) Automatic1111 çalıştırmanızı sağlar.

## Temel Terimler ve Kavramlar

### Checkpoint (Model)
Görsel üretiminin temelidir. `.safetensors` uzantılı dosyalardır.
*   **SD 1.5:** Eski ama en çok eklentiye sahip sürüm.
*   **SDXL:** Daha yüksek çözünürlük ve detay sunan yeni sürüm.
*   **Civitai:** Binlerce özel eğitilmiş modeli bulabileceğiniz platform.

### LoRA (Low-Rank Adaptation)
Ana modele (Checkpoint) eklenen küçük eklentilerdir. Modeli değiştirmeden belirli bir stili, karakteri veya nesneyi çizmesini sağlar.
*   *Örnek:* "Anime LoRA"sı eklerseniz, model anime tarzında çizer.

### ControlNet
Görselin yapısını (poz, derinlik, kenar çizgileri) koruyarak üretim yapmanızı sağlar.
*   *Örnek:* Bir insan fotoğrafındaki pozu (duruşu) alıp, aynı pozda bir robot çizdirebilirsiniz.

### Prompting (İsteme)
*   **Pozitif Prompt:** Çizilmesini istedikleriniz (örn: `cat, cute, fluffy, cinematic lighting`).
*   **Negatif Prompt:** Çizilmesini **istemediklerini** (örn: `ugly, blurry, low quality, extra fingers`).

## Donanım Gereksinimleri (Lokal İçin)
*   **GPU:** NVIDIA RTX serisi (Tercihen 8GB VRAM ve üzeri).
*   **RAM:** Minimum 16GB.
*   **Depolama:** Modeller çok yer kapladığı için (her biri 2-6GB) geniş bir SSD.

## Kaynaklar
*   [Civitai](https://civitai.com/) (Model ve LoRA indirme merkezi)
*   [Hugging Face](https://huggingface.co/) (AI modellerinin GitHub'ı)
*   [Reddit r/StableDiffusion](https://www.reddit.com/r/StableDiffusion/)
