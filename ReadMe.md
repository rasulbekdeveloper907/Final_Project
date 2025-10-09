# 🎯 Loyiha nomi:
**Vaqealar Kalendari: Semantik Afisha Yig‘ish Tizimi**

---

## 📌 1. Loyiha Tavsifi

Mazkur loyiha doirasida, foydalanuvchilar uchun konsertlar, teatrdagi sahnalar, ko‘rgazmalar, festivallar va boshqa madaniy tadbirlar haqidagi ma’lumotlarni turli saytlardan avtomatik yig‘ib, **semantik modelga asoslangan kalendar** shaklida taqdim etuvchi tizim ishlab chiqiladi.

---

## 🎯 2. Loyiha Maqsadi

- Web scraping orqali turli manbalardan tadbir ma’lumotlarini yig‘ish  
- Yig‘ilgan ma’lumotlarni vaqt, joy, janr, tashkilotchi kabi atributlar asosida **semantik modellashtirish**  
- Tadbirlarni filtrlash, saralash va qidirish imkoniyatini beruvchi **foydalanuvchi interfeys** yaratish  

---

## 🧩 3. SML: Semantik Modellashtirish

### 🎭 Event (Tadbir) klassi:

Event
│
├── name (nomi)
├── date (sana)
├── time (vaqt)
├── location (joy)
├── type (turi: konsert, teatr, ko‘rgazma...)
├── organizer (tashkilotchi)
├── price (narx)
├── language (til, agar spektakl bo‘lsa)


### 🧠 Ontologik Tuzilma (soddalashtirilgan):

Thing
│
├── Event
│ ├── Concert
│ ├── Theater
│ ├── Exhibition
│ ├── Festival
│
├── Location
│ ├── City
│ ├── Venue
│
├── Organizer


> Ushbu modelni **OWL (Web Ontology Language)** formatida yaratib, **RDF** bilan bog‘lash mumkin. SPARQL yordamida semantik qidiruvlar amalga oshiriladi.

---

## 🔧 4. Texnologiyalar

| Maqsad                   | Texnologiya yoki vosita        |
|--------------------------|-------------------------------|
| Web scraping             | Python (BeautifulSoup, Scrapy) |
| Ma’lumotlar saqlash      | MongoDB / PostgreSQL / RDF Store |
| Ontologiya yaratish      | Protégé (ontologiya modeli)   |
| Semantik qidiruv         | SPARQL                        |
| Backend                  | Flask / Django                |
| Frontend (ixtiyoriy)     | React / Bootstrap             |

---

## 🌐 5. Web Scraping Nishonlari (manbalar)

- https://afisha.uz  
- https://biletonline.uz  
- https://iTicket.uz  
- Teatrlar, san’at galereyalari, konsert zallari saytlarining afisha bo‘limlari

---

## 📊 6. Foydalanuvchi Uchun Imkoniyatlar

- "Bugungi konsertlar"ni ko‘rish  
- Joy, sana, turi bo‘yicha **filtrlash**  
- "Toshkentdagi teatrdagi spektakllar" degan **semantik so‘rovlar** yuborish  
- JSON-LD yoki RDF formatida **ma’lumotni eksport qilish**  

---

## ✅ 7. Kutilayotgan Natijalar

- Semantik modellashtirilgan **tadbirlar bazasi**  
- Avtomatik ma’lumot yig‘uvchi **scraper**  
- Foydalanuvchilarga qulay **qidiruv interfeysi**  
- **SML tamoyillari asosida ontologik tizim**

---

> 🧠 Loyiha ilmiy, amaliy va texnik jihatdan dolzarb bo‘lib, SML (Semantik Mantiqiy Loyihalash) yondashuvlarini chuqur o‘rganish uchun ajoyib asos bo‘ladi.

