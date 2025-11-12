# Franse Huizen Checker

Een complete tool voor het kopen van een huis in Frankrijk, met prijschecker en interactieve valkuilen checklist.

🔗 **Live Demo:** https://antonnoe.github.io/franse-huizen-checker/

## ✨ Features

### 📍 Adres Zoeker
- Live autocomplete met Franse adressen
- Officiële BAN (Base Adresse Nationale) API
- Snelle zoekresultaten

### 💰 Prijzen Checker
- Recente verkopen binnen 5km radius
- Gemiddelde prijzen & prijs per m²
- Prijsranges (min/max)
- DVF (Demandes de Valeurs Foncières) Open Data
- Updates 2x per jaar door de Franse overheid

### ✅ Interactieve Checklist
- 39 valkuilen bij het kopen van een huis in Frankrijk
- Gebaseerd op 30+ jaar ervaring
- Categorieën: Voorbereiding, Financieel, Juridisch, Technisch, etc.
- Progress tracker
- Automatisch opslaan in browser
- Uitklapbare details per punt

## 🚀 Deployment naar GitHub Pages

### Stap 1: Upload bestanden naar GitHub

```bash
# Clone de repository
git clone https://github.com/antonnoe/franse-huizen-checker.git
cd franse-huizen-checker

# Voeg index.html toe
git add index.html
git commit -m "Add Franse Huizen Tool"
git push origin main
```

### Stap 2: Activeer GitHub Pages

1. Ga naar je repository op GitHub: https://github.com/antonnoe/franse-huizen-checker
2. Klik op **Settings** (tandwiel icoon)
3. Scroll naar beneden naar **Pages** in het linker menu
4. Bij **Source** selecteer: **Deploy from a branch**
5. Bij **Branch** selecteer: **main** en folder **/ (root)**
6. Klik **Save**

### Stap 3: Wacht op deployment

- Na 1-2 minuten is de site live op: https://antonnoe.github.io/franse-huizen-checker/
- Je krijgt een groen vinkje te zien bij "Your site is live at..."

## 🔧 Integratie in WordPress

### Methode 1: iFrame (simpel)

```html
<iframe 
  src="https://antonnoe.github.io/franse-huizen-checker/" 
  width="100%" 
  height="1200px"
  frameborder="0"
  style="border: none;">
</iframe>
```

### Methode 2: Direct embed (HTML block in Gutenberg)

1. Maak een nieuw artikel/pagina in WordPress
2. Voeg een **Custom HTML** block toe
3. Plak de iframe code hierboven
4. Publiceer!

## 📝 Checklist Uitbreiden

De checklist zit in de `VALKUILEN` array in `index.html`. Om items toe te voegen:

```javascript
{
  id: 40,  // Volgend nummer
  title: "Titel van de valkuil",
  description: "Uitgebreide beschrijving met advies",
  category: "financieel"  // Kies: voorbereiding, financieel, juridisch, technisch, locatie, renovatie, keuring, erfrecht, veiligheid, buurt
}
```

Voeg items toe aan de `VALKUILEN` array (rond regel 40 in index.html).

## 🎨 Kleuren Aanpassen

De primaire kleur is `#800000` (bordeaux rood). Om te wijzigen:

1. Zoek naar `#800000` in index.html
2. Vervang alle voorkomsten met je nieuwe kleur
3. Push naar GitHub

## 🔄 Updates Maken

```bash
# Maak je wijzigingen in index.html
git add index.html
git commit -m "Update checklist met nieuwe valkuilen"
git push origin main

# GitHub Pages update automatisch binnen 1-2 minuten
```

## 📊 Gebruikte APIs

### DVF+ Open Data API
- **URL:** https://apidf-preprod.cerema.fr/dvf_opendata/
- **Licentie:** Open Data (Licence Ouverte 2.0)
- **Updates:** 2x per jaar (april & oktober)
- **Data:** Alle Franse vastgoedtransacties sinds 2014

### BAN (Base Adresse Nationale)
- **URL:** https://api-adresse.data.gouv.fr
- **Licentie:** Open Data
- **Updates:** Continue updates
- **Data:** Alle Franse adressen

## 🛠️ Technische Stack

- **React 18** - UI Framework (via CDN)
- **Tailwind CSS** - Styling (via CDN)
- **Lucide Icons** - Icon set (via CDN)
- **Vanilla JavaScript** - No build process needed!

## 📱 Browser Support

- ✅ Chrome/Edge (laatste 2 versies)
- ✅ Firefox (laatste 2 versies)
- ✅ Safari (laatste 2 versies)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🐛 Troubleshooting

### Tool laadt niet
- Check of GitHub Pages is geactiveerd in Settings
- Wacht 2-3 minuten na de eerste deployment
- Check de Console (F12) voor errors

### Prijzen laden niet
- DVF API kan soms traag zijn
- Sommige gebieden hebben weinig data
- API updates 2x per jaar

### Checklist wordt niet opgeslagen
- Check of LocalStorage is ingeschakeld in de browser
- Private/Incognito mode kan LocalStorage blokkeren

## 📄 Licentie

© 2025 Communities Abroad (Anton Noë)

## 🤝 Contact

- Website: https://infofrankrijk.com
- Forum: https://nederlanders.fr
- KvK: 55741509

## 🎯 Toekomstige Features

- [ ] Kaart view met verkochte huizen
- [ ] Export checklist naar PDF
- [ ] Vergelijk tool (meerdere adressen)
- [ ] Prijstrend grafieken
- [ ] Franse vertaling
- [ ] 100+ extra valkuilen toevoegen
- [ ] Email reminders voor checklist items
