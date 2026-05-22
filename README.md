# 🏋️ FitFuelHub — BMI Calculator & Health Analytics

> A browser-based health analytics tool that calculates BMI, tracks trends over time, and delivers personalized diet and fitness guidance.

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Chart.js](https://img.shields.io/badge/Chart.js-Trend%20Analytics-FF6384?style=flat-square)](https://www.chartjs.org/)

---

## 🎯 Project Overview

FitFuelHub is a client-side health analytics application that goes beyond a simple BMI calculator. It persists your history in the browser, charts your BMI trend over time, and serves personalised diet plan PDFs based on your age group and weight category — all with zero backend required.

---

## ✨ Features

### Core Calculator
- Calculates BMI from height and weight inputs
- Classifies result: Underweight · Normal · Overweight · Obese
- Visual BMI range chart with colour-coded zones

### 📈 BMI Trend Analytics *(Analytics Enhancement)*
- Logs every BMI reading with a timestamp to browser localStorage
- Renders an interactive **Chart.js line chart** showing your BMI history
- Highlights WHO threshold lines (18.5 and 25) directly on the chart
- Tracks trend direction: improving / stable / worsening
- Clear history button to reset tracking data

### 🥗 Personalised Diet Plans
- Age-group segmentation: 18–25 · 25–35 · 35–45 · 45+
- Separate diet PDFs for Underweight and Overweight per group
- Downloadable plans for offline use

### 🔐 User Login
- Simple login page with session-based access control
- Protects the calculator and diet resources

---

## 📁 Project Structure

```
BMI_Calculator/
├── index.html            # Main BMI calculator with trend chart
├── script.js             # BMI logic, localStorage history, Chart.js rendering
├── style.css             # Main styles
├── login.html            # Login page
├── login.css             # Login styles
├── diet.html             # Diet plan selection page
├── diet.css              # Diet page styles
├── [age-group]-[status].pdf  # Personalised diet plan PDFs (8 files)
└── README.md
```

---

## 🚀 Getting Started

No installation required. All logic runs in the browser.

```bash
# Clone the repository
git clone https://github.com/Yohangala/BMI_Calculator.git
cd BMI_Calculator

# Open in browser
open index.html
# Or just double-click index.html in your file explorer
```

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| Structure | HTML5 |
| Styling | CSS3 |
| Logic | Vanilla JavaScript (ES6+) |
| Trend Charts | Chart.js |
| Data Persistence | Browser localStorage |
| Diet Resources | PDF files (age + weight category) |

---

## 📊 Analytics Design

The BMI tracker stores readings as a JSON array in `localStorage`:

```json
[
  { "date": "2024-01-15", "bmi": 24.3, "category": "Normal" },
  { "date": "2024-02-01", "bmi": 23.8, "category": "Normal" }
]
```

Chart.js renders this as a time-series line chart with reference lines at BMI 18.5 (Underweight threshold) and 25 (Overweight threshold), making health trends immediately visible.

---

## 🔮 Future Improvements

- [ ] Export BMI history as CSV for external analysis
- [ ] Multi-user profiles with separate history per user
- [ ] Integration with a Python/Flask backend for cloud-synced history
- [ ] Calorie intake tracker linked to diet plans
- [ ] Power BI embed for population-level BMI analytics

---

## 👤 Author

**Yohan Gala** · [github.com/Yohangala](https://github.com/Yohangala) · [yohangala2004@gmail.com](mailto:yohangala2004@gmail.com)

*Computer Engineering · K. J. Somaiya Institute of Technology · Mumbai*
