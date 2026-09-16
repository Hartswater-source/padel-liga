# Padel Liga

Dashboard vir twee agt-speler padelgroepe oor agt weke — 'n vroueliga en 'n mansliga.

Die webwerf self bevat geen persoonlike inligting nie. Die name, bankbesonderhede,
speeltye, punte en betalings leef in Firestore en is slegs sigbaar vir wie met die
groep se wagwoord aangemeld het.

## Die twee ligas

Bo-aan die bladsy staan 'n knoppie om tussen **Vroue** en **Mans** te wissel.
Elke liga hou sy eie dokument in Firestore:

| Liga | Firestore-dokument | Geld |
|---|---|---|
| Vroue | `seasons/seisoen1` | Registrasie + fonds + bankbesonderhede |
| Mans | `seasons/mans1` | Geen — elke groep bespreek en betaal self |

By die mansliga is die Kostes-blad heeltemal weg.

## Lêers

| Lêer | Wat dit doen |
|---|---|
| `index.html` | Die bladsy se dop |
| `styles.css` | Alle uitleg en kleur |
| `app.js` | Die logika: ligas, rotasie, punte, koste |
| `config.js` | **Die enigste lêer wat jy invul** — jou Firebase-projek se besonderhede |
| `firestore.rules` | Die reëls om in die Firebase-konsole te plak |
| `robots.txt` | Hou soekenjins weg |
| `.nojekyll` | Nodig vir GitHub Pages |

## Opstel

1. Firebase-projek → Firestore-databasis → reëls uit `firestore.rules` plak.
2. Authentication → E-pos/wagwoord aan → een gebruiker skep → daardie adres by
   `SHARED_EMAIL` in `config.js`, en die wagwoord met die groep deel.
3. Webtoepassing registreer → die `firebaseConfig`-blok in `config.js` plak.
4. Alles na 'n GitHub-repo oplaai → Settings → Pages aanskakel.
5. Die GitHub-adres by Authentication → Settings → Authorized domains byvoeg.
6. Die adres oopmaak, wagwoord intik, en per liga die eenmalige opstelskerm invul.
