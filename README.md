[TR]
# Loan Prediction Projesi

Bu proje, bir finans kurumundaki müşterilerin kredi ödeme olasılıklarını (iyi/kötü müşteri) tahmin edebilecek bir model geliştirmeyi amaçlamaktadır. Ayrıca, model temelinde kredi başvurusu sırasında müşterilere sorulması gereken sorular belirlenmiştir.

---

## Proje Hedefleri

1. **Kredi Ödeme Tahmini**: Müşterilerin kredi ödeme durumlarını tahmin ederek kredi riskini minimize etmek.
2. **Soruların Belirlenmesi**: Müşterilerden toplanması gereken önemli bilgileri belirlemek.

---

## Veri Analizi (EDA)

Veri setinde toplam **256.984** gözlem ve **19** değişken bulunmaktadır. Eksik veriler ve aykırılık değerleri temizlenmiş, istatistiksel analiz gerçekleştirilmiştir. Aykırılıklar ve eksik verilerle ilgili yapılan işlemler şunlardır:

- **Eksik Veriler**: 
  - `Credit Score`, `Years in Current Job`, `Annual Income` gibi eksik değerler doldurulmuştur.
  - `Months Since Last Delinquent` sütunu çok fazla eksik veri içerdiği için kaldırılmıştır.

- **Aykırılıklar**: 
  - `Current Loan Amount`, `Credit Score`, `Number of Open Accounts` gibi değişkenlerde bulunan aykırılık değerler düzeltilmiştir.

---

## Özellik Mühendisliği (Feature Engineering)

Aşağıdaki yeni değişkenler oluşturulmuştur:
- **Loan Count**: Müşterinin sahip olduğu toplam kredi sayısı.
- **Total Loan Amount**: Müşterinin toplam kredi tutarı.

Kategorik değişkenler için "one-hot encoding" yöntemi kullanılmış ve veri ölçeklendirilmiştir.

---

## Modelleme

Kullanılan algoritmalar ve doğruluk oranları:
- **Lojistik Regresyon**: %99.86
- **K-En Yakın Komşu (KNN)**: %99.44
- **Destek Vektör Makineleri (SVM)**: %99.86
- **Rastgele Orman (Random Forest)**: %99.86
- **Naive Bayes**: %99.07
- **Karar Ağacı**: %99.71

En iyi model: **Lojistik Regresyon (Logistic Regression)** %99.86 doğruluk oranıyla.

### Model Sonuçları
- Doğruluk oranı: %99.86
- Karışıklık Matrisi (Confusion Matrix):
  - **İyi Müşteri** doğru tahmin sayısı: 22.113
  - **Kötü Müşteri** doğru tahmin sayısı: 11.884

---

## Sonuçlar ve Sorular

Bu proje, kredi riskini değerlendirmek için yüksek doğruluk oranına sahip bir model sunmuştur. Projenin sonuçları sayesinde finans kuruluşları, müşteri seçim süreçlerini optimize edebilir.

### Müşterilere Sorulacak Sorular:
1. Kredi skorunuz nedir?
2. Toplam kredi miktarınız (Total Loan Amount) ne kadar?
3. Kaç açık kredi hesabınız var?
4. Kredinizin süresi nedir? (Kısa veya uzun vade)
5. Mevcut kredi bakiyeniz nedir?

---

[EN]
# Loan Prediction Project

This project aims to develop a model that predicts whether a customer of a financial institution is likely to repay their loan (good/bad customer). Additionally, based on the model, questions to be asked to customers during loan applications are identified.

---

## Project Goals

1. **Loan Repayment Prediction**: Predict customers' loan repayment status to minimize credit risk.
2. **Questionnaire Design**: Determine the essential information required from customers during the loan application process.

---

## Exploratory Data Analysis (EDA)

The dataset consists of **256,984** observations and **19** variables. Missing data and outliers have been cleaned, and statistical analysis was performed. Key steps include:

- **Handling Missing Data**:
  - Missing values in columns like `Credit Score`, `Years in Current Job`, and `Annual Income` were filled with appropriate measures (mean or median).
  - The column `Months Since Last Delinquent` was dropped due to a large number of missing values.

- **Handling Outliers**:
  - Outliers in `Current Loan Amount`, `Credit Score`, and `Number of Open Accounts` were corrected.

---

## Feature Engineering

The following new features were created:
- **Loan Count**: The total number of loans a customer has.
- **Total Loan Amount**: The total amount of loans a customer owes.

Categorical variables were encoded using one-hot encoding, and data was standardized for modeling.

---

## Modeling

The following algorithms were evaluated with their respective accuracy scores:
- **Logistic Regression**: 99.86%
- **K-Nearest Neighbors (KNN)**: 99.44%
- **Support Vector Machines (SVM)**: 99.86%
- **Random Forest**: 99.86%
- **Naive Bayes**: 99.07%
- **Decision Tree**: 99.71%

**Best Model**: **Logistic Regression** with an accuracy of 99.86%.

### Model Results
- **Accuracy**: 99.86%
- **Confusion Matrix**:
  - Correctly predicted **Good Customers**: 22,113
  - Correctly predicted **Bad Customers**: 11,884

---

## Outcomes and Recommendations

This project provides a high-accuracy model to assess credit risk effectively. Financial institutions can leverage the results to optimize customer selection processes.

### Questions to Ask Customers:
1. What is your current credit score?
2. What is your total loan amount?
3. Do you have multiple open credit accounts?
4. What is the term of your loan? (Short-term or long-term)
5. What is your current credit balance?

---
