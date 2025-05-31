## Projenin Amacı

Bu çalışmanın temel amacı, farklı coğrafyalarda bulunan şehirlerin **yol ağı yapılarının nicel metriklerle karşılaştırılması**, **şehir planlaması, ulaşım verimliliği ve yapısal dayanıklılık** açısından değerlendirilmesidir. 

Analiz sonucunda elde edilen veriler, şehirleşme stratejilerinin ve yol ağı planlamalarının daha sağlıklı kurgulanmasına katkı sağlamayı hedeflemektedir.

## İncelenen Şehirler

Bu proje, dört farklı şehirdeki yol ağlarının karşılaştırmalı analizini kapsamaktadır:

- **Elazığ (Türkiye)**
- **İstanbul (Türkiye)**
- **Barcelona (İspanya)**
- **Dubai (BAE)**

## Veri Seçim Kriteri

Tüm yol ağları, **benzer cadde genişliğine sahip alanlar** temel alınarak seçilmiştir. Bu sayede, şehirler arası karşılaştırmaların **adil, tutarlı ve karşılaştırılabilir bir zemin üzerinde** yapılması sağlanmıştır.

## Yol Ağı Modeli

İncelenen tüm ağlar, **yönlü çoklu grafik (MultiDiGraph)** yapısında modellenmiştir. Bu yapı, özellikle **çok yönlü yolları ve çoklu bağlantı noktalarını** gerçekçi biçimde temsil etmeye olanak tanır.


<table>
  <tr>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/istanbul1.png?raw=true" alt="Istanbul" width="400"/><br>
      <b>İstanbul</b>
    </td>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/barcelona1.png?raw=true" alt="Barcelona" width="400"/><br>
      <b>Barcelona</b>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/elazig1.png?raw=true" alt="Elazig" width="400"/><br>
      <b>Elazığ</b>
    </td>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/dubai1.png?raw=true" alt="Dubai" width="400"/><br>
      <b>Dubai</b>
    </td>
  </tr>
</table>





## **Analiz Özet Tablosu**

| Şehir         | Düğüm | Kenar | Derece Entropisi | Closeness Ort. | Betweenness Ort. | Modülerlik | En Yüksek PageRank |
| ------------- | ----- | ----- | ---------------- | -------------- | ---------------- | ---------- | ------------------ |
| **Elazığ**    | 2597  | 7102  | 1.84             | 0.0339         | 0.0109           | 0.91       | 0.0008             |
| **İstanbul**  | 1235  | 2643  | 2.46             | 0.0365         | 0.0173           | 0.89       | 0.0034             |
| **Barcelona** | 1663  | 2922  | 1.95             | 0.0327         | 0.0153           | 0.87       | 0.0026             |
| **Dubai**     | 1135  | 2074  | 1.97             | 0.0348         | 0.0213           | 0.88       | 0.0029             |


## Ağ Yapısı İncelemesi

### 1. **Düğüm ve Kenar Yoğunluğu**

**Elazığ**, en yüksek düğüm (**2597**) ve kenar (**7102**) sayısına sahiptir. Bu durum, kentsel dokunun oldukça ayrıntılı olduğunu ve sokakların sık bağlantılarla örüldüğünü gösterir. Daha organik ve dağınık bir şehir planlamasına işaret edebilir.

**İstanbul**, diğer şehirlerle karşılaştırıldığında daha düşük düğüm sayısına (**1235**) sahip olmasına rağmen, oldukça yüksek **modülerlik** ve **derece entropisi** değerleri ile dikkat çeker. Bu, karmaşık ve bölgesel olarak yoğunlaşmış bir yol ağına işaret etmektedir.

**Barcelona**, **1663** düğüm ve **2922** kenar ile dengeli bir yapıya sahiptir. Yüksek düzeyde planlanmış şehir yapısı, özellikle kare grid sistemine yakın bir yol yapısıyla açıklanabilir.

**Dubai**, **1135** düğüm ve **2074** kenar ile analizdeki en kompakt yol ağına sahiptir. Ancak yüksek **betweenness** ve **closeness** ortalamaları, ağ üzerindeki önemli yolların daha merkezi ve kritik roller oynadığını göstermektedir. Bu da modern planlamaya sahip bir şehir için beklenen bir sonuçtur.



### 2. **Derece Dağılımı Analizi**

Derece dağılımı, bir ağdaki düğümlerin kaç bağlantıya (kenara) sahip olduğunu gösterir. Bu dağılım, şehirlerin yol ağının ne derece düzenli, planlı veya organik bir yapıya sahip olduğunu anlamada kritik rol oynar.


<table>
  <tr>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/istanbul2.png?raw=true" alt="Istanbul" width="400"/><br>
      <b>İstanbul</b>
    </td>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/barcelona2.png?raw=true" alt="Barcelona" width="400"/><br>
      <b>Barcelona</b>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/elazig2.png?raw=true" alt="Elazig" width="400"/><br>
      <b>Elazığ</b>
    </td>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/dubai2.png?raw=true" alt="Dubai" width="400"/><br>
      <b>Dubai</b>
    </td>
  </tr>
</table>

---

####  **Elazığ**

- Düğümlerin **%58.91’i derece 6**’dır — bu çok yüksek bir oran.
- Bu durum, **grid-like** bir yol ağına işaret etmektedir. Yollar çoğunlukla altı farklı yöne bağlantı sunar.
- **Derece entropisi düşük (1.84)**: Ağın oldukça tekrarlı ve düzenli olduğunu gösterir bu durum esneklik konusunda sınırlı olabilmeyi sağlayabilir.

---

####  **İstanbul**

- **Derece dağılımı en çeşitli şehir** olarak öne çıkar:
  - **Derece 3 (%25)**, **derece 4 (%23)** ve **derece 6 (%26)** önemli oranlardadır.
- **En yüksek entropi değeri (2.46)** İstanbul’dadır.
  - Bu da yol ağının oldukça **karmaşık, organik ve düzensiz** bir büyüme gösterdiğini ortaya koyar.
- Bu çeşitlilik, şehrin **tarihi ve plansız büyüme süreçleriyle** açıklanabilir.

---

####  **Barcelona**

- **Derece 3 (%39.1)** ve **derece 4 (%40.2)** en baskın olanlardır.
- Bu dağılım, **planlı şehircilik anlayışının** sonucudur ve Barcelona'nın **kare/dikdörtgen sokak ızgarası** tasarımını yansıtır.
- **Entropi değeri düşük (1.95)**: Ağın yapısı düzenli, öngörülebilir ve homojen.

---

####  **Dubai**

- **Derece 3 (%51)** ve **derece 4 (%23)** ağırlıktadır.
- **Derece 6 (%10.7)** oranında da dikkat çekici şekilde mevcuttur.
- Bu dağılım, **modern, merkez odaklı planlamanın** göstergesidir.
- Büyük arter yollar çevresinde gelişen bağlantılar söz konusudur.
- **Entropi (1.97)** açısından Barcelona’ya benzese de, yol ağının karakteri daha **merkezileşmiş ve hiyerarşik** yapıdadır.


### 3. **Closeness Centrality Analizi**

**Closeness centrality**, bir düğümün diğer tüm düğümlere olan ortalama uzaklığının tersidir. Bu metrik, bir düğümün ağ genelinde ne kadar **"merkezi" ve ulaşılabilir** olduğunu gösterir. Ortalama closeness değeri, ağın genel erişilebilirliğine dair güçlü bir göstergedir.


####  Closeness Centrality İstatistikleri

| İstatistik | **Elazığ** | **İstanbul** | **Barcelona** | **Dubai** |
|------------|------------|--------------|---------------|-----------|
| Minimum    | 0.0218     | 0.0243       | 0.0221        | 0.0220    |
| Maksimum   | 0.0447     | 0.0537       | 0.0459        | 0.0484    |
| Ortalama   | 0.0339     | 0.0365       | 0.0327        | 0.0348    |

---

####  **Değerlendirme**

- **İstanbul**, closeness centrality ortalaması açısından **en yüksek değere** sahiptir (**0.0365**). 
  - Bu, yolların genel olarak birbirine daha yakın olduğunu ve şehir içi ulaşımın daha **merkezi ve erişilebilir** bir yapıya sahip olduğunu gösterir.

- **Dubai**, benzer şekilde yüksek ortalama closeness değeri ile **etkin ve merkezi** bir yol yapısı sunmaktadır. 
  - **Modern ve planlı altyapısı**, bu metriğe olumlu katkı sağlar.

- **Elazığ** ve **Barcelona**, daha **düşük ortalamalara** sahiptir. 
  - Bu durum, bazı bölgelerin merkezden uzak kaldığını ya da yol ağı yapısının daha **geniş alanlara yayıldığını** gösterebilir.

- Özellikle **Barcelona**’da bu durum, planlı olmasına rağmen sokakların **uzun ve düzenli bloklar halinde** dizilmesinden kaynaklanabilir. 
  - Bu da her düğümden diğerine olan mesafeleri hafifçe artırabilir.
 


### 4. **Betweenness Centrality  Analizi**

**Betweenness centrality**, bir düğümün, diğer düğümler arasındaki **en kısa yollar üzerindeki geçiş sayısını** ölçer. Yüksek betweenness değeri, düğümün **kritik bir bağlantı noktası** olduğunu ve ağın genel akışında **önemli rol** oynadığını gösterir.

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/istanbul4.png?raw=true" alt="Istanbul" width="400"/><br>
      <b>İstanbul</b>
    </td>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/barcelona4.png?raw=true" alt="Barcelona" width="400"/><br>
      <b>Barcelona</b>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/elazig4.png?raw=true" alt="Elazig" width="400"/><br>
      <b>Elazığ</b>
    </td>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/dubai4.png?raw=true" alt="Dubai" width="400"/><br>
      <b>Dubai</b>
    </td>
  </tr>
</table>

#### Betweenness Centrality İstatistikleri

| İstatistik | **Elazığ** | **İstanbul** | **Barcelona** | **Dubai** |
|------------|------------|--------------|---------------|-----------|
| Ortalama   | 0.0109     | 0.0173       | 0.0153        | 0.0213    |
| Maksimum   | 0.1413     | 0.1690       | 0.1200        | 0.1523    |

---

####  **Değerlendirme**

- **Dubai**, **ortalama betweenness** açısından **en yüksek değere** sahiptir (**0.0213**).
  - Bu, ağın belirli noktalarında **yüksek yoğunluklu geçişlerin** gerçekleştiğini ve **ana arter yolların açıkça tanımlı** olduğunu göstermektedir.
  - **Modern planlamaya** sahip şehir yapısı, bu tür merkezi yolların oluşumunu destekler.

- **İstanbul**, **maksimum betweenness** değeri açısından liderdir (**0.1690**).
  - Bu, bazı düğümlerin **yoğun trafik yükü altında** olduğunu ve **boğaz etkisi** yaratabilecek **kritik kavşakların** bulunduğunu gösterir.

- **Barcelona**, ortalama değerde İstanbul’a yakın olsa da maksimum değer açısından biraz daha **dengelidir**.
  - Bu da **trafik yükünün, kısmen daha homojen** dağıldığını gösterebilir.

- **Elazığ**, hem **ortalama (0.0109)** hem de **maksimum (0.1413)** değeriyle **en düşük betweenness** seviyesine sahiptir.
  - Bu durum, ağın daha **homojen**, **yerel geçişlerin yaygın** ve belirli bir **merkezi yoğunluk noktası** bulunmadığını ortaya koyar.
 


### 5. **Modülerlik (Topluluk Yapısı) Analizi**

**Modülerlik**, bir ağın ne kadar iyi şekilde alt gruplara (**topluluklara**) ayrıldığını ölçer.  
Yüksek modülerlik değeri, ağın daha fazla **içsel bağlantıya sahip parçalara** bölünebildiğini;  
düşük modülerlik ise daha **bütünleşik, bağlantılı** bir yapı sergilediğini gösterir.

####  Modülerlik Değerleri

| **Şehir**     | **Modülerlik Değeri** |
|---------------|------------------------|
| **Elazığ**    | 0.91                   |
| **İstanbul**  | 0.89                   |
| **Dubai**     | 0.88                   |
| **Barcelona** | 0.87                   |

---

####  **Değerlendirme**

- **Elazığ**, **0.91** değeriyle **en yüksek modülerlik oranına** sahiptir.  
  - Bu, ağın belirgin şekilde farklı **alt bölgeler (örneğin mahalleler)** olarak gruplaştığını ve bu bölgelerin **kendi içlerinde yoğun bağlantıya**, dışa karşı ise **sınırlı geçişe** sahip olduğunu gösterir.  
  - Yani **komşuluk bazlı yoğunluk** oldukça fazladır.

- **İstanbul** ve **Dubai**, yüksek ama daha **orta seviyelerde modülerlik** sunar.  
  - Bu durum, hem **yerel topluluk yapısının korunduğunu** hem de **genel entegrasyonun sağlandığını** işaret eder.  
  - **Karma şehir planlaması** olan bu iki şehirde modülerlik **dengeli** durumdadır.

- **Barcelona**, **0.87** ile **en düşük modülerlik değerine** sahiptir.  
  - Bu durum, şehrin yol ağının daha **bütünleşik ve entegre** bir yapıda olduğunu, **bölgesel ayrışmaların zayıf** olduğunu gösterir.  
  - Yani, şehir genelinde daha **tutarlı ve yaygın bağlantılar** kurulmuştur.
 





### 6. **Entropi (Yapısal Karmaşıklık)**

**Entropi**, bir ağın **yapısal düzensizliğini ve çeşitliliğini** ölçen bir metriktir.  
Derece dağılımındaki çeşitlilik arttıkça entropi değeri de artar.  
Bu da, ağın daha **karmaşık ve öngörülemez** olduğunu gösterir.



<table>
  <tr>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/istanbul3.png?raw=true" alt="Istanbul" width="400"/><br>
      <b>İstanbul</b>
    </td>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/barcelona3.png?raw=true" alt="Barcelona" width="400"/><br>
      <b>Barcelona</b>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/elazig3.png?raw=true" alt="Elazig" width="400"/><br>
      <b>Elazığ</b>
    </td>
    <td align="center">
      <img src="https://github.com/abdullah-tanriverdi/UrbanRoadNetworkAnalysis/blob/master/ss/dubai3.png?raw=true" alt="Dubai" width="400"/><br>
      <b>Dubai</b>
    </td>
  </tr>
</table>


####  Entropi Değerleri

| **Şehir**     | **Entropi** |
|---------------|-------------|
| **Elazığ**    | 1.84        |
| **İstanbul**  | 2.46        |
| **Barcelona** | 1.95        |
| **Dubai**     | 1.97        |

---

####  **Değerlendirme**

- **İstanbul**, entropi değeri açısından açık ara **en yüksek yapıya** sahiptir (**2.46**).  
  - Bu durum, şehirdeki yol ağının **organik, düzensiz ve çok yönlü** bir yapıya sahip olduğunu gösterir.  
  - Farklı **yol tipleri, sokak düzenleri ve kavşaklar** iç içe geçmiştir.

- **Dubai** ve **Barcelona**, **orta seviyede entropiye** sahiptir.  
  - Bu iki şehirde de belirli bir düzen hissedilmekle birlikte, özellikle **merkezi bölgelerde karmaşık yapılar** mevcuttur.  
  - Bu da hem **modern planlama** hem de **esneklik** anlamına gelir.

- **Elazığ**, **en düşük entropi (1.84)** ile en **düzenli ve tekrar eden yol yapısına** sahip şehir olarak öne çıkmaktadır.  
  - Bu yapı genellikle **grid-like** şehirleşmenin göstergesidir.
 

## Genel Değerlendirme ve Detaylı Analiz

### Dubai
Dubai’nin yol ağı yapısı; yüksek modülerlik ve yüksek betweenness centrality (aracılık merkeziyeti) değerleriyle öne çıkar.  
Bu metrikler, şehrin planlı ve hiyerarşik bir ulaşım sistemine sahip olduğunu göstermektedir.  
Özellikle ana arter yolların belirginliği, ulaşımın merkezî noktalara odaklandığını ve bu düğümlerin kritik öneme sahip olduğunu ortaya koyar.

Ancak, yüksek aracılık merkeziyeti değerleri, bazı yolların aşırı trafik yüküne maruz kalma riskini artırabilir.  
Bu tür yapılar, trafik tıkanıklığına karşı hassas olmakla birlikte, Dubai gibi yeni ve genişleyebilen şehirlerde bu durum genellikle iyi altyapı yönetimi ve kapasite artırımıyla dengelenebilir.

Derece dağılımının dengeli oluşu, şehirde planlı kentsel gelişimin bir yansımasıdır ve ulaşımın istikrarlı şekilde örgütlendiğini gösterir.

---

### Barcelona
Barcelona, düşük modülerlik değerine rağmen denge ve bütünleşik ulaşım açısından güçlü bir performans sergilemektedir.  
Yol ağının düşük modülerliği, şehir genelinde sınırları net olmayan alt bölgeler ve daha bütünleşik bir kent dokusu anlamına gelir.

Derece dağılımı homojen olup, bu durum şehirde yolların birbirine dengeli biçimde bağlandığını ve alternatif güzergâhların mümkün olduğunu ortaya koymaktadır.

Bu yapı, trafik akışının çeşitli yollara yayılabilmesi açısından avantaj sağlarken, aynı zamanda lokal trafik sıkışıklıklarının diğer bölgelere kolayca yansımasına da neden olabilir.

Barcelona’nın ağ yapısı, planlı kentsel gelişimi ve etkin ulaşım tasarımını yansıtan bir örnek teşkil etmektedir.

---

### Elazığ
Elazığ’ın yol ağı, yüksek modülerlik ve düşük aracılık merkeziyeti ile yerel merkezlere dayalı ve dağıtık bir ulaşım sistemini temsil etmektedir.

Ağ üzerindeki düğümlerin büyük bölümünün derece 6 olması, ızgara tipine yakın ve düzenli bir yol şebekesi sunar.  
Bu yapı, hem planlamada kolaylık, hem de ulaşımda esneklik sağlar.

Düşük betweenness değerleri, Elazığ’da ağın genelinde trafik yükünün homojen dağıldığını, belirli düğümlerde aşırı yoğunlaşmaların olmadığını göstermektedir.

Bu durum, trafik dayanıklılığı açısından olumlu olsa da, merkezîlik düzeyinin düşüklüğü, ulaşım optimizasyonunda sınırlı seçenekler sunabilir.

---

### İstanbul
İstanbul, analiz edilen şehirler arasında en yüksek entropi, en yüksek closeness centrality ve en yüksek betweenness centrality ortalamalarına sahiptir.

Bu veriler, şehrin çok merkezli, yoğun ve organik büyüyen bir yol ağına sahip olduğunu gösterir.  
Yüksek yapısal karmaşıklık, İstanbul’un heterojen ve düzensiz sokak dokusunu ortaya koyar.

Bu yapı, şehre dinamik ulaşım seçenekleri sunarken, aynı zamanda bazı kavşak ve bağlantıların kritik yük taşıyıcıları haline gelmesine neden olur.

Betweenness değerlerinin yüksekliği, bazı yolların trafik açısından boğaz noktaları haline gelerek sıkışıklıklara neden olabileceğini işaret eder.

Bu nedenle, trafik yönetimi, altyapı geliştirme ve yoğunluk analizleri, İstanbul gibi karmaşık yapılara sahip şehirlerde öncelikli olmalıdır.



| Kriter / Şehir                    | Dubai                                        | Barcelona                                      | Elazığ                                     | İstanbul                                    |
|----------------------------------|----------------------------------------------|-----------------------------------------------|--------------------------------------------|---------------------------------------------|
| **Modülerlik**                   | Yüksek (planlı, hiyerarşik, ana arterler belirgin) | Düşük (daha bütünleşik, sınırları net olmayan bölgeler) | En yüksek (belirgin mahalle/topluluk kümelenmeleri) | Orta-yüksek (karmaşık, çok merkezli yapı)   |
| **Betweenness Centrality (Ortalama)** | En yüksek (ana arterler ve kritik kavşaklar mevcut) | Orta (dengeli performans)                      | En düşük (ağ homojen, merkezî düğüm yok)   | Yüksek (bazı kavşaklarda aşırı trafik riski) |
| **Derece Dağılımı**              | Dengeli; derece 3, 4 ve 6 yaygın              | Homojen; dereceler 3 ve 4 baskın               | Baskın derece 6; ızgara tipi yapı          | Çok çeşitli; dereceler 3, 4, 6 yüksek         |
| **Entropi (Yapısal Karmaşıklık)** | Orta (düzenli, modern planlama)                | Düşük-orta (planlı ve düzenli)                 | En düşük (tekrarlı, düzenli yol yapısı)    | En yüksek (düzensiz, organik büyüme)          |
| **Closeness Centrality (Ortalama)** | Orta (yollar iyi bağlantılı)                   | Düşük (küresel erişilebilirlik daha az)       | Düşük (küresel erişilebilirlik daha az)   | En yüksek (yollar birbirine daha kısa mesafede) |
| **Trafik Yükü Dağılımı**         | Kritik arterler yoğun trafik riski taşıyor    | Alternatif yollar sayesinde dengeli            | Trafik daha dağıtık, tıkanma noktası az    | Bazı düğümler aşırı yük altında, tıkanıklık riski |
| **Yol Ağı Tipi**                 | Planlı, hiyerarşik, ana arterlere dayalı      | Planlı, bütünleşik, alternatiflere açık        | Izgara tipi, dağıtık ve esnek               | Karmaşık, çok merkezli, organik büyüme        |
| **Öne Çıkan Özellik**            | Kritik merkezlerde yoğunluk; iyi altyapı yönetimi | Bütünleşik şehir dokusu; lokal trafik yayılımı | Esnek, dayanıklı yol ağı; belirgin yerel kümelenme | Dinamik, çok merkezli; altyapı ve trafik yönetimi öncelikli |




# Uzun Vadeli Şehirleşme Planları İçin Öneriler

### 1. Modüler Yapıyı Sağlama
Elazığ gibi yüksek modülerlik değerine sahip şehirlerde, mahalle veya bölge bazlı kümelenmiş yol yapısını desteklenmesi lazım.  
Bu, yerel ulaşımı kolaylaştırır ve trafik yükünü dengeler. Ancak, bölgeler arası güçlü ana arterlerle şehirler arası bağlantıyı zayıflatmamak şartıyla.

### 2. Alternatif Bağlantılar Tasarlama
İstanbul örneğinde olduğu gibi karmaşık ve çok merkezli şehirlerde, kritik kavşakların yükünü azaltmak için birden fazla alternatif yol bağlantılar oluşturulması lazım.
Bu, trafik tıkanıklıklarının önüne geçer.

### 3. Düzenli ve Entegre Yol Ağı Kurma
Barcelona ve Dubai’de görülen dengeli derece dağılımı ve entegre yol yapısını örnek alınması lazım. 
Böylece şehir içi dolaşımı kolaylaştırabilir, merkezi yolların aşırı yüklenmesini önlenebilinir.

### 4. Ana Arter Kapasitesini Artırma
Dubai’nin yüksek aracılık betweenness değerine dikkat ederek, ana arterlerin kapasitesini artırılmalı ve mutlaka alternatif güzergahlar oluşturmalı.  
Bu, trafik yönetimini iyileştirir.

### 5. Erişilebilirliği Yükseltme
İstanbul’un yüksek closeness  değerini hedeflenmeli.  
Şehir içindeki tüm bölgelerin birbirine kolayca ulaşabilmesi için yollar arasındaki mesafeleri kısaltılmalı ve yol düğümlerini dengeli dağıtılmalı.

### 6. Esnek ve Dayanıklı Ağlar Oluşturma
Modülerlik, merkeziyet ve erişilebilirlik kriterlerini dengede tutarak, hem lokal hem de genel ulaşımda esnek ve dayanıklı bir yol altyapısı tasarlanmalı.

### 7. Kritik Noktaları İzleyin ve Güncelleyin
Tıkanıklık riski olan kritik kavşaklar ve ana arterler için öncelikli iyileştirmeler yapılmalı  
Alternatif rotalar planlayarak ve altyapıyı düzenli izleyip güncelleyerek sürdürülebilir bir sistem kurulmalı.








