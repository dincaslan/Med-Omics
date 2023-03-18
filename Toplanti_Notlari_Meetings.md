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

<summary>23/4/22 23 Nisan, neşeyle doluyor insan? </summary>

### Toplantı 3
Katılımcılar: Mustafa, Ali Osman, Ayşe Gökçe, Fatma Betül
  
STRING ödevi üzerinden hipoteze bakış.

Mustafa: EGFR-Ras?
STRING'de XXX ile ilşkili XXX hastalarındaki genin ilşkisel proteinleri tespit edip; cBioportal'da mutasyon için survival (ölüm kalım) 
testi ile yaşamsal önemini tespit etmek (tanı/tedavi için önemli olabilir).

Ayşe geri-dönüt: Ölüm kalım analizlerinde sample size (veri-seti büyüklüğü önemli).
İfade analizi başlangıç için faydalı olabilir. Bu durumda, bazı ilişkisel genler için GEO'dan ön analiz. (Kendi minik analiz aracı var GEO'nun da).
Diğer downstream genlerle ilşkisine bakmak da geniş bir açı verebilir. Diğer bağlanan genlere ki bu ilişki XXX ile YYY arasında özel mi değil mi (specific or not).

Ali Osman: TTTT-RRRR ilşkisi (KKKK bağı üzerinden)
Arkaplan: XXX(TTTT)'in negatif prognostif belirteç olarak bazı kanserlerde kullanılıyor olması.
Bu yolağı çalışmak açısından fare modelinin var olması.
Modifikasyonun squamous cell carcinoma (SCC) vs. adenocarcinoma (AC) üzerinde etki farkı.

RRR-TTTT ilişkisi üzerinden Rho Family ve DOCK family üzerinden STRING ilişki ağının araştırılması.

KRAS mutasyonu ile yakından ilişkili üç kanser tipinde bu genlerin araştırılması.

Ali Osman'ın makale ve video önerisi:
https://pubmed.ncbi.nlm.nih.gov/30664679/
https://www.youtube.com/watch?v=lcfrqe3gvr4&t=2751s

Ayşe geri-dönüt: Birbirine bağlanıyorlarsa, direk ilişkili olmaları normal. Ancak, negatif-pozitif korelasyon, aileler içindeki genleri işlevlerini tanımlamak açısından faydalı olabilir. Kısacası bir bütün olarak çalışmak.
Metastaz verisi yoksa, metastazı işaret eden EMT marker (belirteç) bakılabilir.
cBioportal'daki XXX(RAC1) geni negatif ve pozitif ilşkili genleri ayrı ayrı alıp, STRING'e koyup aralarında EMT işareti gösteren bir ilişki var mı yok mu ayrıca bakılabilir.
Sağlıklı dokular üzerinden, doku özelinde gen ifade verisi: gtex, https://gtexportal.org/home/
Normal ve. kanser:
ccle, https://sites.broadinstitute.org/ccle/
nci-60, https://dtp.cancer.gov/discovery_development/nci-60/
ucsc-xena, https://xenabrowser.net/

Ayşe, XenaBrowser demo gösterimi.

Ayşe, GEO Datasets üzerinden veria analiz demo gösterim.

GEO, https://www.ncbi.nlm.nih.gov/geo/
Örnek veriseti: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE190731

Search gene diyince NCBI'da, burada ilki datasetler ikincii örnekler için. İlkini seç.
GEO Datasets'i soldan seçimi daha özelleştirip daralatabilirsiniz.
GSE numarası önemli, verisetlerin kimlik numarası (ID).

Bazen işlem yapılmamış, raw veriyi bulmak mümkün.
Series matrix file, normalize edilmiş veriler genelde.
logFC: log cinsinden fold change (değişim) değeri. +, artış;-, azalış (kontrole göre).
x-axis'e bakmak lazım. Bazı genlerin zaten ifade değeri çok düşük, o yüzden ufak değişimler bile yüksek logFC ile sonuçlanabilir ancak ifade ettiği anlam yeterli olmayabilir.

Expression Atlas, https://www.ebi.ac.uk/gxa/home
Doku özel, ifade değerine bakmak için faydalı olabilir
Firebrowse da işe yarayabilir, http://firebrowse.org/viewGene.html
  
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
