# Moodle-rekin integrazioa

## Moodle-n SEB konfigurazio oinarrizkoa

### Aurrebaldintzak
- Moodle 3.5 edo berriagoa instalatuta izatea
- Moodle gunean administratzaile baimenak izatea
- SEB nabigatzailea ikasleen ordenagailuetan instalatuta izatea

### Moodle-n SEB konfiguratzeko urratsak

1. **Azterketa bat konfiguratu SEB-rekin**
    - Sortu edo editatu azterketa bat Moodle-n
    - Galdetegiaren konfigurazioan, joan "Safe Exam Browser" atalera
    - Hautatu "Bai" "Safe Exam Browser behar da" aukeran
    - Konfiguratu nahi diren murrizketak:
      - Atera nabigatzailetik debekatu
      - Laster-teklak desgaitu
      - Konfiguratu nabigazio modua

### Gomendatutako konfigurazioa azterketetarako

```xml
<?xml version="1.0" encoding="UTF-8"?>
<plist version="1.0">
<dict>
    <key>allowBrowsingBackForward</key>
    <false/>
    <key>allowReloading</key>
    <false/>
    <key>browserViewMode</key>
    <integer>1</integer>
    <key>enablePlugIns</key>
    <false/>
    <key>enableJavaScript</key>
    <true/>
    <key>enableJava</key>
    <false/>
    <key>enableCookies</key>
    <true/>
</dict>
</plist>
```

### Arazo arrunten konponbideak

1. **Ikasleek ezin badute azterketa hasi**
   - Egiaztatu Moodle-ren URLa ondo konfiguratuta dagoela SEB-en
   - Egiaztatu SSL ziurtagiria baliozkoa dela

2. **Murrizketekin arazoak**
   - Egiaztatu SEB konfigurazioa ondo aplikatu dela galdetegian
   - Egiaztatu ez daudela kontraesanezko konfiguraziorik

3. **Konexio erroreak**
   - Egiaztatu sare konexioa
   - Egiaztatu behar diren portuak irekita daudela

### Baliabide gehigarriak
- [SEB-ren dokumentazio ofiziala](https://safeexambrowser.org/)
- [Moodle-rekin integrazio gida](https://docs.moodle.org/all/eu/Safe_Exam_Browser)
- [SEB laguntza foroa](https://safeexambrowser.org/support_forum/index.html)
