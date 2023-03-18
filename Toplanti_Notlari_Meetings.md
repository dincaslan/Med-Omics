# Tüm Toplantı Notları (Meeting Notes)

<details>

<summary>26/3/22 Tanışma</summary>

### Toplantı 1

Kodlama değil, araçlar ve fikir geliştirirken bu araçlardan nasıl ifade edebiliriz öncelikli olacak.

Hasta verisi bakımı için cBioPortal örneği

(Dikkat ediniz, farklı zaman dilimli veriler oluyor)

cBioPortal örnek tutorial yapıldı

=>100 sample iyi bir veri seçimi olabilir (mümkün oldukça çok olsun)

DNA metilasyon her zaman genetik değişiklikle korrele olmayabilir

RNA-seq verilerini raw veri olduğu için log düzenleme kullanımı

Negatif-pozitif ilişki: Pearson (parametric, gen ifadesi direk önemli) vs. Spearman (non-parametric, sıralayıp, grup içinde kıyaslama) (mesela şu da yardımcı olabilir, https://www.nature.com/articles/nmeth.2937)

Mesela Breast cancer: ER status ilk önemli bulgu

cBioPortal'da veri indirip kendiniz de veriyi analiz edebiliyorsunuz.

BoxPlot, 95%lik dilim ve outliers açıklandı. (detaylı bilgi için boxplot ve quartiles lara bakılabilir, şu da iyi olabilir https://www.nature.com/articles/nmeth.2813)

p-value vs. q-value.

Neden log transformasyona dair makale örneği: Log-transformation and its implications for data analysis (https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4120293/)

Verilerde yeni sorular ile yeni projeler üretmek mümkün. Verilerle yapılacak çok şey var.

Önce bir hipotez belirleme

cBioportal ile bir ön araştırma (explore)

Bir şeylerin ilişkili olduğunu ve değiştiğini buldum

Bir sonraki görüşme için: cBioPortal üzerinden exploration

R Tutorial gönderilecek (başlangıç seviyesi), şu sayfa iyi başlangıç için: https://www.tutorialspoint.com/r/index.htm ve https://www.statmethods.net/management/index.html

Pubmed üzerinden validasyon çalışması, örnek olarak gidebilir.

</details>

---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
Katılımcılar: Ali Osman, Mustafa, Ayşe Gökçe, Neslihan, Fatma Betul

Fatma:
Head&Neck kanserinde (HNSCC) HPV ile ilişkili olduğu genlerin survival tahmin etmede diğer driver olduğu düşünülen genlerle karşılaştırması.

Survivor grafiğini gösterirken yaşam kalite/süresini tahmin edecek genleri tek tek çizmekte fayda var.
Tek tek odd değerlerini göstermek. 
Alternatif survival grafiği çizdirmek için: http://xena.ucsc.edu/

Mustafa:
Primer tümör mutasyonlara bakarak nereye metastaz yapacağını tahmin edebilir miyiz?

Bununla ilgili Neslihan'ın önerdiği makale: https://www.cell.com/cell/fulltext/S0092-8674(22)00003-4?_returnURL=https%3A%2F%2Flinkinghub.elsevier.com%2Fretrieve%2Fpii%2FS0092867422000034%3Fshowall%3Dtrue

Volkan Plot ile ilgili köşe yazım: https://rsgturkey.com/tr/plot-plot-veri-gorsellestirme-volkan-plot/
cBioPortal (daha çok genomik) alternatifi: http://gepia.cancer-pku.cn/ (expresyon üzerinden genelde)

İkinci kısım olarak Ayşe, STRING (protein protein interaction tool) tutorial verdi:
link: https://string-db.org/
Genlerin beraber litaratürde anılıp anılmaması. 

Mesela KRAS ve ilşkili genlerin yüklenip literatürde nasıl bir bağlantısal karşılığı olduğuna bakılabilir.

Strength: Fisher's Exact Test sonucu. 
FDR: False Discovery Rate'i de şimdilik p-value gibi düşünebilirsiniz.
count in network: daha büyük olanlar daha bilgi verici olabilir.
Settings'den mesela KRAS özelinde network çıkarmak mümkün.
Not: Text-mining'i çıkarabiliyoruz bağlantıyı çizerken bazen, her zaman güvenilir bir kaynak değil. Sadece experimental (deneysel) veri üzerinden gitmek isteyebiliyoruz.

Over-representation vs Enrichment Analysis.
Over representation analizi: Temel olarak manual olan listeler var (genler birbiri, pathway ile eşlenmiş). Daha sonra biz kendi gen listemizi verince, bizim birkaç genimiz bu gen içinde var olsun. Daha sonra olasılık hesabı yapıyor. Yani bizim genlerimiz şans eseri mi yoksa gerçekten önemli olarak mı var.

Şimdilik ikinci toplantı ödevi olarak STRING üzerinden hipotezinizde ilişkili gen ailesini STRING üzerinden incelemek diyebiliriz.
  
<details>

---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
---------------------
<details>

<summary>9/4/22 Başlangıç</summary>

### Toplantı 2
  
<details>
