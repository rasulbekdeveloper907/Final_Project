# 🤖 Machine Learning Modellari — Regression tahlili

Bu bo‘limda biz tarixiy shaxslarning umr davomiyligini (ya'ni `life_span`) turli regressiya modellar orqali bashorat qilishga harakat qildik. `Models/` papkasi ushbu modellarni yaratish, o‘qitish, baholash va saqlashga oid kodlarni o‘z ichiga oladi.

---

## 🎯 Maqsad

> "Tarixiy shaxsning tug‘ilgan va vafot etgan sanasi, kasbi, ta’limi kabi atributlar asosida u nechchi yoshgacha yashaganini aniqlay olamizmi?"

**Target ustun**: `life_span` (butun son, yil)

---

## ⚙️ Ishlatilgan Regression modellari

1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**
4. **XGBoost Regressor**

---

## 🧪 Modellar natijalari (R² — Determinatsiya koeffitsienti)

| Model                   | R² Score  | Izoh |
|-------------------------|-----------|------|
| ✅ Decision Tree         | **1.00**   | Treningda to‘liq moslik |
| Random Forest           | 0.91      | Kengaytirilgan, barqaror model |
| XGBoost                 | 0.99      | Tez va aniq model, past overfitting |
| Linear Regression       | 0.20      | Oddiy model, lekin kam aniqlik |

> **Eng yaxshi model**: `DecisionTreeRegressor` (lekin ehtiyot bo‘ling: bu overfitting bo‘lishi mumkin)

---
📁 Model fayllari

| Fayl nomi                 | Taqdim etilgan maqsad            |
| ------------------------- | -------------------------------- |
| `linear_model.pkl`        | `LinearRegression()` obyekt      |
| `decision_tree_model.pkl` | `DecisionTreeRegressor()` obyekt |
| `random_forest_model.pkl` | `RandomForestRegressor()` obyekt |
| `xgb_model.pkl`           | `XGBRegressor()` obyekt          |


🧠 Xulosa

Decision Tree modeli life_span ustunini ideal tarzda moslashtirdi, lekin bu overfitting bo‘lishi mumkin.

Random Forest va XGBoost modellarining ishlashi yuqori va yanada barqaror.

Linear Regression juda past natija ko‘rsatdi — bu model bu tipdagi murakkab atributlar uchun yaroqsiz.

📌 Kelajakdagi ishlar:

 Kross-valyadatsiya (cross_val_score) orqali modelni baholash

 Pipeline yordamida to‘liq jarayonni avtomatlashtirish

 Modelni .joblib orqali saqlash va Streamlit ilovasiga integratsiya qilish

 Ensemble Learning (bir nechta modelni birlashtirish)

📂 Fayl tuzilmasi (Models/ papkasi)
 Models/
├── decision_tree_model.pkl
├── random_forest_model.pkl
├── xgb_model.pkl
├── linear_model.pkl
├── model_utils.py
├── model_training.ipynb
└── README.md

🧑‍💻 Muallif

👨‍💻 Ism: Rasulbek 

💌 Email: rassiazzi9218@gmail.com

🔗 GitHub: https://github.com/rasulbekdeveloper907


"Model tanlash — bu faqat raqamlar emas, balki ehtiyoj va kontekstga mos yechim topishdir."