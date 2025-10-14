# 🧠 Tarixiy Shaxslarning Kasbiga Ko‘ra Umrini Bashoratlash — Regression Machine Learning Loyiha

## 📌 Loyihaning qisqacha tavsifi

Ushbu loyiha tarixiy shaxslarning kasbi va boshqa atributlari asosida ularning umr davomiyligini **doimiy son (yillar)** sifatida bashorat qilishga qaratilgan. Maqsad — qaysi kasb egalari uzoq umr ko‘rganini aniqlash va bashorat qilish.

Datasetda 2500 dan ortiq tarixiy shaxs haqidagi ma’lumotlar mavjud bo‘lib, ularning tug‘ilgan va vafot etgan yili, kasbi, yashagan davri kabi atributlar kiritilgan.

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
  - `Umr davomiyligi` (target — sonli qiymat sifatida)

---

## 🎯 Loyihaning maqsadi

> Tarixiy shaxslarning kasbiga va boshqa atributlarga asoslanib, ularning umr davomiyligini yillar bo‘yicha aniq bashorat qilish.

---

## ⚙️ Ishlatilgan texnologiyalar

- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib / Seaborn (vizualizatsiya uchun)
- Jupyter Notebook

---

## 🛠️ Ish jarayoni

1. **Ma'lumotlarni tozalash**  
   - Tug‘ilgan yoki vafot etgan yili bo‘lmagan yozuvlarni olib tashlash  
   - Noto‘g‘ri va manfiy qiymatlarni filtr qilish  

2. **Feature Engineering**  
   - `Umr = Vafot etgan yil - Tug‘ilgan yil` sifatida hisoblash  
   - Kasb, asr va yashagan davr kabi kategorik ustunlarni raqamli formatga o'tkazish (`LabelEncoder`, `OneHotEncoder`)  

3. **Model tanlash va o‘qitish**  
   - Decision Tree Regressor  
   - Random Forest Regressor  
   - Linear Regression  
   - XGBoost Regressor  

4. **Model baholash**  
   - R² (R-squared) balli orqali aniqlik baholandi  

---

## 📊 Natijalar

| Model               | R² balli (%) |
|---------------------|--------------|
| Decision Tree       | 100.0%       |
| Random Forest       | 91.0%        |
| Linear Regression   | 20.0%        |
| XGBoost             | 99.0%        |

> ✅ **Eng yaxshi natija**: Decision Tree Regressor — 100% R² balli bilan.

---

## 📈 Vizualizatsiyalar

- Kasb bo‘yicha umr davomiyligi taqsimoti  
- Modellarning R² ballarini solishtirish grafigi  
- Predict va actual qiymatlar taqqoslanishi grafigi  

---

## 🚀 Kelajakdagi reja

- Qo‘shimcha atributlar kiritish (hudud, shaxsning ijtimoiy mavqei va boshqalar)  
- Modelni yanada yaxshilash uchun hyperparameter tuning  
- Kross-valyadatsiya asosida model barqarorligini oshirish  
- Interaktiv web-interfeys yaratish (Streamlit yoki Flask)  

---

## 💻 Loyihani ishga tushirish

```bash
git clone https://github.com/username/tarixiy-kasb-umr-bashorati.git
cd tarixiy-kasb-umr-bashorati
pip install -r requirements.txt
jupyter notebook


📞 Aloqa

Loyihaga oid savollar uchun:
Email: rassiazzi9218@gmail.com

GitHub: https://github.com/rasulbekdeveloper907