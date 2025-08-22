# Mobile Price Range Prediction

## 📌 Layihə haqqında
Bu layihə mobil telefonların texniki xüsusiyyətlərinə əsasən qiymət aralığını (`price_range`) proqnozlaşdırmaq üçün **Logistic Regression** modellərini istifadə edir. 
L1 və L2 regularizasiyaları müqayisə edilir, ən yaxşı parametrlər GridSearchCV ilə tapılır və nəticələr həm də **SHAP interpretability** vasitəsilə izah olunur.

## 🎯 Məqsəd
- Logistic Regression ilə təsnifat modelini qurmaq
- L1 və L2 regularizasiyalarını müqayisə etmək
- Modelin nəticələrini Confusion Matrix ilə göstərmək
- SHAP ilə modelin qərar mexanizmini interpretasiya etmək

## ⚙️ Texnologiyalar
- Python (pandas, numpy, scikit-learn)
- Matplotlib, Seaborn (vizualizasiya)
- SHAP (interpretability)

## 🚀 Addımlar
1. Dataset yüklənir və train/test bölünməsi aparılır
2. Xüsusiyyətlər `StandardScaler` ilə miqyaslandırılır
3. `GridSearchCV` ilə ən yaxşı Logistic Regression parametrləri tapılır
4. L1 və L2 modelləri qurularaq nəticələr müqayisə edilir
5. Confusion Matrix ilə nəticələr vizual göstərilir
6. SHAP ilə ən vacib xüsusiyyətlər interpretasiya olunur

## 📊 Nəticələr
- Ən yaxşı model: **Logistic Regression (L2, C=100, solver=lbfgs)**
- Train Accuracy: ~0.987  
- Test Accuracy: ~0.99  

### Confusion Matrix
- L1 və L2 modelləri üçün qarışıqlıq matrisləri vizual olaraq göstərilmişdir.

### SHAP interpretability
- Ən təsirli xüsusiyyətlərdən biri **RAM** olmuşdur.
- Digər vacib xüsusiyyətlər: `battery_power`, `px_height`, `px_width`.

## 📌 Qeydlər
- Layihə təhsil və portfel məqsədi ilə hazırlanmışdır.
- Gələcəkdə əlavə modellərlə (RandomForest, XGBoost) müqayisə edilə bilər.
