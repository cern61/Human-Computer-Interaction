<div align="center">

# 🧠 Gemini AI - Google Colab Kullanılabilirlik Analizi

**İnsan-Bilgisayar Etkileşimi (HCI) Projesi**

[![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://colab.research.google.com/)
[![Gemini AI](https://img.shields.io/badge/Gemini_AI-8E75B2?style=for-the-badge&logo=googlebard&logoColor=white)](#)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](#)
[![HTML/JS/CSS](https://img.shields.io/badge/Frontend-E34F26?style=for-the-badge&logo=html5&logoColor=white)](#)

*Yapay Zeka Entegrasyonlu Kod Asistanlarının Geliştirici Deneyimine Etkisi*

</div>

---

## 📌 Proje Hakkında

Bu proje, **İnsan-Bilgisayar Etkileşimi** dersi kapsamında, Google Colab içerisine entegre edilmiş **Gemini AI** kod asistanının kullanılabilirliğini ölçmek amacıyla gerçekleştirilmiştir. 

Farklı deneyim seviyelerinden (Düşük, Orta, Uzman) toplam 9 katılımcıdan, sadece doğal dil istemleri (prompt) kullanarak işlevsel bir **Sudoku oyunu** geliştirmeleri istenmiştir. Bu süreç; WCAG (Erişilebilirlik), Sezgisel Değerlendirme, SUMI, TAM ve Yenilik Yayılımı modelleri ile analiz edilmiştir.

**Proje Ekibi:** Ceren Naz Dervişoğlu & Pelin Almalı

---

## 🎮 En Başarılı Çıktı: Uzman Katılımcı Sudoku Oyunu

Bu depoda bulunan `game` (Notebook) dosyası, test grubumuzdaki uzman katılımcılardan birinin (Yüksek Seviye) Gemini AI'ı en verimli şekilde yönlendirerek elde ettiği **nihai, profesyonel Sudoku oyununu** içermektedir.

Sadece yapay zeka istemleriyle oluşturulan bu oyun, Colab hücresi içinde kusursuz çalışan bir web arayüzüne sahiptir.

### 🌟 Oyunun Özellikleri (AI Tarafından Üretildi)
*   ⏱️ **Dinamik Zamanlayıcı:** 10 dakikayı geçince uyarı veren akıllı sayaç.
*   🎚️ **Zorluk Seviyeleri:** Kolay, Orta, Zor (Algoritmik boşluk yönetimi).
*   💡 **İpucu Sistemi:** Tıkandığınızda doğru rakamı gösteren 3 haklı ipucu butonu.
*   ⌨️ **Klavye Desteği:** Yön tuşları (oklar) ile gezinme ve rakam/silme tuşlarıyla hızlı giriş.
*   🏆 **Lokal Skor Tablosu:** `localStorage` kullanılarak en iyi sürelerin kaydedilmesi ve listelenmesi.
*   🎨 **Görsel Geri Bildirim:** Seçili satır/sütun/kutu vurgulama, aynı rakamları parlatma ve anlık hata kontrolü (Yeşil/Kırmızı renk uyarıları).

### 🚀 Nasıl Çalıştırılır?
1. Dosyayı Google Colab'de açın.
2. `Python 3` kernel'inin seçili olduğundan emin olun.
3. İlk hücreyi (Sudoku tahta üretici Python mantığı) çalıştırın.
4. İkinci hücreyi (HTML/JS/CSS arayüz motoru) çalıştırın.
5. Hücre çıktısında beliren interaktif Sudoku tahtasında oynamaya başlayın!

---

## 📊 Kullanılabilirlik Araştırması Sonuçları

Gemini AI'ın Colab entegrasyonu, 9 katılımcı üzerinde 5 farklı akademik metotla test edilmiştir. İşte öne çıkan bulgular:

### 1. Teknolojiyi Kabul Modeli (TAM) ve Yenilik Yayılımı
*   **Algılanan Kullanım Kolaylığı (AKK):** Entegre "Kodu Hücreye Ekle (Insert)" butonu sayesinde özellikle düşük/deneyimsiz grupta memnuniyet tavan yapmıştır. Katılımcıların çoğu AKK'ye 7 üzerinden 6 veya 7 vermiştir.
*   **Kullanım Niyeti:** Katılımcıların **%88.9'u (8/9)** gelecekte bu aracı kesinlikle kullanacağını belirtmiştir. Araç, tüm gruplar tarafından "Tam Benimseme" seviyesinde kabul görmüştür.

### 2. SUMI (Yazılım Kullanılabilirlik Ölçümü)
*   Ortalama puanlar: Deneyimsiz grupta (4.1/5), Orta grupta (3.6/5), Uzman grupta (4.2/5).
*   Uzman kullanıcılar doğru *prompt* mühendisliği ile beklentilerinin üzerinde (K9 - 4.6 Puan) ürünler elde edebilmiştir.

### 3. Sezgisel Değerlendirme (Heuristic Evaluation)
| Sezgisel İlke | Bulgu | Kritiklik |
| :--- | :--- | :--- |
| **Kullanıcı Kontrolü** | "Insert" butonu bazen mevcut kodu güncellemek yerine sürekli yeni hücre açarak notebook'u kalabalıklaştırıyor. | Orta |
| **Sistem Durumu** | Üretilen oyunlardaki JS kaynaklı gizli hatalar arayüze yansımıyor, geliştirici konsolunu (F12) açmak gerekiyor. | **Kritik** |
| **Hata Önleme** | Yanlış eklenen bir kodu AI panelinden geri almak (Undo) sezgisel olarak zor. | Orta |

### 4. WCAG Erişilebilirlik (Accessibility)
*   **✅ Başarılı:** DOM sıralaması, ekran okuyucu uyumu, %200 yakınlaştırma (Zoom), hiyerarşik yapı.
*   **⚠️ Kısmi/İyileştirilebilir:** 
    *   Koyu temada üretilen kod bloklarındaki bazı syntax renkleri (Kontrast < 4.5:1).
    *   Dar ekranlarda Colab ana çalışma alanı ile Gemini panelinin üst üste binmesi.
    *   Hücreye kod aktarırken ekran okuyucu (Screen Reader) odaklanmasının otomatik kaymaması.

---

## 🎯 Sonuç ve Öneriler

Google Colab + Gemini AI entegrasyonu; **kullanıcı dostu, yüksek erişilebilirliğe sahip ve öğrenme eğrisini ciddi anlamda düşüren** bir yapıdadır. Hiç kod bilmeyen bir kullanıcının bile çalışan bir Sudoku oyunu yapabilmesi sistemin gücünü göstermektedir. 

**Geliştirme Önerileri:** Hata ayıklama süreçlerinde tarayıcı konsoluna bağımlılığı azaltmak için Colab içi daha güçlü bir *debugger* entegrasyonu ve kod ekleme (Insert/Replace) davranışının kullanıcıya daha net sunulması (UI revizyonu) gerekmektedir.
```eof