---
title: Rezultate
description: Raport sintetic asupra rezultatelor obținute în etapele de lucru
background: /assets/img/negresti.jpg
permalink: /raport/
---

## Etapa I
## Organizarea și stabilirea fluxurilor de lucru în vederea implementării Infrastructurii de Date Spațiale (SDI)
> Etapa I a urmărit îndeplinirea primului obiectiv al proiectului și anume 
acela de a _stabili cadrul conceptual și metodologic necesar implementării Infrastructurii de Date Spațiale._

##### **Act. 1.1. Organizarea și stabilirea fluxurilor de lucru în vederea implementării Infrastructurii Spațiale de Date (SDI)**

În cadrul acestei activități s-a procedat la proiectarea SDI urmărindu-se aspectele legate de structura și conținutul acesteia, tipurile de date disponibile și procedurile
 de prelucrare și procesare, programele și uneltele care urmează a fi utilizate precum și echipamentele necesare atât pentru implementarea SDI cât și pentru culegerea datelor
 de sol. În acest sens au avut loc o serie de întâlniri de lucru cu membrii echipei în care s-a stabilit că Infrastructura de Date Spațiale trebuie să respecte standardele OGC
 (Open Geospatial Consortium), trebuie să conțină pe cât posibil date cu caracter deschis sau cu politici de acces bine definite, să utilizeze predominant programe și unelte
 Open Source (QGIS, GRASS, SAGA, R, PYTHON) și să ofere posibilitatea utilizării și exploatării de către o categorie cât mai mare de specialiști cu preocupări în domeniul științei
 solului. Din punct de vedere al structurii s-a convenit ca SDI să conțină o componentă destinată stocării și administrării datelor spațiale și a altor tipuri de date necesare,
 o componentă destinată procesării și analizării bazei de date în scopul obținerii de informații noi necesare cartografierii solului și administrării teritoriului și o componentă
 destinată vizualizării și exploatării bazei de date.

##### **Act. 1.2. Evaluarea parametrilor tehnici ai SDI și realizarea paginii WEB a proiectului.**
În cea de-a doua etapă s-au evaluat parametrii tehnici ai SDI respectiv s-au stabilit echipamentele hardware necesare pentru achiziția, procesarea, stocarea și backup-ul datelor
 și informațiilor utilizate precum și programele necesare pentru implementarea acesteia. Urmărind structura SDI s-a stabilit că datele spațiale vor fi stocate într-o baza de date
 găzduită de un server cu ajutorul căruia se va realiza și aplicația de WEB-Mapping din etapa a III-a de implementare a proiectului, iar backup-ul va fi asigurat de o soluție de
 tip NAS separată. Aceasta servește și pentru efectuarea de copii de siguranță periodice ale stațiilor de lucru. Pentru procesarea și analiza datelor spațiale s-a stabilit ca este
 necesară achiziția unei stații de lucru capabilă să efectueze sarcini complexe (interpolări, machine learning) și să poată prelucra date de dimensiuni mari (modele numerice cu
 rezoluție spațială mare, imagini satelitare etc.). Pe lângă aceasta au fost achiziționate si o serie de stații de lucru mobile care să permită cu ușurință prelucrarea datelor de
 dimensiuni reduse sau efectuarea unor sarcini mai puțin solicitante.

Din punctul de vedere al achiziției datelor în teren s-a stabilit ca sunt necesare echipamente destinate fotografiei aeriene (Dronă multispectrală), senzor de culoare cu ajutorul
 căruia se pot calibra fotografiile efectuate asupra profilelor de sol asigurându-se astfel o acuratețe mai mare a culorilor precum și identificarea automată a culorii probei de
 sol conform codului de culori Munsell. Destinată înregistrării temperaturii suprafeței solului precum și echipamente pentru prelevarea probelor de sol.

Realizarea celor două etape ale primului obiectiv al proiectului au dus la elaborarea unui plan de lucru care să faciliteze ulterior realizarea eficientă a celorlalte
 obiective prevăzute în planul de realizare a proiectului.

## Etapa a II-a
## Realizarea bazei de date spațiale și dezvoltarea metodelor, modelelor și uneltelor destinate procesării datelor, interogării bazei de date și a rapoartelor specifice
> Etapa a doua de realizare a proiectului de cercetare cuprinde practic două obiective majore ale proiectului, respectiv _dezvoltarea unei baze de date spațiale
 relaționale_ și a _metodelor, modelelor și uneltelor destinate procesării și analizei datelor precum și a interogării bazei de date_. 
 Aceasta etapă conține opt activități specifice și una suport destinate îndeplinirii celor două obiective.

##### **Act. 2.1. – Dezvoltarea schemei conceptuale a bazei de date relaționale.**

În cadrul acestei activități am definit elementele componente ale tabelelor de atribute ale profilelor de sol reprezentate prin geometrie de tip punct și a unităților de
 sol reprezentate prin poligoane. S-a stabilit ca pentru fiecare tabel să existe un element de legătură astfel încât să fie posibilă relaționarea acestora. 
Atributele specifice profilelor de sol au fost grupate în trei categorii distincte pentru a facilita ulterior interogarea acestora. Astfel o primă grupă de atribute este
 constituită din caracteristicile geografice ale profilului de sol precum coordonatele geografice, forma de relief, vegetația, tipul de scurgere, panta, expoziția, litologia etc.
 Cea de-a doua categorie majoră de atribute ale profilului de sol o constituie orizonturile componente și caracteristicile morfologice ale acestora, respectiv denumirea
 orizontului, culoarea după codul de culori Munsell, textura, structura, porozitatea, trecerea dintre orizonturi, prezența fragmentelor de rocă sau artefacte în orizonturile
 de sol. În final cea de-a treia grupă de elemente se referă la analizele fizico-chimice ale fiecărui orizont în parte (pH, conținutul de carbonați, fracțiunile granulometrice,
 densitatea aparentă, humus, conținutul de N-P-K, conținutul de săruri etc.). Toate aceste elemente sunt grupate în trei tabele distincte relaționate pe baza ID-ului
 profilului de sol. Unitățile de sol, reprezentate sub formă de poligon cuprind pe de-o parte informații legate de tipul de sol, suprafața, perimetru, profil caracteristic (ID)
 și pe de altă parte elemente componente obținute în urma interogărilor specifice fie a stratelor spațiale (DEM, strate climatice, relief, litologie) fie a tabelelor privind
 caracteristicile solului, rezultatele fiind prezentate sub forma de clase conform Metodologiei Elaborarii Studiilor Pedologice și Agrochimice. Introducerea datelor în tabele
 se realizează fie prin digitalizarea fișelor de sol din studiile pedologice fie în teren sau pe baza rezultatelor analizelor de laborator.
În baza de date relațională urmează să fie introdus și un strat spațial reprezentând TEO-urile care va fi creat în urma intersecției dintre US-uri și C clasele de panta și
 expoziție clasificate conform metodologiei.
De asemenea s-au stabilit arealele de lucru pentru care s-au obținut studii pedologice la scara 1:10000 și în care s-au programat deplasări în teren pentru recoltarea de probe
 de sol suplimentare care să vină în completarea studiilor și să permită realizarea unui studiu nou. În alegerea zonelor de studiu ![fig. 1](/assets/img/harta_studii.png)
_Distribuția arealelor de studiu._ s-au avut în vedere o serie de criterii precum specificul utilizării terenului (pomicultură, viticultură, arabil, pășuni), prezența siturilor
 arheologice sau a anumitor elemente particulare (tipuri de sol azonale, zone inundabile sau zone destinate dezvoltării infrastructurii, arii protejate) precum și
 disponibilitatea unor studii pedologice cât mai complete. S-a urmărit astfel introducerea unor informații noi în baza de date care să permită și realizarea de studii
 interdisciplinare precum identificarea zonelor care necesită un anumit regim de protecție, sau identificarea unor elemente restrictive în planurile de dezvoltare.

##### **Act. 2.2. – Selectarea, colectarea și procesarea datelor spațiale Open Source**

Așa cum s-a stabilit în etapa I, pentru extragerea unor parametri suplimentari privind caracteristicile factorilor pedogenetici sau diferite date suport a fost necesară 
descărcarea datelor disponibile din diferite surse de date în regim deschis (tab.1).

| Tipul de date | Format | Acoperire | Rezoluția spațială (m) | Scara | Sursa |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Litologia | WMS raster | națională | | 200000 | <https://geo-spatial.org/> |
| EU-DEM | raster | continentală | 25 | - | <https://land.copernicus.eu/> |
| ALOS PALSAR | raster | globală | 12,5 | - | <https://search.asf.alaska.edu/#/> |
| LIDAR | raster | locală | 1 | - | ABA Prut-Bârlad |
| ROCADA | raster | națională | 11000 | - | ANM |
| ECAD | raster | continentală | 11000 | - | <https://www.ecad.eu/> |
| TerraClimate | raster | globală | 4500 | - | <https://developers.google.com/earth-engine/datasets/catalog> |
| CLC | vector | continentală | - | 200000 | <https://land.copernicus.eu/> |
| Riparian zones | vector | continentală | - | 10000 | <https://land.copernicus.eu/> |
| Urban atlas | vector | continentală | - | 10000 | <https://land.copernicus.eu/> |
| Natura 2000 | vector | continentală | - | 10000 | <https://land.copernicus.eu/> |
| Limite administrative | vector | națională | - | 5000 | <https://inspire-geoportal.ec.europa.eu/> |
| Limite bazine hidrografice | vector | națională | - | 100000 | <https://inspire-geoportal.ec.europa.eu/> |
| Rețea hidrografică | vector | națională | - | 100000 | <https://inspire-geoportal.ec.europa.eu/> |
| Areale protejate | vector | națională | - | 10000 | <https://inspire-geoportal.ec.europa.eu/> |
| Landsat | raster | globală | 30 | - | <https://developers.google.com/earth-engine/datasets/catalog> |
| Sentinel 2 | raster | globală | 10/20 | - | <https://developers.google.com/earth-engine/datasets/catalog> |

În plus, au fost solicitate date spațiale aparținând unor instituții publice pentru completarea SDI și crearea unor strate suport (planuri topo-cadastrale, utilizarea
 terenului după ortoplan, hărți geologice la scara 1:50000). Aceste date sunt utilizate frecvent de către pedologi în procesul de cartografiere a resurselor de sol și au
 fost solicitate doar pentru exemplificarea utilizării acestora în cadrul SDI.
Datele cu acoperire continentală sau globală au fost extrase după limita reprezentând granița Romaniei,sau după limitele unităților administrative de gradul 2 (județe) și apoi
 reproiectate în sistemul de proiecție Pulkovo 1942(58) / Stereo70 (cod EPSG:3844) și în funcție de specificul acestora au fost procesate individual.
Astfel, Harta geologică se prezintă sub formă de serviciu WMS la scara 1:200,000 (<https://geo-spatial.org/>) și poate fi utilizată fie în format original fie poate fi
 digitizată, însă datorită complexității sale acest proces se recomandă a fi aplicat doar pe suprafețe reduse. În plus, pentru anumite areale, am scanat hărțile geologice la
 scara 1:50,000 și le-am georeferențiat pentru a fi utilizate ca suport în cartografierea unităților de sol.
Modelele numerice ale terenului au fost obținute la trei rezoluții spațiale diferite, respectiv la 25m (EUDEM) disponibil pentru întreaga suprafață a României, 12,5m 
(ALOS PALSAR) cu un grad de acoperire mai redus și 1m (LIDAR) cu acoperire la nivel bazinal 
Cele trei modele au utilizare distinctă în cadrul procesului de cartografiere pedologică, însă pentru a putea fi utilizate acestea au trebuit să fie reproiectate în sistemul
 Pulkovo 1942(58) / Stereo70 al României. După reproiectarea și filtrarea modelelor numerice în vederea îndepărtării artefactelor, s-au realizat o serie de teste pentru
 a determina rezoluția optimă și sursa pentru fiecare categorie de parametri morfometrici ce vor constitui caracteristicile terenului in baza de date. Astfel, pentru indicii
 morfometrici generali, exceptând panta și expoziția, și pentru reprezentarea scurgerii apei pe versant rezultatele cele mai bune au fost obținute în cazul rezoluției de 25m
 (EUDEM) datorită numărului redus de artefacte și a unui grad de generalizare suficient. Modelul numeric de la ALOS PALSAR de 12,5m rezoluție a dat cele mai bune rezultate la
 modelarea pantelor, expoziției și a curburilor suprafeței însă nu oferă acoperire integrală pentru teritoriul României și poate fi reeșantionat la 10m rezoluție fără a se pierde
 informația spațială.
Modelul LIDAR a fost obținut pentru o regiune relativ redusă pentru a fi testată utilitatea acestuia în procesul de cartografiere a solurilor. Pentru a putea fi utilizat în
 condiții optime, acesta a fost generalizat la rezoluția de 10m și analizele au indicat că se poate utiliza în special pentru cartografierea alunecărilor de teren, a ravenelor
 dar și pentru identificarea unor forme de relief din zonele joase. La rezoluția de 1m, datorită numeroaselor artefacte și detalii este recomandat a se utiliza pe suprafețe
 reduse în special în areale cu interes arheologic sau pentru conservarea patrimoniului. O atenție deosebită a fost acordată pantelor și expoziției versanților deoarece acești
 doi parametri au impact major asupra delimitării TEO-urilor și asupra calcului notelor de bonitare și una din problemele utilizării acestor parametri sub formă de raster
 este că valorile pixelilor au tendința de a se reduce în special în zonele cu valori mari de pantă. Pentru a diminua efectul de reducere al valorilor de pantă și expoziție,
 obținerea acestor două strate s-a realizat după modelul numeric cu rezoluție de 10m LIDAR, iar pentru zonele în care acesta nu poate fi obținut după ALOS PALSAR.
Parametrii climatici au fost descărcați pentru intervalul cuprins între 1961 – 2013 (ROCADA), 1961 – 2020 (ECAD și TerraClimate) și au fost calculați o serie de indici
 climatici precum media multianuală a temperaturilor, suma precipitațiilor medie multianuală, evapotranspirația potențială, umiditatea solului, viteza vântului la înălțimea
 de 10m, nebulozitatea, durata de strălucire a soarelui ![fig. 2](/assets/img/indicatori.PNG){: width="100%"}_Exemple de indicatori pedologici_ Toți acești parametri vor fi
 utilizați după completarea bazei de date pentru calculul claselor de calitate a solului. Gradul de acoperire a datelor climatice este la nivel național și s-a reușit aducerea
 la o rezoluție spațială de 4 km prin interpolare utilizând regression kriging. Stratele spațiale privind utilizarea terenurilor, rețeaua hidrografică, limitele bazinelor
 hidrografice, limitele administrative și alte fișiere în format vectorial au ca scop crearea stratelor suport pentru procesul de cartografiere permițând delimitarea arealelor
 destinate cartografierii solului, cu regim special sau care prezintă interes deosebit precum ariile protejate sau siturile arheologice. 

Imaginile satelitare LANDSAT și SENTINEL 2 au fost descărcate pentru întreg teritoriul României pentru o perioadă cuprinsă între 1984 – 2019 (LANDSAT) și 2015 – 2020 (SENTINEL)
 sub formă de mozaic multispectral. Imaginile satelitare sunt folosite pentru dezvoltarea modelelor predictive de distribuție spațială a parametrilor de sol. 

##### **Act. 2.3. – Digitizarea și pregătirea datelor pedologice existente în format analog**

Principalele surse de date privind caracteristicile la ora actuală sunt studiile pedologice realizate și deținute de oficiile pedologice. Digitalizarea studiilor pedologice s-a realizat în câteva etape distincte. Astfel în primă fază au fost scanate fișele US și borderoul de analize împreună cu hărțile de sol și alte cartograme specifice (TEO-uri, cartograme ale reliefului) care sunt utilizate pentru validarea extragerii automate a diferiților parametri. 

Din fiecare fișă de sol au fost extrase diferențiat și introduse în baza de date cele trei tabele menționate la Act. 2.1. pentru fiecare profil în parte, în plus fiind introduse și unitatea administrativă și județul din care face parte. Hărțile de sol, după scanare, au fost georeferențiate prin metoda punctelor de corespondență, pentru fiecare hartă fiind create minim 40 de puncte astfel încât eroarea reziduală minimă să fie sub 5m. Punctele de corespondență reprezintă preponderent intersecții de drumuri și alte elemente stabile (cladiri, corpuri de proprietate) astfel încât să se obțină acuratețea maximă. Ca suport pentru georeferențiere s-a utilizat serviciul Google Satellite disponibil în addon-ul QuickMapServices din QGIS.
După georeferențiere, de pe hărțile pedologice au fost extrase două strate spațiale distincte reprezentând profilele de sol sub formă de punct la care s-a înregistrat și ID-ul pentru a fi relaționat ulterior de tabelele de atribute din baza de date și unitățile de sol sub formă de poligon fiind adăugat în tabela de atribute și Nr. US, ca element de legătură pentru relaționările ulterioare. În plus, s-au digitizat și TEO-urile pentru a fi folosite la validarea procesului automat de extragere a acestora.
În urma digitizării studiilor pedologice obținute cu sprijinul OSPA județene au fost obținute o serie de strate spațiale reprezentând distribuția spațială a unităților de sol, localizarea profilelor reprezentative și tabelele cu atributele acestora care ulterior au fost introduse în baza de date. Pe lângă aceste studii a fost necesară introducerea în baza de date a unor tabele auxiliare reprezentând clasele pentru valorile principalilor indicatori de bonitare pentru a fi utilizate în dezvoltarea modelelor și a uneltelor destinate interogării bazei de date. ![fig. 3](/assets/img/digitizare.PNG){: width="75%"}_Reprezentarea procesului de digitizare_

##### **Act. 2.4 – Colectarea și procesarea datelor din teren (profile de sol, imagini aeriene)**

Deplasările în teren, realizate pe parcursul acestei etape, s-au realizat în dublu scop, cel de culegere de date pentru realizarea studiilor pedologice noi și pentru completarea bazei de date cu elemente suplimentare precum imagini aeriene preluate cu ajutorul dronei multispectrale, înregistrarea culorii orizonturilor de sol cu ajutorul senzorului de culoare precum și a temperaturii suprafeței solului. Imaginile aeriene sunt utilizate pentru identificarea unor particularități distincte ale terenului precum eroziunea în suprafață sau prezența sărurilor la suprafața solului. Determinarea culorii solului utilizând senzorul de culoare s-a realizat în scopul de a dezvolta o metodă semiautomată de identificare a acestui parametru cu o precizie ridicată dat fiind faptul că determinarea culorii utilizând catalogul Munsell prezintă un grad ridicat de subiectivism.  

Măsurarea temperaturii solului este utilizată pentru calibrarea indicatorilor LST (land surface temperature) calculați după imaginile satelitare, indicatori folosiți de asemenea pentru dezvoltarea modelelor de distribuție spațială a parametrilor de sol. 

În urma deplasărilor din teren au fost recoltate un număr de 200 de probe ce au fost trimise pentru analize fizico-chimice la un laborator specializat.

##### **Act. 2.5 – Dezvoltarea modelelor și instrumentelor necesare obținerii automate a indicilor derivați și a unor parametri de sol.**

Pentru automatizarea proceselor de prelucrare a datelor spațiale și obținerea de informații noi necesare în procesul de cartografiere a unităților de sol am început în această etapă dezvoltarea de instrumente și modele specifice. Astfel, utilizând limbajul de programare PYTHON au fost create o serie de unelte pentru automatizarea proceselor repetitive precum vectorizarea claselor de pantă și de expoziție în vederea obținerii TEO-urilor.
Cu ajutorul modulului Model Designer implementat în QGIS am început realizarea de modele de procesare pentru extragerea automată a indicatorilor morfometrici ai terenului și Arealelor Climatic Omogene (ACO), strate spațiale de bază în SDI care permit delimitarea US-urilor cu un grad ridicat de acuratețe și sunt utilizate și în calculul claselor de calitate. ![fig. 4](/assets/img/TEOI_morfo.PNG){: width="75%"}_Exemple de modele și indici geomorfometrici_

##### **Act. 2.6 – Dezvoltarea modelelor de distribuție spațială a parametrilor de sol**

Pentru obținerea distribuției spațiale a parametrilor de sol am utilizat baza de date LUCAS (Land Use and Coverage Area frame Survey) pentru teritoriul României și o serie de indicatori obținuți anterior (EU-DEM, panta, indicele topografic de umiditate -TWI, NDVI, LAT, LON). Scopul acestor modele este de a crea un set de strate spațiale care să ilustreze distribuția spațială a principalilor indicatori de bonitare astfel încât modelul de calcul al notelor de bonitare să preia automat aceste informații din baza de date. 
Pentru modelarea distribuției spațiale au fost testate o serie de metode de interpolare precum ordinary kriging (OK), regression-kriging (RK), geographically weighted regression (GWR) și ensemble machine learning (EML). Pentru validarea rezultatelor a fost selectat în mod aleator un set independent de puncte (160 pentru proprietățile chimice și 220 pentru fracțiunile granulormetrice) care nu au fost incluse în procesul de interpolare. Analizând indicatorii statistici calitativi pentru eșantioanele de validare (tab. 2) am observat că cele mai bune rezultate au fost obținute în cazul pH-ului, carbonului organic și a conținutului de carbonați, iar cele mai slabe rezultate au fost obținute în cazul fosforului (P), a potasiului (K) și a argilei. Pentru fiecare parametru în parte a fost identificată și metoda optimă de interpolare pe baza performanței statistice obținute. 

|||**pH** |||||**EC** |||
|-----------|-----------|
|**Method** |**R2** |**ME** |**MAE** |**RMSE** |**Method** |**R2** |**ME** |**MAE** |**RMSE**| 
|**OK** |0.416|0.065|0.748|0.957|OK |0.163|0.392|7.687|11.527|
|**RK** |0.464|0.05|0.736|0.917|RK |0.2|0.442|7.542|11.241|
|**GWR** |0.463|0.015|0.728|0.916|GWR |0.178|-0.251|9.055|13.326|
|**GWR-OK** |0.461|0.033|0.708|0.917|GWR-OK |0.241|-19.916|21.369|24.738|
|**EML** |0.466|0.43|0.79|1.01|EML |0.234|-0.074|7.759|11.106
|||**OC** |||||**CaCO3** |||
|-------|--------|---------|-------|--------|---------|-------|--------|---------|---------|
|**Method** |**R2** |**ME** |**MAE** |**RMSE** |**Method** |**R2** |**ME** |**MAE** |**RMSE**| 
|**OK** |0.354|-2.132|7.631|10.682|OK |0.301|0.354|13.016|21.9|
|**RK** |0.439|-2.003|7.17|9.822|RK |0.337|0.539|12.772|21.366|
|**GWR** |0.29|-3.029|9.121|17.549|GWR |0.338|-0.09|12.993|23.107|
|**GWR-OK** |0.274|-2.703|9.201|17.903|GWR-OK |0.323|0.06|13.034|23.699|
|**EML** |0.358|-0.771|7.276|10.087|EML |0.319|0.5|13.276|21.894|
|||**P** |||||**N** |||
|-------|--------|---------|-------|--------|---------|-------|--------|---------|---------|
|**Method** |**R2** |**ME** |**MAE** |**RMSE** |**Method** |**R2** |**ME** |**MAE** |**RMSE**| 
|**OK** |0.005|-0.527|12.411|19.628|OK |0.239|-0.108|0.678|0.905|
|**RK** |0.043|-0.829|12.465|18.845|RK |0.285|-0.094|0.648|0.874|
|**GWR** |0.007|-2.572|15.78|28.837|GWR |0.238|-0.19|0.745|1.089|
|**GWR-OK** |0.006|-2.299|15.832|29.252|GWR-OK |0.227|-0.189|0.772|1.123|
|**EML** |0.021|-0.509|12.11|19.038|EML |0.245|0.009|0.64|0.873|
|||**K** |||||**Clay** |||
|-------|--------|---------|-------|--------|---------|-------|--------|---------|---------|
|**Method** |**R2** |**ME** |**MAE** |**RMSE** |**Method** |**R2** |**ME** |**MAE** |**RMSE**| 
|**OK** |0.098|-1.904|116.772|207.694|OK |0.108|0.802|15.463|18.779|
|**RK** |0.116|-2.04|114.612|205.588|RK |0.086|0.868|15.472|19.104|
|**GWR** |0.029|-30.67|143.977|255.157|GWR |0.075|0.552|15.594|20.598|
|**GWR-OK** |0.028|-28.458|144.221|256.186|GWR-OK |0.073|0.555|15.702|20.725|
|**EML** |0.15|-0.444|111.143|203.697|EML |0.111|0.821|15.15|18.755|
|||**Silt** |||||**Sand** |||
|-------|--------|---------|-------|--------|---------|-------|--------|---------|---------|
|**Method** |**R2** |**ME** |**MAE** |**RMSE** |**Method** |**R2** |**ME** |**MAE** |**RMSE**| 
|**OK** |0.191|-0.107|12.669|16.974|OK |0.301|-0.779|12.72|16.629|
|**RK** |0.194|-0.119|12.61|16.946|RK |0.319|-0.901|12.431|16.404|
|**GWR** |0.163|-0.376|13.48|18.158|GWR |0.183|-0.246|13.842|18.926|
|**GWR-OK** |0.16|-0.202|13.526|18.26|GWR-OK |0.19|-0.427|13.79|18.922|
|**EML** |0.191|0.014|12.25|16.994|EML |0.332|-0.697|12.296|16.24|

Pe baza acestor rezultate au fost selectate metodele de interpolare optime pentru fiecare parametru pentru fi utilizat și la scară locală la nivel de UAT (unitate administrativ teritorială).

##### **Act. 2.7. și 2.8 – Dezvoltarea barelor de instrumente destinate calculului funcțiilor de pedotransfer și a interogării bazei de date și dezvoltarea de instrumente (add-on) destinată analizei statistice a datelor**

Până în prezent au fost realizate o serie de unelte bazate pe integrarea
 limbajului R în QGIS pentru extragerea statisticilor descriptive, pentru ilustrarea distribuției verticale a parametrilor de sol 
 și a culorii acestuia, pentru analiza distribuției datelor (utilizată și în cazul modelelor predictive) și pentru clasificarea 
 fracțiunilor granulometrice conform SRTS 2012 sub forma diagramelor ternare.
Uneltele realizate pe parcursul acestei etape, constând în modele de geoprocesare
și unelte bazate pe limbajul R au fost agregate în bare de unelte pentru a facilita utilizarea acestora de către pedologi.
Modelele destinate geoprocesării au fost create pentru obținerea rapidă a stratelor spațiale specifice necesare în procesul
 de cartografiere al solurilor cum ar fi, spre exemplu extragerea Teritoriilor Ecologic Omogene (TEO) pe baza intersectiei
 dintre Unitățile de Sol și clasele de pantă și expoziție conform MESP-87 (fig. 2) sau extragerea tipurilor simplificate de relief. 
În plus, pe lângă uneltele menționate anterior, au mai fost elaborate și o serie de funcții cu ajutorul limbajelor 
Python și R destinate în principal pentru codificarea valorilor principalilor indicatori de bonitare conform MESP-87 
dar și pentru calculul unor parametri fizico-chimici pe baza de funcții de pedotransfer.
![fig. 5](/assets/img/unelteR.PNG){: width="75%"}_Exemple de funcții și rezultatele acestora pentru exploatarea bazei de date_


##### **Act. 2.9 – Diseminarea rezultatelor și participarea la manifestări științifice naționale și internaționale**

În etapa a doua, pe baza rezultatelor obținute în cadrul activităților prevăzute în Planul de realizare a proiectului au fost publicate sau sunt în fază de evaluare (major revision)
o serie de lucrări științifice în jurnale ISI și într-un volum al unei manifestări științifice naționale. 

Astfel, utilizând rezultatele din cadrul Act. 2.2. s-a publicat un articol ISI în revista Environmental Research, într-un colectiv extins intitulat Global changes in soil organic carbon and implications
for land degradation neutrality and climate stability [DOI: 10.1016/j.envres.2021.111580](https://doi.org/10.1016/j.envres.2021.111580), care analizează schimbările întervenite la nivel global în distribuția carbonului organic în perioada 2001 – 2015. 

Pe baza activităților 2.3 și 2.4 s-a elaborat un articol cu o tematică multidisciplinară intitulat Multidisciplinary approach to human - environmental interactions at the Roman-Byzantine Ibida fortress (Dobrogea, South-Eastern Romania)
în care este exemplificată utilizarea informațiilor pedologice și în alt context decât cel legat de cartografierea solului, respectiv pentru înțelegerea relațiilor dintre om și pedopeisaj în perioada antică.
Articolul a fist trimis spre publicare în revista ISI Environmental Archaeology (Taylor & Francis Online) și este în faza de re-evaluare după realizarea corecturilor propuse de recenzori. 

Cel de-al treilea articol trimis spre publicare, Spatial modelling of topsoil parameters in Romania using geostatistics and machine learning, la revista PLOS ONE
descrie rezultatele activității 2.6. și este în curs de re-evaluare după realizarea corecturilor propuse de recenzori. 

De asemenea au mai fost publicate două articole in extenso în volumul ”Diferențieri teritoriale ale învelișului de pedologic din Regiunea Nord-Est a României”, dedicat simpozionului Factori și procese pedogenetice din zona temperată,
ediția a XXX-a, desfășurat în perioada 16-19 septembrie 2021 la Iași și Piatra Neamț și publicat la Editura Universității ”Alexandru Ioan Cuza” din Iași: 

    Radu Gabriel Pîrnău, Cristian Valeriu PATRICHE, Bogdan ROȘCA, Dragoș Alexandru MIREA, Vasile DIACONU, Ionuț VASILINIUC, Cristina Oana STAN, Constantin RUSU, Particularități ale solurilor din Depresiunea Ozana-Topolița: implicații pedogenetice ale analizei multi-elementale în context arheologic,  

    Cristian Valeriu PATRICHE, Bogdan ROȘCA, Radu Gabriel PÎRNĂU, Ionuț VASILINIUC, Cartografierea digitală a proprietăților solului în România pe baza datelor LUCAS  

Tot în cadrul aceluiași simpozion am organizat un atelier de lucru (workshop) intitulat ”Model de infrastructură de date spațială Open Source destinată cartografierii caracteristicilor învelișului de sol”, în care am prezentat rezultatele
obținute până în acest moment în cadrul proiectului. În urma prezentării au fost purtate o serie de discuții cu specialiștii din domeniul pedologiei, prezenți la acest simpozion, pentru a identifica și alte necesități în ceea ce privește structura SDI
sau a capabilităților oferite de aceasta. 

## Etapa a III-a 
## Elaborarea metadatelor, a politicilor de acces și dezvoltarea aplicației web-mapping și testarea Infrastructurii de Date Spatiale

##### **Act. 3.1 - Proiectarea formularelor de metadata și generarea semiautomată a acestora.**
Formularele  de  metadata  au  fost  elaborate  conform  specificațiilor  INSPIRE  și  au  fost  elaborate pentru fiecare strat spațial în parte. În acest scop au fost utilizate facilitățile programului QGIS  dar  și  cele  oferite  de  extensia  PgMetadata  realizată  de  **3liz**  (<https://docs.3liz.org/qgis-pgmetadata-plugin/>) care permite atașarea metadatelor direct în baza de date ![fig. 4](/assets/img/formular_metadata.PNG){: width="50%"} Fișa de metadate conține în general informații legate de titlul stratului spațial, o scurtă descriere a acestuia, un istoric al realizării stratului, extinderea spațială și sistemul de coordonate precum și date tematica stratului, identificatori sau restricții de utilizare. Pe lângă aceste informații sunt adăugate și date de contact sau cele legate de persoana care a cules sau editat datele respective. 

##### **Act 3.2 - Dezvoltarea aplicației de webmapping**
În cadrul acestei activități am optat pentru alegerea unei aplicații care să permită colectarea datelor din teren. 
În acest sens am ales utilizarea aplicației destinate dispozitivelor mobile Merginmaps (<https://merginmaps.com/>) care ne-a permis să testăm colectarea datelor din teren și actualizarea bazei de date de la distanță.
Aplicația permite sincronizarea cu proiectul deschis în QGIS și cu configurațiile destinate formularelor de date din proprietățile fișierului. Un avantaj major al acestei aplicații este că adaugă în mod automat valorile coordonatelor geografice și permite introducerea datelor cu ușurință. De asemenea permite introducerea opțiunilor de selectare a valorilor atributelor pe baza unor tabele auxiliare ceea ce simplifică utilizarea în teren a echipamentelor mobile ![fig. 5](/assets/img/app.PNG){: width="90%"} _Configurarea elementelor aparținând formularului și modul în care apar în aplicație_ Aplicația este disponibilă pentru dispozitivele mobile de tip smartphone sau tabletă și poate fi instalată atât pe sisteme de operare Android cât și pe Apple.

##### Act. 3.3, 3.4 și 3.5 - **Integrarea constituenților în infrastructura de date spațiale și testarea funcționalității componentelor acesteia**
Toate datele spațiale realizate în cadrul activităților anterioare, împreună cu baza de date și uneltele suplimentare au fost integrate într-un tot unitar reprezentând Infrastructura de date Spațiale (SDI) având un server dedicat și o soluție de back-up sub forma unui NAS. Au fost create configurațiile necesare conectării unor utilizatori multipli simultan. Odată cu integrarea tuturor componentelor necesare s-a trecut la testarea funcționalității SDI.
După integrarea componentelor în SDI, s-au realizat o serie de teste pentru a verifica funcționalitatea platformei. Astfel în primă fază, s-a testat funcționalitatea aplicației de la Act. 3.3 pentru a actualiza baza de date a profilelor de sol. În acest scop s-au efectuat o serie de deplasări în teren unde au fost introduse o serie de date atât analitice în cazul unor profile existente cât și colectate în cazul unor profile săpate în teren. În cea de-a doua fază, componentele SDI au fost testate prin parcurgerea tuturor etapelor necesare realizării unui studiu pedologic începând cu etapa de teren și finalizând cu cea de birou. Datele spațiale utilizate în cadrul studiului au permis realizarea stratelor reprezentând unitățile de sol și teritoriile ecologic omogene la scara 1:5000 cu un grad de detaliu ridicat. De asemenea extragerea valorilor indicatorilor pentru bonitare s-a realizat cu ușurință datorită bazei de date relaționale, iar legenda hărții solurilor a fost creată automat prin interogări specifice.

##### Act. 3.6 - Diseminarea rezultatelor. Organizarea unuiworshop privind functionalitatile SDI pentrucartografierea solurilor.

În ultima etapă a proiectului, pe baza activităților anterioare, a fost publicat articolul 
**Multidisciplinary approach to human - environmental interactions at the Roman-Byzantine Ibida fortress (Dobrogea, South-Eastern Romania)** în jurnalul ISI Environmental Archaeology [DOI: 10.1080/14614103.2022.2058685](https://doi.org/10.1080/14614103.2022.2058685), 
a fost publicat un articol nou în revista Sustainability (**Climate Warming-Induced Changes in Plant Phenology in the Most Important Agricultural Region of Romania**, [DOI: 10.3390/su14052776](https://doi.org/10.3390/su14052776), 
iar un al treilea articol, intitulat **Modelling and mapping recent forest biomass changes in Romania using complex data and machine learning algorithms**, trimist spre publicare în jurnalul Stochastic Environmental Research and Risk Assessment (Springer), este în faza de reevaluare după realizarea corecturilor sugerate de recenzori, .
Pe lângă lucrările științifice publicate sau în curs de publicare, rezultatele științifice au fost prezentate în cadrul Congresului Mondial de Știința Solului desfășurat la Glasgow, UK, în perioada 31.07.2022 – 05.08.2022 și în cadrul Landscape Archaeology Conference desfășurate la Iași, în perioada 10-15.09.2022. 
De asemenea în cadrul Simpozionului Factori și procese pedogenetice din zona temperată, desfășurat la Covasna (6-9.10.2022) 
a fost organizat workshop-ul intitulat **Metode și modele de analiză și interogare a bazei de date pedologice, componenta de baza a SDI (Spatial Data Infrastructure) destinata cartografiei solului si administrarii teritoriului** unde au fost demonstrate funcționalitățile SDI

##### **Concluzie**
Platforma integrată reprezentată de Infrastructura de Date Spațiale dedicată cartografierii solului la scară mare este adresată în principal specialiștilor din domeniul științei solului dar și cercetătorilor din alte domenii precum și fermierilor sau administratorilor de terenuri agricole. 
Componentele principale ale acestei platforme, se bazează în principal pe unelte, programe și date deschise dar integrează și date cu circulație restrânsă. Astfel , SDI 
conține în principal o baza de date relațională cu informații legate de principalele caracteristici ale solului, date spațiale suplimentare care servesc ca suport
 pentru cartografierea unităților de sol, unelte destinate exploatării datelor spațiale și a bazei de date și echipamente hardware specifice.
![fig. 6](/assets/img/schema.PNG){: width="100%"}
Infrastructura de Date Spațială este adaptată atât lucrului în birou cât și de pe teren utilizând o aplicație capabilă să interacționeze de la distanță,
 în special pentru culegerea de date și informații noi. Această aplicație a fost adaptată cerințelor bazei de date și poate rula de pe echipamente mobile
 de tip smartphone, tabletă sau GPS-uri performante cu sistem de operare Android.
Nu în ultimul rând, SDI este în totalitate Open Source, deci implică costuri minime legate doar de achiziția echipamentului și a resursei umane.
![fig. 7](/assets/img/final.png)


