# Moodle-rekin integrazioa

## Moodle-n SEB konfigurazioa

### 🎥 Moodle-rekin integrazioaren bideo-tutoriala

Hasi aurretik, gomendatzen dugu SEB Moodle-rekin integratzeko prozesu osoa erakusten duen bideo-tutorial hau ikustea:

[![SEB Moodle-rekin integratzeko tutoriala](https://img.youtube.com/vi/clRh0efdSJo/0.jpg)](https://www.youtube.com/watch?v=clRh0efdSJo)

### 📋 Aurretiko baldintzak
- Moodle 3.5 edo berriagoa instalatuta
- Moodle gunean administratzaile baimenak
- Ikasleen ordenagailuetan SEB nabigatzailea instalatuta
- "Galdetegia" jarduera aktibatuta Moodle-n

## 🔧 Moodle-n konfigurazioa

### 1. Gaitu SEB galdetegian

1. **Sortu/Editatu galdetegia**:
    - Joan azterketa gehitu nahi duzun ikastaroaren atalera
    - Egin klik "Gehitu jarduera edo baliabidea" botoian
    - Aukeratu "Galdetegia" eta egin klik "Gehitu" botoian

2. **Konfiguratu SEB**:
    - Galdetegiaren konfigurazio orrian, joan **Safe Exam Browser** atalera
    - Aukeratu **"Bai"** **"Behartu Safe Exam Browser erabiltzera"** aukeran
    - Aukeratu konfigurazio mota:
      - **Nabigatzailearen konfigurazioa**: Erabili Moodle-ren oinarrizko aukerak
      - **SEB konfigurazio fitxategia**: Kargatu konfigurazio pertsonalizatutako fitxategi bat

### 2. Gomendatutako konfigurazio aukerak

#### 🔒 Segurtasun oinarrizko aukerak
 - **Blokeatu nabigatzailetik irtetea**: Saihestu ikasleek SEB itxi dezaten azterketan zehar
 - **Desgaitu laster-teklak**: Saihestu Alt+Tab edo Ctrl+W bezalako konbinazioak erabiltzea
 - **Pantaila osoko modua**: Behartu azterketa pantaila osoan erakustera
 - **Blokeatu pantaila-argazkiak**: Saihestu ikasleek edukia grabatzea

#### 🌐 Sare konfigurazioa
 - **Baimendu webgune zehatzak**: Baimendutako URL-en zerrenda zuria
 - **Blokeatu deskargak**: Saihestu fitxategien deskarga azterketan zehar
 - **Baimendu baliabide lokalak**: Baliagarria tokiko fitxategiak dituzten azterketetarako

### 3. Konfigurazio aurreratua

Konfigurazioa pertsonaliza dezakezu XML fitxategi baten bidez. Hona hemen garrantzitsuenak diren aukerak dituen adibide bat:

## ⚙️ Gomendatutako XML konfigurazioa

```xml
<?xml version="1.0" encoding="UTF-8"?>
<plist version="1.0">
<dict>
    <!-- Nabigazioa -->
    <key>allowBrowsingBackForward</key>
    <false/>
    <key>allowReloading</key>
    <false/>
    <key>newWindow</key>
    <false/>
    <key>enableSpellCheck</key>
    <false/>
    
    <!-- Nabigatzailearen leihoa -->
    <key>browserViewMode</key>
    <integer>1</integer> <!-- 1 = Pantaila osoa -->
    <key>hideToolbar</key>
    <true/>
    
    <!-- Segurtasuna -->
    <key>quitURL</key>
    <string>about:blank</string>
    <key>quitURLConfirm</key>
    <true/>
    
    <!-- Web edukia -->
    <key>enablePlugIns</key>
    <false/>
    <key>enableJava</key>
    <false/>
    <key>enableJavaScript</key>
    <true/>
    <key>enableCookies</key>
    <true/>
    
    <!-- Teklatua -->
    <key>enableKeychain</key>
    <false/>
    <key>enableInputManagers</key>
    <false/>
</dict>
</plist>
```

### 📝 Aukera garrantzitsuen azalpena

| Aukera | Balioa | Azalpena |
|--------|--------|-----------|
| `browserViewMode` | 1 | Pantaila osoa (2 = Leihoa, 3 = Ertzik gabe) |
| `allowReloading` | false | Saihestu orria berritzea azterketan zehar |
| `enablePlugIns` | false | Desaktibatu nabigatzailearen plugin guztiak |
| `enableJavaScript` | true | Beharrezkoa Moodle-ren funtzionamendurako |
| `quitURL` | about:blank | SEB-tik irtetean erakutsiko den orria |
| `enableKeychain` | false | Desaktibatu pasahitz-kutxaren sarbidea |

## 🛠️ Arazo arrunten konponbideak

### 1. Ikasleek ezin badute azterketa hasi
- **Sintomak**: SEB ez da abiatzen edo errorea erakusten du azterketa irekitzean
- **Konponbidea**:
    - Egiaztatu Moodle gunearen URLa ondo konfiguratuta dagoela SEB-en
    - Egiaztatu SSL ziurtagiria baliozkoa eta ongi instalatuta dagoela
    - Ziurtatu ikasleek SEB-ren bertsio egokia dutela instalatuta

### 2. Murrizketekin arazoak
- **Sintomak**: Murrizketak ez dira behar bezala aplikatzen
- **Konponbidea**:
    - Egiaztatu SEB konfigurazio fitxategia ondo formatuta dagoela
    - Egiaztatu ez daudela kontraesanezko konfiguraziorik XML fitxategian
    - Ziurtatu SEB nabigatzailea eguneratuta dagoela azken bertsiora

### 3. Konexio erroreak
- **Sintomak**: Konexio galera azterketan zehar
- **Konponbidea**:
    - Egiaztatu sare konexioaren egonkortasuna
    - Ziurtatu beharrezko portuak (80, 443) irekita daudela suebakiaren konfigurazioan
    - Konfiguratu itxaronaldia galdetegiaren konfigurazioan

## 📌 Aholku gehigarriak

1. **Aurreko probak**:
    - Beti egin probak proba-erabiltzaile baten aurretik
    - Egiaztatu murrizketa guztiek espero bezala funtzionatzen dutela

2. **Komunikazioa ikasleekin**:
    - Eman argibide argiak SEB nola instalatu eta erabiltzeari buruz
    - Egin saio proba bat ikasleekin azterketa errealaren aurretik

3. **Segurtasun kopia**:
    - Gorde erabilitako SEB konfigurazioaren kopia bat
    - Eduki B plan bat teknikoko arazoen kasurako

## 🔗 Baliabide gehigarriak

- [📚 SEB-ren dokumentazio ofiziala](https://safeexambrowser.org/)
- [🎓 Moodle-rekin integrazio gida osoa](https://docs.moodle.org/all/eu/Safe_Exam_Browser)
- [💬 SEB-ren laguntza foroa](https://safeexambrowser.org/support_forum/index.html)
- [SEB laguntza foroa](https://safeexambrowser.org/support_forum/index.html)
