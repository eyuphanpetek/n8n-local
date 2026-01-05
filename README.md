# 🤖 Akıllı Müşteri İçgörü Asistanı (v2.8)

Bu proje, müşteri geri bildirimlerini anlık olarak analiz eden, duygusunu (sentiment) ölçen, geçmiş müşteri etkileşimlerini kontrol eden ve kurumsal bilgi bankasına (RAG) dayanarak profesyonel yanıtlar üreten yapay zeka destekli bir otomasyon sistemidir.

![Arayüz Önizlemesi](https://via.placeholder.com/800x400?text=Premium+Dashboard+UI)

## ✨ Özellikler

- **🧠 Akıllı Analiz:** Groq (Llama-3.3 70B) kullanarak derinlemesine duygu ve içerik analizi.
- **📊 Canlı Dashboard:** Toplam analiz sayısı, genel puan ortalaması ve memnuniyet oranlarını anlık takip.
- **📚 Bilgi Bankası (RAG):** n8n içinde gömülü FAQ sayesinde şirket kurallarına ve ürün bilgilerine dayalı doğru cevaplar.
- **🕒 Müşteri Geçmişi:** Google Sheets entegrasyonu ile müşterinin geçmiş yorumlarını hatırlayan "bağlamsal" zeka.
- **🎭 Ton Seçimi:** Cevapların "Profesyonel", "Samimi" veya "Resmi" tonda üretilmesini sağlama.
- **🎤 Gelişmiş Sesle Yazma:** Canlı önizleme, hata yönetimi ve Türkçe dil desteği ile sesli geri bildirim girişi.
- **🎨 Premium UI:** Modern Glassmorphism tasarımı, Skeleton Loader ve Konfeti kutlamaları.

## 🛠️ Teknoloji Yığını

- **Frontend:** Vanilla HTML5, CSS3 (Modern Glassmorphism), JavaScript (ES6+).
- **Backend:** [n8n](https://n8n.io/) (Self-hosted Docker).
- **AI / LLM:** [Groq Cloud](https://groq.com/) (Llama 3.3 70B).
- **Database:** Google Sheets API.
- **Tunnel:** [ngrok](https://ngrok.com/) (Permanent Static Domain).
- **Deployment:** [Vercel](https://vercel.com/) (Frontend), Local Docker (Backend).

## 🚀 Kurulum

### 1. n8n Kurulumu

Projedeki son sürüm olan `.json` dosyasını (`Akıllı Müşteri İçgörü Asistanı v2.8 - Real Stats.json`) indirin ve n8n arayüzünden **Import** edin.

### 2. Kimlik Bilgileri

n8n içinde aşağıdaki servisler için `Credentials` tanımlamanız gerekmektedir:

- **Groq API:** LLM analizi için.
- **Google Sheets OAuth2:** Verilerin kaydı ve geçmiş sorgusu için.

### 3. Frontend Bağlantısı

`index.html` içindeki `N8N_BASE_URL` değişkenini kendi n8n webhook URL'nizle güncelleyin:

```javascript
const N8N_BASE_URL = 'https://nonsuppressive-pluggingly-carlota.ngrok-free.dev';
```

### 4. Yayına Alma

GitHub reponuzu Vercel'e bağlayarak frontend kısmını saniyeler içinde yayına alabilirsiniz.

## 📁 Proje Yapısı

```text
├── index.html          # Ana Dashboard ve Kullanıcı Arayüzü
├── bilgi_bankasi.md    # AI için referans dökümanı
├── workflows/          # n8n Workflow JSON dosyaları (v1.0 - v2.8)
└── README.md           # Proje dökümantasyonu
```

## 📝 Lisans

Bu proje eğitim ve geliştirme amaçlı oluşturulmuştur
---

**Geliştirici:** [Eyüphan Petek](https://github.com/eyuphanpetek)
