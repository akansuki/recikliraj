# Recikliraj! 🗺️

Mapa reciklažnih mesta za papir, baterije i aluminijum u Novom Sadu, Srbija.

## 📋 Opis

Recikliraj! je interaktivna web aplikacija koja prikazuje lokacije reciklažnih mesta na mapi. Aplikacija omogućava korisnicima da pronađu najbliža mesta za reciklažu papira, baterija i aluminijuma.

## ✨ Funkcionalnosti

- 🗺️ **Interaktivna mapa** - Prikaz reciklažnih mesta na OpenStreetMap kartama
- 📍 **Geolokacija** - Automatsko pronalaženje korisnikove lokacije
- 🔄 **Retry geolokacije** - Dugme za ponovno pronalaženje lokacije
- 📊 **Statistika** - Prikaz broja mesta po tipovima reciklaže
- 📱 **Responsive dizajn** - Optimizovano za desktop i mobilne uređaje
- 🎨 **Legenda** - Objašnjenje tipova markera na mapi
- ⏳ **Loading indikator** - Vizuelna povratna informacija tokom učitavanja podataka
- ✅ **Validacija podataka** - Automatska provera ispravnosti podataka

## 🛠️ Tehnologije

- **Leaflet.js** - Biblioteka za interaktivne mape
- **OpenStreetMap** - Tile slojevi za kartografiju
- **Font Awesome** - Ikone
- **Bootstrap 5** - CSS framework
- **jQuery** - DOM manipulacija
- **Leaflet Awesome Markers** - Prilagođeni markeri

## 🚀 Instalacija i pokretanje

### Preduslovi

- Python 3.x (za lokalni development server)
- Moderni web pregledač sa podrškom za ES6

### Pokretanje lokalnog servera

1. Klonirajte repozitorijum:

```bash
git clone https://github.com/akansuki/recikliraj.git
cd recikliraj
```

2. Pokrenite Python server:

```bash
python start-server.py
```

3. Otvorite aplikaciju u browseru:

```
http://localhost:8000/index.html
```

### Direktno otvaranje

Možete direktno otvoriti `index.html` u browseru, ali neki browseri mogu blokirati učitavanje lokalnih JSON fajlova zbog CORS politike. Preporučuje se korišćenje lokalnog servera.

## 📊 Format podataka

Podaci o reciklažnim mestima se čuvaju u `markers.json` fajlu u sledećem formatu:

```json
[
  {
    "types": ["paper"],
    "coordinates": [45.24832, 19.840079],
    "name": "Maksima Gorkog 1"
  },
  {
    "types": ["paper", "battery"],
    "coordinates": [45.26049, 19.80656],
    "name": "Lidl Novo Naselje"
  }
]
```

## 🔧 Razvoj

### Dodavanje novih lokacija

1. Otvorite `markers.json`
2. Dodajte novi objekat sa poljima `types`, `coordinates` i `name`
3. Validacija će automatski proveriti ispravnost podataka

### Validacija

Aplikacija automatski validira:

- Postojanje obaveznih polja
- Tip podataka (array, string, number)
- Validnost koordinata (latitude: -90 do 90, longitude: -180 do 180)
- Validnost tipova reciklaže

Greške se loguju u konzoli pregledača.

---

Napravljeno sa ❤️ za bolju reciklažu u Novom Sadu
