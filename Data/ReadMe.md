# 🧠 Tarixiy Shaxslar Ma'lumotlari — Tahlil va Bashorat Loyihasi

## 📌 Loyihaning qisqacha tavsifi

Ushbu loyiha tarixiy shaxslarning boy bio-ma’lumotlar to‘plami asosida ularning hayoti, yutuqlari, kasbi, yashagan joyi, tahsili va oilaviy ahvoli kabi atributlar asosida **tahlil qilish**, **tozalash**, hamda Machine Learning orqali **umr davomiyligini bashorat qilish**ga qaratilgan.

Loyihaning asosiy maqsadi:
> **Tarixiy shaxslarning kasbi, yashagan asri va boshqa atributlari ularning umriga qanday ta’sir qilganini o‘rganish.**

---

## 🧾 Dataset haqida

- **Fayl nomi**: `historical_figures.csv`  
- **Yozuvlar soni**: 2022 ta  
- **Ustunlar soni**: 20 ta  
- **Hajmi**: ~316 KB  
- **Format**: CSV (UTF-8)

### 🔍 Ustunlar (Columnlar) tavsifi:

| Ustun nomi       | Tavsifi |
|------------------|---------|
| `name`           | Shaxsning to‘liq ismi |
| `birth_date`     | Tug‘ilgan sana (ko‘pincha `{{birth date|...}}` formatida) |
| `birth_place`    | Tug‘ilgan joyi |
| `death_date`     | Vafot etgan sana (`{{death date|...}}` formatida) |
| `death_place`    | Vafot etgan joyi |
| `nationality`    | Millati yoki fuqaroligi |
| `occupation`     | Kasbi yoki lavozimi |
| `years_active`   | Faol bo‘lgan yillari |
| `known_for`      | Nima bilan mashhur bo‘lganligi |
| `awards`         | Olgan mukofotlari |
| `alma_mater`     | O‘qigan oliy ta’lim muassasalari |
| `education`      | Ta’lim darajasi |
| `employer`       | Ishlagan tashkilotlari |
| `notable_works`  | Muhim asarlari |
| `field`          | Faoliyat sohasi (fan, san’at, siyosat va h.k.) |
| `spouse`         | Turmush o‘rtog‘i |
| `children`       | Farzandlari |
| `parents`        | Ota-onasi |
| `religion`       | Dini |
| `genre`          | Asar yozgan janri (agar bo‘lsa) |

---

## 🧹 Ma’lumotlarni tozalash (Data Cleaning)

Loyihada quyidagi **tozalash bosqichlari** bajarildi:

- `birth_date` va `death_date` ustunlaridagi **Wiki-sintaksis (`{{birth date|...}}`)** formatini pars qilish.
- `death_date - birth_date` orqali **`life_span`** ustuni hosil qilindi.
- Noto‘liq yoki bo‘sh `death_date` yozuvlari olib tashlandi (bashorat uchun yaroqsiz).
- Nomutanosib, g‘alati yoki noto‘g‘ri qiymatlar (`life_span > 120`, `life_span < 10`) chiqarib tashlandi.
- `occupation`, `field`, `nationality` kabi ustunlar bir necha qiymatli bo‘lishi mumkinligi sababli, `explode()` yoki `multi-label encoding` usullari ko‘rib chiqildi.
- Matnli ustunlardan **text preprocessing** ishlari: lowercasing, stripping, format tozalash (`{{...}}`, `[[...]]`, `|` belgilaridan tozalash)

---

## 🎯 Loyihaning maqsadi

> Tarixiy shaxslarning atributlari asosida ularning **umr davomiyligini regressiya orqali bashorat qilish**.

Yondashuvlar:
- Regression (life_span ni son sifatida bashorat qilish)
- Kasblarga qarab o‘rtacha umr tahlili
- Model baholash va eng yaxshi algoritmni tanlash

---

## 🤖 Ishlatilgan texnologiyalar

- **Python 3.x**
- **Pandas, NumPy** — ma’lumotlarni qayta ishlash
- **Matplotlib, Seaborn** — vizualizatsiya
- **Scikit-learn** — ML modellar
- **XGBoost** — ilg‘or ML model
- **Regex (re module)** — matnni tozalash

---

## 🧠 Regression modellari natijalari

| Model                | R² (aniqlik) |
|----------------------|--------------|
| Decision Tree        | ✅ **1.00** (100%) |
| Random Forest        | 0.91         |
| XGBoost              | 0.99         |
| Linear Regression    | 0.20         |

> **Eng yaxshi model**: `Decision Tree Regressor`

---

## 📈 Vizualizatsiyalar

- 📊 Kasblar bo‘yicha o‘rtacha `life_span` (barplot)
- 📉 Model R² solishtiruv grafigi
- 🔍 Predict vs Actual umr davomiyligi (scatter plot)
- 📂 Null/NaN qiymatlarning taqsimoti (heatmap)

---

## 🔮 Qiziqarli kuzatishlar

- 👑 **Monarxlar**, **olimlar**, va **san’atkorlar** orasida umr davomiyligi nisbatan uzun bo‘lgan.
- 🛠️ Ko‘p hollarda `occupation` mavjud bo‘lmagan shaxslar uchun model noto‘g‘ri baho beradi.
- 📜 O‘rta asr shaxslarining ma’lumotlari ko‘pincha noaniq yoki noto‘liq.

---

## 🚀 Kelajakdagi reja

- [ ] Streamlit yoki Gradio yordamida interaktiv UI yaratish
- [ ] Wikipedia API orqali avtomatik attribute to‘ldirish
- [ ] Kross-valyadatsiya bilan modelni yanada mustahkamlash
- [ ] Kasblar asosida klasterlash (unsupervised learning)

---

## 💻 Loyihani ishga tushirish

```bash
git clone https://github.com/username/historical-lifespan-predictor.git
cd historical-lifespan-predictor
pip install -r requirements.txt
jupyter notebook


🧑‍💻 Muallif

👨‍💻 Ism: Rasulbek 

💌 Email: rassiazzi9218@gmail.com

🔗 GitHub: https://github.com/rasulbekdeveloper907
