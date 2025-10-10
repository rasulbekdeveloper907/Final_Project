# 🧠 Tarixiy Shaxslar Umrini Bashoratlash — Classification Machine Learning Loyiha

## 📌 Loyihaning qisqacha tavsifi

Ushbu loyiha Machine Learning (ML) yordamida tarixiy shaxslarning qancha umr ko‘rganini **klassifikatsiya qilish** (toifalarga ajratish) maqsadida amalga oshirildi. Datasetda 2500 nafar tarixiy shaxs haqida ma’lumotlar mavjud bo‘lib, ular asosida shaxslarning umr davomiyligi quyidagi guruhlarga ajratildi:

- `0-30 yosh`
- `31-50 yosh`
- `51-70 yosh`
- `71+ yosh`

Ma’lumotlar asosida ML modellar yordamida har bir shaxs qaysi umr guruhiga kirishini aniqlashga harakat qilinadi.

---

## 📁 Ma'lumotlar (Dataset)

- **Manba**: [Dataset havolasi yoki manba nomi]
- **Yozuvlar soni**: 2500 ta tarixiy shaxs
- **Format**: CSV
- **Ustunlar**:
  - `Ism`
  - `Tug‘ilgan yil`
  - `Vafot etgan yil`
  - `Kasbi`
  - `Yashagan davri`
  - `Asr`
  - `Umr davomiyligi` (Target → klaslarga ajratilgan)

> **Target** (maqsadli ustun): `Umr_guruhi` (`0-30`, `31-50`, `51-70`, `71+`)

---

## 🎯 Loyihaning maqsadi

Model quyidagi savolga javob beradi:

> "Tarixiy shaxsning tug‘ilgan va vafot etgan yili, yashagan davri, kasbi kabi atributlarga qarab, u nechchi yoshgacha yashaganini bashorat qila olamizmi?"

---

## ⚙️ Ishlatilgan texnologiyalar

- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn (vizualizatsiya uchun)
- Jupyter Notebook

---

## 🛠️ Ish jarayoni

1. **Ma'lumotlarni tozalash**:  
   - Tug‘ilgan yoki vafot etgan sanasi yo‘q yozuvlar o‘chirildi
   - Noto‘g‘ri va manfiy qiymatlar filtrlandi

2. **Feature Engineering**:
   - `Umr = Vafot etgan yil - Tug‘ilgan yil`
   - `Umr` ustuni asosida toifalarga ajratilgan `Umr_guruhi` yaratildi
   - Asr, kasb va davr kabi ustunlar sonli formatga o‘tkazildi (`LabelEncoder`, `OneHotEncoder`)

3. **Model tanlash va o‘qitish**:
   - `Support Vector Machine (SVM)`
   - `K-Nearest Neighbors (KNN)`
   - `Decision Tree`
   - `Random Forest`

4. **Model baholash**:
   - `Accuracy`
   - `Confusion Matrix`
   - `Classification Report (Precision, Recall, F1-score)`

---

## 📊 Natijalar

| Model           | Accuracy (%) |
|------------------|--------------|
| SVM              | 88%          |
| KNN              | 85%          |
| Decision Tree    | 90%          |
| Random Forest    | **83%** ✅   |

> ✅ **Eng yaxshi model**: Random Forest — 83% aniqlik bilan to‘g‘ri tasniflagan.

---

## 📈 Vizualizatsiyalar

- Confusion Matrix grafigi
- Umr guruhlarining taqsimoti
- Har bir model uchun F1-score solishtirmasi

---

## 🚀 Kelajakdagi ishlar

- Ko‘proq atributlar qo‘shish (hudud, shaxsning statusi: podsho, sarkarda, oddiy fuqaro va h.k.)
- Modelni balansi notekis sinflar uchun yaxshilash (class imbalance)
- Web interfeys yaratish (Streamlit orqali)

---

## 💻 Ishga tushirish

```bash
git clone https://github.com/username/tarixiy-umr-klassifikatsiyasi.git
cd tarixiy-umr-klassifikatsiyasi
pip install -r requirements.txt
jupyter notebook
