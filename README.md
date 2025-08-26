# Vietnam History Chat Datasets (VI & EN)

A family of synthetic, instruction-style **chat datasets** about **Vietnamese history (905–2025)**, designed for fine-tuning reasoning-capable chat models (e.g., GPT-OSS / Harmony, TRL).  
Each record follows a **ShareGPT/ChatML-like** `messages` structure with optional assistant reasoning in an `analysis` channel and a concise reply in `final`.

> **Use cases:** supervised fine-tuning (SFT) for text-generation and QA tasks; curriculum-style pretraining on historical knowledge; bilingual VI/EN experiments.

---

## 📚 Available datasets (Hugging Face)

- **500K (VI):** https://huggingface.co/datasets/minhxthanh/Vietnam-History-500K-Vi  
- **500K (EN):** https://huggingface.co/datasets/minhxthanh/Vietnam-History-500K-En  
- **200K (VI):** https://huggingface.co/datasets/minhxthanh/Vietnam-History-200K-Vi  
- **200K (EN):** https://huggingface.co/datasets/minhxthanh/Vietnam-History-200K-EN  
- **100K (VI):** https://huggingface.co/datasets/minhxthanh/Vietnam-History-100K_Vi  
- **100K (EN):** https://huggingface.co/datasets/minhxthanh/VietNam-History-100K_EN  
- **50K (VI):** https://huggingface.co/datasets/minhxthanh/Vietnam-History-50K  
- **25K (VI):** https://huggingface.co/datasets/minhxthanh/VietNam-History-25K  
- **15K (VI):** https://huggingface.co/datasets/minhxthanh/Vietnam-History-15k

> All datasets declare **MIT** license on their Hugging Face pages.  
> Tasks: Text Generation / Question Answering; Format: JSON; Modalities: Text; Languages: VI or EN (per dataset).

---

## 🔎 Data format

Each row is a JSON object with a single key `messages`:

```json
{
  "messages": [
    {"role": "system", "content": "You are a Vietnam history assistant. Explain briefly..."},
    {"role": "user", "content": "What happened in 1427?"},
    {"role": "assistant", "channel": "analysis", "content": "Reasoning..."},
    {"role": "assistant", "channel": "final", "content": "Decisive victories... Ended Ming occupation."}
  ]
}
