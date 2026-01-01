# DeepSeek

DeepSeek, gelişmiş yapay zeka modelleri ve kodlama asistanları geliştiren öncü bir kuruluştur. Açık kaynaklı modelleri ve güçlü performanslarıyla dikkat çekerler.

## Öne Çıkan Modeller

### DeepSeek-V3
DeepSeek-V3, güçlü bir Karışık Uzmanlar (Mixture-of-Experts - MoE) dil modelidir.
- **Parametre:** 671 Milyar (37 Milyar aktif)
- **Mimari:** Multi-head Latent Attention (MLA) ve DeepSeekMoE
- **Performans:** GPT-4 ve Claude 3.5 Sonnet ile rekabet edebilir düzeyde.
- **Kullanım:** Çok dilli NLP görevleri, yaratıcı yazarlık, soru-cevap.

### DeepSeek-Coder
Kodlama görevleri için özel olarak eğitilmiş, açık kaynaklı kod modelleri serisidir.
- **Context Window:** 16K - 128K token (versiyona göre)
- **Desteklenen Diller:** Python, Java, C++, JavaScript ve 80+ dil.
- **Yetenekler:** Kod tamamlama, hata ayıklama, birim test yazma.

## Kurulum ve Kullanım

### Python ile Kullanım (Hugging Face Transformers)

DeepSeek modellerini Python kütüphanesi ile kullanmak için aşağıdaki adımları izleyebilirsiniz:

```bash
pip install transformers torch
```

```python
from transformers import AutoTokenizer, AutoModelForCausalLM
import torch

model_name = "deepseek-ai/deepseek-coder-6.7b-instruct"
tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForCausalLM.from_pretrained(model_name, torch_dtype=torch.float16).cuda()

prompt = "Bana Python ile bir Fibonacci fonksiyonu yaz."
inputs = tokenizer(prompt, return_tensors="pt").to(model.device)

outputs = model.generate(**inputs, max_new_tokens=100)
print(tokenizer.decode(outputs[0], skip_special_tokens=True))
```

### API Kullanımı

DeepSeek API uyumlu bir OpenAI istemcisi ile de kullanılabilir:

```python
from openai import OpenAI

client = OpenAI(
    api_key="YOUR_DEEPSEEK_API_KEY",
    base_url="https://api.deepseek.com/v1"
)

response = client.chat.completions.create(
    model="deepseek-chat",
    messages=[
        {"role": "system", "content": "Sen yardımcı bir asistansın."},
        {"role": "user", "content": "Merhaba, nasılsın?"},
    ]
)

print(response.choices[0].message.content)
```

## Kaynaklar

- [DeepSeek Resmi Web Sitesi](https://www.deepseek.com/)
- [DeepSeek GitHub](https://github.com/deepseek-ai)
- [Hugging Face Modelleri](https://huggingface.co/deepseek-ai)
- [Teknik Makaleler](https://arxiv.org/search/cs?query=DeepSeek)
