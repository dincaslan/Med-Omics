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
  
</details>

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
* ccle, https://sites.broadinstitute.org/ccle/
* nci-60, https://dtp.cancer.gov/discovery_development/nci-60/
* ucsc-xena, https://xenabrowser.net/

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
  
</details>

---------------------
<details>

<summary>22/5/22 Mustafa ve Ali Osman, kısaca paylaşım</summary>

### Toplantı 4
Katılımcılar: Mustafa, Ali Osman, Ayşe Gökçe, Fatma Betül

Mustafa: EGFR vs. RASA1

Ayşe geridönüt: 
Kanserde survival datası için mutasyon verisi karşılaştırmak istiyorsak, vaka sayısının (number of cases) 100 ve üstü olması, 
ve karşlaştırılan genleri hasta gruplarının benzer büyüklükte olması önemli.
Bunları nerede bulabiliriz? Genom sekanslama ya da mutation profiling datasetlerine bakmak lazım.

Farklı dokuları kıyaslarken de doku specific mi bir farklılık olduğuna bakmak lazım. Primary bir doku vs. normal doku kıyaslama yapılırken farklı doku kıyaslaması direk yapılması tavsiye edilmez.

Kalsiyum bağımlı analiz yapmak çok genel olur. Spesifik downstream yolaklardan gitmek daha mantıklı olabilir.

Co-occurance durumun olabilir mutasyonlarda. Bu durumda tümörün surivalını artırıyor olabilir. 
Survival analizi yaparken overall survival yerine disease-free survival'a bakmak bu açıdan daha faydalı olabilir.
Beraber hareket ettikleri genlerin durumuna da bakılabilir. Hangi yolakta etkili. Bu durumda belki bir "cluster" (grupsallık) mevcut olabilir.

Bir genin inaktive olduğuna bakmak için genelde downstream genine bakılır. Mesela p53 için p21 gibi.

Ali Osman: R'da gene ko-expresyon analizi nasıl yapılır üzerine çalışmış.
WGCNA paketi üzerinden analiz yapmış. 
Link: https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-9-559

PCA alternatifi olarak t-SNE (t-distributed stochastic neighbour embedding): https://www.nature.com/articles/s41467-019-13056-x
Good read on t-SNE: https://www.analyticsvidhya.com/blog/2017/01/t-sne-implementation-r-python/

Ayşe geridönüt:
Spearman'da WGCNA'de uygun.

TCGA'da datasetler daha büyük olduğu için RSEM'in kullandığı distribution-based method daha uygun olduğu için.

TCGA verileri RSEM normalized count data oluyor. RSEM üzerine: https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-12-323

Bu yüzden raw count data isteyen DESeq2 workflowu için uygun değil. 

WGCNA için RSEM normalize edilmiş veri: "The RNA-Seq data input for WGCNA in terms of gene co-expression network construction?"
Biostars'da soru ve cevap: https://www.biostars.org/p/280650/
"Whether one uses RPKM, FPKM, or simply normalized counts doesn't make a whole lot of difference for WGCNA analysis as long as all samples were processed the same way"

High throughput dizilime analizi için normalizasyon teknikleri üzerine: https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-015-0778-7

Bir sonraki toplantı hedefi: RNA-seq dizileme analizi giriş, R'da differensiyel gen ifadesi analizi örnek
  
</details>

---------------------
<details>

<summary>11/6/22 Toplantı </summary>

### Toplantı 5
Katılımcılar: Mustafa, Ali Osman, Ayşe Gökçe, Fatma Betül

Ayşe: RNA-Seq intro tutorial
* Microarray vs. RNA-Seq
* How RNA-seq is done briefly
* Steps of RNA-Seq from RNA isolation to analysis
* Fastq file format
* RNA Seq analysis from quality control to normalization/differential gene expression analysis

Ve bunların ardından
Galaxy ile RNA-seq diferansiyel veri analizi: https://usegalaxy.org/

Ek notlar (fb)
RNA-Seq genel girişi, başta sona: https://chagall.med.cornell.edu/RNASEQcourse/Intro2RNAseq.pdf
Illumina dizilim kısaca: https://www.youtube.com/watch?v=fCd6B5HRaZ8
uzunca: https://www.youtube.com/watch?v=oIJaA6h2bFM
FastQC detaylı açıklama: https://www.bioinformatics.babraham.ac.uk/projects/fastqc/
  
</details>

---------------------
<details>

<summary>25/6/22 MednOmics Genel Bakış </summary>

### Toplantı 6
Katılımcılar: Mustafa, Ali Osman, Ayşe Gökçe, Fatma Betül
  
Bugün genel olarak program nasıl geçti, neleri öğrenmek iyiydi, nereler eksik kaldı (öğrenecek yeni konular) gibi soruları cevapladık.

* cBioPortal
* STRING
* Geo Database/GEO2R
* GALAXY
gibi araçlara aşinalık kazanıp,

* Survival Graphs
* FDR, q value
ve diğer bazı grafik yorumlama ve istatistik analizler konusunda altyapı kazanmanın epey faydalı olduğuna kanaat getirildi.

Ancak, RNA-Seq ve R'da analiz gibi medikal öğrencilerin sıklıkla kullanmadığı teknik ve yöntemleri kullanırken biraz daha katılımcıların aktif olması ve ön araştırma yapması gerektiği sonucuna varıldı.
Bu konuda mentorler olarak teşvik etmek için "Aşinalık kazandıracak soru listesi", "Worksheet" gibi ön ödevlerle öğrencilerin aktif katılımının ve aşinalık aşamasının hızlandırılması önerildi.

Öte yandan, bir hipotez üzerinde tartışma ve ilerlemenin iyileştirilmesi konusunda 2 öneri sunuldu:
1. önceden planlanmış veyahut hazır bir hipotezin adım adım takip edilmesi
2. gruplar oluşturup, katılımcıların kendi hipotezleri ile grup olarak çalışması

Gelecek için de şunlar planlandı:
* İstatistik için ayrı bir ders. Böylece FDR, Enrichment Analysis, parametricve non-parametric testler gibi konular ve ayrımların daha detaylı tartışılması. 
Bunun için şu öne çıktı: 
1. Önce teorik ders (ilk zoom)
2. Sonra R'da uygulamalı bio-istatistik (ikinci zoom)

Bunun haricinde
* Expression Atlas gibi araçların da etkin kulanımının faydasının öne çıkarılması, mesela "hangi gen hangi durumda hangi dokuda farklı davranmış" ve "meta-analizler"de kullanışlı olması gibi bilgilerin gözden kaçması ihtimaline karşı, eski notlara bir geri bakış tavsiye edildi.

* Single-cell RNA seq giriş dersi (Fatma)

* Multi-modal sequencing approaches
  
* Differential co-expression networks/analysis
gibi konuların Jouurnal club gibi 15dklık bir makale tartışmasını takiben method üzerinde yoğunlaşarak anlatılması/çalışılmasına karar kılındı.

* Özellikle medikal öğrencilerin biyoenformatik eğitimi konusunda nerden başlaması ve nasıl ilerlemesi konusunda örnek kaynak listesi oluşturulmasına karar verildi. 
Bu amaçla 3 adımdan bahsedildi:
  
1. RSG Blog'da öncü köşe yazısı (ilk deneyimlerimiz)
  
2. RSG Blog'da serinin devamı yazımız, gelecek deneyimlerimizle.
  
3. Bütün bunların "Bootcamp" olarak bir website ve github kaynak listesinde detaylı olarak toplanıp halka açık kaynak olarak arz edilmesi.
  
</details>

---------------------
<details>

<summary>16/7/22 Köşe Yazısı </summary>

### Toplantı 7
Katılımcılar: Mustafa, Ali Osman, Fatma Betül
  
Med&Omics: Hekimler için Biyoinformatik serimizin ilk yazısı-son düzeltmeler için toplandık.

Üzerinden geçilecek mevzulara değindik.
GEO2R/RNA-Seq gibi araçları yeniden gözden geçirmek gibi.

İki hafta sonra davetlimiz olabilir (buraya ateş emojisi koyduğumu varsayalım).

Alternatif olarak, bir sonraki toplantı için Ensembl-BioMart'a giriş tutorial' planladık.

Return of Ayşe Jedi'den sonrası için de R'da RNA-Seq'i takiben Data-viz ve İstatistik.
  
</details>

---------------------
<details>

<summary>6/8/22 Ensembl</summary>

### Toplantı 8
Katılımcılar: Mustafa, Ali Osman, Fatma Betül
  
Ensembl Biomart giriş tutorial yapıldı (genelist dosyası genleri ile)
https://www.ensembl.org/biomart/martview/d2352fab41407dc6a6855b9c950d4817

BioMart YouTube tutorial: https://asia.ensembl.org/info/genome/stable_ids/index.html
BioMart Guide: https://www.ensembl.org/info/data/biomart/index.html

Ensembl Biomart'ın kapsamlı veri bankaları arası gen/transcript karşılık gelen tek tek farklı özellikleri/karşılığı incelendi (ENSGXXXXXX'in HGNC ID'si, Gene Type'ı, GO description vs.).

Ensembl id version derken ne kastedildiğine bakıldı: https://ensembl.org/info/genome/stable_ids/index.html

Ali Osman alternatif önerdi: https://biit.cs.ut.ee/gprofiler/gost
Veyahut: https://www.genenames.org/
  
</details>

---------------------
<details>

<summary>10/9/22 TCGA Mutasyon Bilgisi</summary>

### Toplantı 9
Katılımcılar: Mustafa, Ali Osman, Fatma Betül

Sorun: 
3 SNP'nin devamında gelen genlerin ifade ve protein miktarını nasıl etkilediğini

TCGA verisetinden germline mutasyon bilgisini nasıl çıkabilirim?

Whole Genome Seq verietleri etik izinler sebebiyle germline mutasyon bilgisine ulaşması zor.
TCGA yerine küçük verisetlerine bakılabilir. Whole exome dizileme verisetleri vs.
NCBI-dbGaP bir alternatif olabilir.


Bütün TCGA verisetinde mutasyonun etkisine bakış
Cell-line verisetlerine bakmak bir diğer alternatif
https://depmap.org/portal/
https://cellmodelpassports.sanger.ac.uk/

https://dcc.icgc.org/pcawg

Bugünden kısa kısa:
Whole exome dizileme, etik izni kolaylığı ve daha ucuz ooması sebebiyle bazı çalışmalarda whole genome göre daha çok tercih edilebiliyor.

Sonrası:Genome dizileme'ye giriş. 
UCSC üzerinden kullanım.

İstatistik istatistik istatistik

</details>

---------------------
<details>

<summary>24/9/22 qPCR Giriş</summary>

### Toplantı 10
Katılımcılar: Mustafa, Ali Osman, Fatma Betül, Ayşe Gökçe

qPCR veri analizi
qPCR veri yorumlaması
Ct vs.Tm* 

*Oligo dizayn ederkenki annealing Tm ile qPCR sonunda melting curve ile ortaya çıkan Tm ile aynı değil. 
Melting curve analizi detaylı bilgi:
- https://sg.idtdna.com/pages/education/decoded/article/interpreting-melt-curves-an-indicator-not-a-diagnosis
- https://www.gene-quantification.de/real-time-pcr-handbook-life-technologies-update-flr.pdf

qPCR çalışma prensibi, dizayn ve replikaları hakkında detaylı bilgi:
- https://www.thermofisher.com/sg/en/home/life-science/pcr/real-time-pcr/real-time-pcr-learning-center/gene-expression-analysis-real-time-pcr-information/precision-qpcr.html
- https://www.thermofisher.com/sg/en/home/life-science/pcr/real-time-pcr/real-time-pcr-learning-center/gene-expression-analysis-real-time-pcr-information/introduction-gene-expression.html
- https://fatmab-dincaslan.medium.com/qpcr-primer-design-tutorial-879311c591aa

qPCR verisi analiz etme üzerine Livak ve ondan doğan referans hakkında detaylı bilgi:
- http://gene-quantification.net/livak-2001.pdf
- https://www.nature.com/articles/nprot.2008.73
- https://academic.oup.com/nar/article/29/9/e45/2384081?login=true (efficiency meselesi hk.)
- https://www.thermofisher.com/sg/en/home/life-science/pcr/real-time-pcr/real-time-pcr-learning-center/real-time-pcr-basics/absolute-vs-relative-quantification-real-time-pcr.html

Graphpad statistics guide: 
- https://www.graphpad.com/guides/prism/latest/statistics/index.htm
  
</details>

---------------------
<details>

<summary>3/12/22 Ali Osman Proje</summary>

### Toplantı 11
Katılımcılar: Ali Osman, Fatma Betül, Ayşe Gökçe

Bundan önce Ali Osman'ın sorusuna binanen Ayşe'nin önerdiği verilen gen seti için TF bulma için tool: https://maayanlab.cloud/chea3/
"Transcription factors (TFs) are proteins that control gene expression by binding and unbinding near coding regions to regulate the transcriptional machinery. TF enrichment analysis (TFEA) prioritizes transcription factors based on the overlap between given lists of differentially expressed genes, and previously annotated TF targets assembled from multiple resources. ChEA3 is a web-based TFEA tool."

Batch effect için Ayşe'nin önerisi: https://support.bioconductor.org/p/100278/
alterntifler combat ve sva

Ali Osman: Limma- "removeBatchEffect" ile önce ve sonrası datayı kıyaslama fırsatı var. Deseq2'da output vermiyor corrected datayı.
 
Ali Osman'ın proje analizi üzerine tartışma ile başlandı.
  
</details>

---------------------
<details>

<summary>19/3/23 RSG Yönetim Ekibiyle Bilgi Alışverişi</summary>

### Toplantı 12
Katılımcılar: Ravza Gür, Kübra Kubat, Ali Osman, Fatma Betül, Ayşe Gökçe

Med&Omics nedir ne değildir tartışıldı.

Ravza: Sempozyuma eklenebilir ve tanıtımı yapılabilir
Farkındalık için ek medikal alanda yan sempozyum
Klinikten gelenler için slack kanalı
Ali Osman: Kısa tanıtım seminer serisi ile ilgili olanları belirlemek
Ali Osman ve Mustafa: Aşina olmak önemli bu grup bu konuda önemli
Ali Osman: JC grupları, benzer konu ilgisi olan max 5-6 kişiden oluşursa daha etkili olabilir
Med&Omics JC için ilgili bireylere açık olması

Bir sonraki toplantı için ne yapılabilir:

* RNA-Seq Analiz tekrar
-R şu sayfa güzel bence ilk eğitim için https://www.tutorialspoint.com/r/index.htm
-DEseq analizi için baştan sona bana çok faydalı kaynak: https://chagall.med.cornell.edu/RNASEQcourse/Intro2RNAseq.pdf
* Command Line Tools/Linux giriş
-Örnek eğitim: https://github.com/rsgturkey/Workshop2021 
-Mac-> Terminal var; Windows-> için Ubuntu LTS indirebilir Microsoft 
* Makale oylamaca, analiz bakmaca
* SNP Analizi
* CNV/Tumor Heterogeneity/Clonality Analizi

Bir sonraki dersin içeriği ve bir sonraki okunacak makale (1-2 ay süre verilerek)
  
</details>

---------------------
<details>

<summary> Stay Tuned </summary>

### Toplantı 13
  
</details>

---------------------


  

