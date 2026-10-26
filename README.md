<div align="center">

<img src="logo.png" alt="e-Devlet Soyağacı → GEDCOM" width="220">

# e-Devlet Soyağacı → GEDCOM

**Resmî soy kaydınızı her soy ağacı programının açabildiği dosyaya çevirin**

_Tarayıcıda çalışan, Türkçe, kurulum gerektirmeyen dönüştürücü_

[![Dönüştürücüyü Aç](https://img.shields.io/badge/▶_Dönüştürücüyü_Aç-4a788a?style=for-the-badge)](https://kamilsaim.github.io/edevlet-ged/)

![Sürüm](https://img.shields.io/badge/sürüm-2.0-89a38c?style=flat-square)
![Tek dosya](https://img.shields.io/badge/tek_dosya-HTML-7ba3b8?style=flat-square)
![Gizlilik](https://img.shields.io/badge/veri-sunucuya_gitmez-c9a87c?style=flat-square)
![Dil](https://img.shields.io/badge/dil-Türkçe-b89ab8?style=flat-square)

</div>

---

## Ne işe yarar?

e-Devlet'teki **Nüfus ve Vatandaşlık İşleri → Alt-Üst Soy Bilgisi Sorgulama** ekranı; anne-babanızdan büyük dedelerinize, çocuklarınızdan torunlarınıza kadar resmî nüfus kaydını bir tablo olarak gösterir. Bu tablo kendi başına bir ağaç değildir: kimin kimin çocuğu olduğu yalnızca "Babasının Annesinin Babası" gibi yakınlık yazılarından anlaşılır.

Bu araç o tabloyu okuyup aile bağlarını kurar ve **GEDCOM (.ged)** dosyası üretir. GEDCOM, soy ağacı programlarının ortak dosya biçimidir; çıkan dosyayı [Soy Ağacı](https://kamilsaim.github.io/soyagaci/) uygulamasında ya da MyHeritage, Ancestry, FamilySearch, Gramps gibi programlarda açabilirsiniz.

🔒 Her şey tarayıcınızda işlenir. Kimlik ve aile bilgileriniz hiçbir sunucuya gönderilmez.

---

## Hızlı başlangıç

| Adım | Ne yapılır |
|:---:|---|
| **1** | e-Devlet'te **Alt-Üst Soy Bilgisi Sorgulama** ekranını açın |
| **2** | Tabloyu **"Sıra"** başlığından son kişiye kadar fareyle seçip kopyalayın (Ctrl+C) |
| **3** | [Dönüştürücüyü açın](https://kamilsaim.github.io/edevlet-ged/) ve yapıştırma alanına yapıştırın (Ctrl+V) |
| **4** | Tabloyu ve uyarıları kontrol edin → **GEDCOM Oluştur** → **İndir** |
| **5** | `.ged` dosyasını Soy Ağacı uygulamasında **Bilgi → Veri İşlemleri → GED Dosyası Yükle** ile açın |

> Tabloyu önce Excel'e ya da Word'e yapıştırıp kaydettiyseniz, o **.xlsx** veya **.docx** dosyasını da doğrudan yükleyebilirsiniz.

---

## Neleri aktarır?

| Belgedeki bilgi | GEDCOM'da |
|---|---|
| Ad, soyad, cinsiyet | Ad–soyad; isimler düzeltilir (HACI MEHMET → Hacı Mehmet) |
| Yakınlık derecesi | Anne–baba–çocuk bağları; birden çok çocuk ve torunlar baba/ana adından doğru kişiye bağlanır |
| Baba adı, ana adı | Belgede kaydı olmayan anne-babalar yalnızca adıyla eklenir (bir kuşak daha) |
| Doğum yeri ve tarihi | Doğum kaydı. NVİ'nin günü-ayı bilinmeyen eski doğumlar için yazdığı 01/07/YYYY yalnızca **yıl** olarak alınır |
| Durumu: Ölüm | Vefat kaydı; ölüm tarihi bilinmiyorsa "vefat etti, tarihi bilinmiyor" olarak işaretlenir |
| İl-ilçe-mahalle, cilt-hane-birey | Kişinin notuna "Nüfusa kayıtlı: …" olarak yazılır |
| Medeni hâli | Kişinin notuna yazılır |
| Kadınların soyadı | Babası belgedeyse kızlık soyadı ikinci ad kaydı olarak eklenir |

**Tutarsızlık uyarıları:** Bir kişinin "ana adı" ile belgedeki annesinin adı farklıysa (ör. *Ümmü Gülsüm* ↔ *Ümmügülsün*), yakınlık anlaşılamıyorsa ya da bir torunun hangi çocuğa ait olduğu bulunamıyorsa tablo üstünde uyarı gösterilir. Tablodaki alanları dönüştürmeden önce düzeltebilirsiniz.

---

## Teknik notlar

- Tek dosya: `index.html`. Excel okumak için yalnızca [SheetJS](https://sheetjs.com/) kullanılır; Word dosyası tarayıcının kendi sıkıştırma çözücüsüyle açılır.
- Çıktı GEDCOM 5.5.1, UTF-8. Her kişide belgedeki yakınlık `_YAKINLIK` etiketiyle de saklanır.
- Ataların yeri yakınlık yazısından kesin olarak bulunur ("Babasının Annesi" = baba → anne). Çocuk ve torunlar birden çok olabildiği için ebeveynleri, bir kuşak yukarıdaki adaylar arasından belgedeki baba/ana adıyla eşleştirilerek bulunur.

---

## Sürüm geçmişi

| Sürüm | Öne çıkanlar |
|---|---|
| **2.0** | Baştan yazıldı. Aile bağları artık doğru kuruluyor (eski sürümde atalar ağaca bağlanmıyor, anne-babalar mükerrer ekleniyordu) · e-Devlet sayfasından doğrudan yapıştırma ve Word (.docx) desteği · birden çok çocuk ve torun desteği · isim düzeltme, kızlık soyadı, nüfus kaydı notu · tutarsızlık uyarıları · yeni logo |
| **1.0** | İlk sürüm — Excel'den GEDCOM'a dönüştürme |

---

<div align="center">
<sub>e-Devlet ve Nüfus ve Vatandaşlık İşleri Genel Müdürlüğü ile resmî bir bağlantısı yoktur; belgenin kişisel kullanım için dönüştürülmesine yardımcı olur.</sub>
</div>
