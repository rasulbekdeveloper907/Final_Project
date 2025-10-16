# Historical Figures — Data Collection (Web Scraping)

---

## 1. Loyiha haqida

Ushbu loyiha `https://en.wikipedia.org/wiki/Historical_figure` sahifasidan **2650 ta tarixiy shaxs** haqidagi ma’lumotlarni web scraping orqali yig‘ishni maqsad qilgan. Yig‘ilgan ma’lumotlar keyinchalik `life_span` (hayot davomiyligi) ni taxmin qilish uchun regressiya modeliga tayyorlanadi.

---

## 2. Maqsad va asosiy printsiplar

- **Reproducibility:** Har safar bir xil natija olish uchun kod va jarayonlar aniq va qayta ishlanadigan bo‘lishi.
- **Etika va qonuniylik:** Saytning `robots.txt` va foydalanish shartlariga (ToS) qat’iy rioya qilish, serverga zarar yetkazmaslik.
- **Robustlik:** So‘rovlar uchun retry (qayta urinish) mexanizmi, xatoliklarni ushlash va qayta ishlash.
- **To‘liq metadata:** Har bir yozuv uchun original manba URL, yig‘ilgan sana-vaqt, scraper va parser versiyalari kiritiladi.

---


## 3. Litsenziya

Ushbu loyiha uchun MIT LICENSE tavsiya etiladi (agar sizga mos bo‘lsa).

Ma’lumotlar manbai — Wikipedia (CC BY-SA 3.0).
Ma’lumotlardan foydalanishda ushbu litsenziya shartlarini hurmat qiling.