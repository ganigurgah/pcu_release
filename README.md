# 🌌 PCU: Personal Computer User

![PCU Hero Banner](doc/images/release/hero_banner.png)

<div align="center">
  <h3><b>"Siz Bir Sonraki Büyük Adımı Düşünürken, O Sizin İçin Mevcut Olanı İnşa Eder."</b></h3>
  <p><i>Kahvenizi Yudumlayın, Planlarınız Uygulansın.</i></p>

  [![Version](https://img.shields.io/badge/version-2.1.8-blueviolet?style=for-the-badge)](https://github.com/ganigurgah/pcu_release/releases)
  [![License](https://img.shields.io/badge/license-Personal-brightgreen?style=for-the-badge)](LICENSE)
  [![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20Windows%20%7C%20macOS-orange?style=for-the-badge)](#kurulum)
</div>

---

## 🚀 PCU Nedir?

**PCU (Personal Computer User)**, bilgisayarınızı doğal dil komutlarıyla yönetmenizi sağlayan, yerel ve bulut yapay zeka modellerini mükemmel bir uyumla birleştiren yeni nesil bir otonom asistandır. Sadece bir asistan değil, işletim sisteminizin üzerinde dönen akıllı bir katmandır.

### Neden PCU?
Geleneksel asistanların aksine PCU, **Local-First (Önce Yerel)** felsefesiyle çalışır. Verileriniz sizin cihazınızda kalır, komutlarınız doğrudan terminalin gücüyle icra edilir.

---

## ⚙️ Nasıl Çalışır? (Teknik Mimari)

PCU bir "Orkestra Şefi" gibi çalışır. Girdiğiniz her komut önce bir sınıflandırıcıdan geçer ve ardından en uygun motora (Sistem, LLM veya Agent) yönlendirilir.

<details>
<summary><b>🔍 Mimari Şemayı Görüntüle (Mermaid)</b></summary>

```mermaid
graph TD
    User((Kullanıcı)) -->|Doğal Dil / Ses| PCU[PCU Web/Terminal]
    PCU --> Classifier{Classifier}
    Classifier -->|BILGISAYAR| SysCmd[Sistem Komutları]
    Classifier -->|SORU/ARAMA| LLM[LLM Engine]
    Classifier -->|GELISTIRME| AG[Claude / Gemini / Your Choice]
    LLM --> WebSearch[Web Search]
    LLM --> Memory[(Smart Memory)]
    SysCmd --> OS[Linux/MacOS/Windows]
    AG --> Codebase[Kaynak Kod]
```
</details>

---

## ✨ Öne Çıkan Özellikler

<table border="0">
  <tr>
    <td width="50%">
      <h3>🔒 Yerel Otonomi & Gizlilik</h3>
      <p>Ollama entegrasyonu sayesinde tamamen çevrimdışı çalışabilir. Verileriniz asla izniniz dışında internete çıkmaz.</p>
    </td>
    <td width="50%">
      <img src="doc/images/release/local_icon.png" width="200" align="right"/>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <img src="doc/images/release/ai_icon.png" width="200" align="left"/>
    </td>
    <td width="50%">
      <h3>🤖 Hibrit AI Zekası</h3>
      <p>Claude (Antigravity), Gemini ve yerel modeller arasında anlık geçiş yapın. Karmaşık kodlama görevlerinden basit hatırlatıcılara kadar her şeyi yönetin.</p>
    </td>
  </tr>
</table>

### 💎 Neler Yapabilir?
*   **🎙️ Tam Sistem Kontrolü:** "Mail hazırla", "Spotify'ı başlat", "Ekran görüntüsü al" gibi komutları doğal dilde verin.
*   **🧠 Akıllı Hafıza:** Sizin tercihlerinizi, API anahtarlarınızı ve favori çalışma dizinlerinizi unutmaz.
*   **🔍 Ara & Özetle:** İnternetten sizin için araştırma yapar, sayfalarca bilgiyi saniyeler içinde özetler.
*   **📊 Görsel Raporlama:** Sistem performansını ve AI yanıtlarını modern grafiklerle sunar.

---

## 🛠️ Kurulum ve Başlangıç

PCU'yu kullanmaya başlamak için işletim sisteminize uygun olan paketi [Releases](https://github.com/ganigurgah/pcu_release/releases) sekmesinden indirin.

### 1️⃣ Paketi İndirin
*   **Windows:** `pcu-windows.zip`
*   **Linux:** `pcu-linux.zip`
*   **macOS:** `pcu-macos.zip`

### 2️⃣ Kurulumu Çalıştırın
Zip dosyasını bir klasöre çıkartın ve terminalden (veya PowerShell'den) şu komutu çalıştırın:

**Linux / macOS:**
```bash
chmod +x install_pcu.sh && ./install_pcu.sh
```

**Windows:**
```powershell
./install_pcu.ps1
```

---

## ⌨️ Temel Kullanım

Arayüzü açmak için tarayıcınızdan `http://localhost:8765` adresine gidin ve komut vermeye başlayın. PCU hem teknik komutları hem de günlük konuşma dilini anlar:

### 🗣️ Doğal Dil Örnekleri
*   *"PCU, mail hazırla"* — E-posta istemcinizi otomatik açar.
*   *"WhatsApp'tan günaydın yaz"* — Mesajınız hazır şekilde Web WhatsApp'ı açar.
*   *"5 dakika sonra çayı kontrol et diye hatırlat"* — Masaüstü bildirimi gönderir.
*   *"Nvidia hisselerindeki son durumu ara ve özetle"* — Web'den güncel veriyi çekip sunar.
*   *"Yarın sabah 10:00 için toplantı ekle ve şu kişilere mail gönder"* — Takviminize toplantıyı ekler ve katılımcılara otomatik davetiye iletir.

### 🛠️ Teknik Komutlar & Prefiksler
*   `! ls -la` — Doğrudan terminal komutu çalıştırır.
*   `@ag bu projedeki hataları bul` — Antigravity (Claude) motorunu tetikler.
*   `bunu hatırla: Ofisimin adresi Levent/İstanbul` — Kalıcı hafızaya kaydeder.
*   `/status` — Sistem performansını grafik olarak sunar.

---

## 💬 Geri Bildirim ve Destek

PCU'yu geliştirmemize yardımcı olun! Karşılaştığınız hataları veya yeni özellik fikirlerinizi [Issues](https://github.com/ganigurgah/pcu_release/issues) sekmesinden bize iletebilirsiniz.

> [!TIP]
> **Hata Bildirirken:** Lütfen işletim sisteminizi ve kullandığınız PCU sürümünü belirtmeyi unutmayın.

---

<div align="center">
  <p><i>Geleceğin bilgisayar kullanım deneyimini bugünden yaşayın.</i></p>
  <p><b>PCU: Personal Computer User</b></p>
  <p>Built with ❤️ by <b>Gani Gurgah</b></p>
</div>
