# 3. Safe Exam Browser-en Konfigurazioa

## 3.1. SEB-ren konfigurazioaren sarrera

SEB `.seb` fitxategi enkriptatuekin konfiguratzen da, azterketetan duen portaera kontrolatzeko. Garrantzitsua da konfigurazio-tresna ofiziala erabiltzea (`SebWindowsConfig.exe` Windows-en) fitxategi hauek sortzeko.

!!! warning "Garrantzitsua"
    Ezarri beti administratzaile-pasahitza zure konfigurazioetan, aldaketa ez-baimenduak saihesteko.

## 3.2. Konfigurazio-urratsez urrats gida

### 1. Urratsa: Ireki Konfigurazio-tresna

#### Windows-en:
1. Bilatu "SEB Config Tool" abioan.
2. Edo exekutatu zuzenean `SebWindowsConfig.exe` instalazio-karpetatik (normalean `C:\Program Files\SafeExamBrowser\`).

### 2. Urratsa: Oinarrizko Konfigurazioa (Orokorra fitxa)

1. **Hasierako URLa**:
   - Sartu azterketaren URLa (adib: `https://zure-lms.eus/azterketa1`).
   - Ziurtatu `https://` erabiltzen duzula konexio seguruetarako.

2. **Administratzaile-pasahitza**:
   - Ezarri pasahitz indartsu bat (gutxienez 8 karaktere, maiuskulak, minuskulak, zenbakiak eta ikurrak).
   - Pasahitz hau beharko da konfigurazioa aldatzeko.

3. **Baimendu SEB-tik irtetea**:
   - **Gomendatua**: Desgaitu aukera hau ikasleek nabigagailua ixtea eragozteko.
   - Gaituz gero, ezarri "Irteteko pasahitza" administratzailearen pasahitzaren desberdina.

4. **Azterketa-modua**:
   - Aukeratu "Erabili SEB konfigurazio-fitxategia azterketa bat hasteko".
   - Honek azterketa bakoitzerako konfigurazio espezifikoak ahalbidetzen ditu.

### 3. Urratsa: Erabiltzaile-interfazearen konfigurazioa

1. **Pantaila osoko modua**:
   - Gaitu lanerako eremua maximizatzeko eta distrazioak minimizatzeko.
   
2. **Abarra**:
   - Desgaitu sarbide ez-baimenduak saihesteko.
   
3. **Orrialdearen birkarga**:
   - Konfiguratu beharrezkoa bada:
     - "Baimendu abisua" itxiera ustekabekoak saihesteko.
     - Edo desgaitu segurtasun handiagorako.

### 4. Urratsa: Nabigatzailearen konfigurazioa

1. **Nabigazio-blokeoa**:
   - Gaitu "Blokeatu esteka leiho berrietara".
   - Desgaitu atzera/aurrera nabigazioa.
   
2. **Bistaratze-aukerak**:
   - Ezkutatu helbide-barra.
   - Desgaitu ortografia-egiaztatzailea beharrezkoa ez bada.

### 5. Urratsa: Aplikazioen kontrola

1. **Prozesuen monitorizazioa**:
   - Gaitu "Monitorizatu Prozesuak".
   
2. **Baimendutako aplikazioak**:
   - Gehitu baimendutako aplikazioak (adib: Windows kalkulagailua).
   
3. **Blokeatutako aplikazioak**:
   - Gehitu nabigatailuak (Chrome, Firefox, Edge).
   - Sartu mezularitza edo pantaila-argazki aplikazioak.

### 6. Urratsa: Sarearen konfigurazioa

1. **URL iragazkia**:
   - Gaitu "URL iragazkia".
   - Konfiguratu arauak:
     ```
     block:*
     allow:zure-lms.eus/*
     ```
   - Doitu domeinuak zure azterketa-plataformaren arabera.

### 7. Urratsa: Segurtasun-egitura aurreratua

1. **Kiosko modua**:
   - Aukeratu "Sortu Mahaigain Berria".
   - Bakandu azterketa-saioa erabat.
   
2. **Pantaila-argazkien aurkako babesa**:
   - Desgaitu pantaila-argazkiak ateratzeko aukera.
   
3. **Sarbideen blokeoa**:
   - Desgaitu Windows eguneraketak automatikoki.
   - Blokeatu birtualizazio-makinak.

### 8. Urratsa: Teklen blokeoa

1. **Blokeatu beharreko teklak**:
   - Alt+Tab
   - Ctrl+Alt+Del
   - Impr Pant / Pantaila
   - Windows tekla
   - Eskuin-klika

2. **Laster-teklen pertsonalizazioa**:
   - Desgaitu edo berresleitu tekla-konbinazioak beharren arabera.

### 9. Urratsa: LMS-rako konfigurazioa

1. **Nabigatzailearen Azterketa Gakoa**:
   - Sortu gako bakarra azterketarako.
   - Kopiatu zure LMS-n (Moodle, etab.) azterketa konfiguratzean.
   
2. **Konfigurazioaren egiaztapena**:
   - SEB-ek gako hau egiaztatuko du azterketa hastean.
   - Ziurtatu ikasleek konfigurazio zuzena erabiltzen dutela.

## 3.3. Gorde Konfigurazioa

1. **Gorde Txantiloi gisa**:
   - Erabilgarri etorkizuneko azterketetarako.
   - Erabili `.seb` luzapena.
   
2. **Babestu pasahitzarekin**:
   - Ziurtatu fitxategia enkriptatuta dagoela.
   - Egiaztatu pasahitza eskatzen duela irekitzean.

3. **Balioztatze-probak**:
   - Probatu fitxategia probetako ordenagailu batean.
   - Egiaztatu murrizketak guztiak.

## 3.4. Banatu Konfigurazio-fitxategia

1. **Banaketa-metodoak**:
   - Igo fitxategia zure hezkuntza-plataformara.
   - Edo bidali posta elektronikoz ikasleei.
   
2. **Argibideak ikasleentzat**:
   - Azaldu nola ireki fitxategia SEB-ekin.
   - Eskaini laguntza teknikoa beharrezkoa bada.

## 3.5. Arazo Ohikoenak

### Abioaren arazoak
- **SEB ez da abiatzen**:
  - Egiaztatu `.seb` fitxategia ez dagoela hondatuta.
  - Egiaztatu sistemaren baimenak.
  
- **Pasahitz-errorea**:
  - Ziurtatu pasahitz zuzena erabiltzen ari zarela.
  - Egiaztatu maiuskulak eta ikur bereziak.

### Konexio-arazoak
- **URLa ez da kargatzen**:
  - Egiaztatu Internet konexioa.
  - Egiaztatu URLa zuzen idatzi duzula.
  - Ziurtatu domeinua baimendutakoen zerrendan dagoela.

### Errendimendu-arazoak
- **Geldoa**:
  - Itxi beste aplikazioak.
  - Egiaztatu sistemaren baldintzak.

## 3.6. Konfigurazio Seguruaren Aholkuak

### Hobespenak
1. **Pasahitz sendoak**:
   - Erabili letrak, zenbakiak eta ikurrak.
   - Ez partekatu pasahitzak posta elektronikoz.

2. **Aurreko probak**:
   - Egin probak aurretik.
   - Egiaztatu murrizketak guztiak.

3. **Segurtasun-kopia**:
   - Gorde konfigurazioaren kopia bat.
   - Dokumentatu egin dituzun aldaketak.

### Segurtasun gehigarria
- **Eguneraketak**:
  - Mantendu SEB eguneratuta.
  - Egiaztatu segurtasun-eguneratzeak.
  
- **Monitorizazioa**:
  - Gainbegiratu jarduera azterketetan.
  - Erregistratu gorabeherak etorkizunerako hobekuntzak egiteko.

## 3.7. Baliabide Gehigarriak

### Esteka erabilgarriak
- [SEB-ren Dokumentazio Ofiziala](https://safeexambrowser.org/)
- [Windows-erako Konfigurazio Gida](https://safeexambrowser.org/windows/win_usermanual_en.html)
- [Laguntza Foroa](https://safeexambrowser.org/forum/)

### Laguntza Teknikoa
- Jarri harremanetan zure erakundeko arreta-teknikoarekin.
- Eman arazoaren xehetasunak konponbide azkarrago baterako.

---

Hurrengo kapituluan, ikusiko dugu nola integratu SEB Moodle, Blackboard eta Canvas bezalako ikaskuntza-plataformekin, eta nola kudeatu lineako azterketak modu eraginkorrean.
