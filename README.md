https://auracycle.onrender.com/ (this id for live demo)
# 🌸 AuraCycle — Smart Period Tracking & PCOD Risk Prediction

<div align="center">



**A smart period tracking and PCOD risk prediction system — built and deployed by Team Vibecoder.**

🔗 [Live Demo → auracycle.onrender.com](https://auracycle.onrender.com)

</div>

---

## 👩‍💻 Team Vibecoder

| Name | Role |
|------|------|
| **Sneha** | Frontend Developer |
| **Chinky** | Solution Design + Demo |
| **Vishal** | Backend / ML Support |

> GL Bajaj Institute of Technology & ABES Engineering College

---

## ❗ The problem

> **1 in 5 young women in India** has PCOD or PCOS.  
> **70% of these cases go undiagnosed** — with an average diagnosis delay of **2 years**.

**Why do existing apps fail?**
- They assume a fixed 28-day cycle — which breaks the moment a woman's cycle is irregular
- They don't analyze symptoms like acne, mood swings, or weight gain **together**
- There's **zero connection** between the data a woman logs and the doctor who needs that data to diagnose her

---

## 💡 Our Solution — AuraCycle

AuraCycle is not just a tracker. It's a smart health system that:

- Logs cycle dates, flow intensity, and **15+ symptoms** (cramps, acne, hair loss, mood changes, and more)
- Runs an **ML model** to generate a personalized **PCOD Risk Score** — Low, Medium, or High
- Shows **cycle predictions**, fertility window, and symptom trend charts
- Sends **smart alerts** when something looks unusual — like an unusually long cycle
- Gives women a **health report** they can share directly with their doctor

---

## ✨ Features

### 📅 Cycle tracking
- Log period start/end dates and flow intensity
- Supports **irregular cycles** — not limited to 28-day assumptions
- Track **15+ symptoms**: cramps, acne, hair loss, mood swings, weight changes, and more

### 🤖 PCOD Risk Score (ML-Powered)
- Trained ML model using **scikit-learn**
- Uses a saved model file with scaler and label encoder for proper preprocessing
- Outputs **Low / Medium / High** risk based on user's actual inputs — not generic rules

### 📊 Smart Dashboard
- Cycle prediction & next period date
- Fertility window estimation
- Symptom trend charts over time
- Smart alerts for unusual patterns

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | HTML, CSS, JavaScript |
| **Backend** | Python · Flask |
| **Database** | MongoDB |
| **ML Model** | scikit-learn (trained model + scaler + label encoder) |
| **Deployment** | Render (auracycle.onrender.com) |

---

## 🏗️ Project Structure

```
auracycle/
│
├── frontend/               # HTML, CSS, JS files
│   ├── index.html
│   ├── dashboard.html
│   └── assets/
│
├── backend/                # Flask API
│   ├── app.py              # Main Flask app
│   ├── routes/
│   │   ├── cycle.py        # Cycle logging routes
│   │   └── predict.py      # PCOD prediction route
│   └── db.py               # MongoDB connection
│
├── ml_model/               # ML files
│   ├── model.pkl           # Trained scikit-learn model
│   ├── scaler.pkl          # Feature scaler
│   └── label_encoder.pkl   # Label encoder
│
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
```
Python 3.9+
MongoDB (local or Atlas)
pip
```

### Installation

```bash
# 1. Clone the repo
git clone https://github.com/your-username/auracycle.git
cd auracycle

# 2. Install dependencies
pip install -r requirements.txt

# 3. Set environment variables
cp .env.example .env
# Add your MongoDB URI

# 4. Run the Flask app
python app.py
```

### Environment Variables

```env
MONGO_URI=mongodb+srv://your_user:your_password@cluster.mongodb.net/auracycle
SECRET_KEY=your_secret_key
```

---

## 🤖 ML Model — How It Works

- **Algorithm:** scikit-learn classifier (trained on PCOD symptom data)
- **Input features:** cycle irregularity, flow intensity, acne, hair loss, mood swings, weight gain, and 9 more symptoms
- **Preprocessing:** StandardScaler + LabelEncoder saved as `.pkl` files
- **Output:** Risk label — `Low`, `Medium`, or `High`
- **Why it's different:** Risk is based on the **user's own symptom combination**, not generic age/BMI rules

```python
# Prediction flow (simplified)
features = preprocess(user_input, scaler, label_encoder)
risk = model.predict(features)
# → "High", "Medium", or "Low"
```

---

## 📈 Impact

| Stat | Value |
|------|-------|
| Women with PCOD in India | 1 in 5 |
| Go undiagnosed | 70% |
| Avg diagnosis delay | 2 years |
| Symptoms tracked by AuraCycle | 15+ |
| Live deployment | ✅ auracycle.onrender.com |

---

## 🔒 Privacy

- No health data is shared with third parties
- All cycle and symptom data is stored securely in MongoDB
- Users can delete their data at any time

---

## 📄 License

MIT License — feel free to fork and contribute!

---

<div align="center">

**Built with 💜 by Team Vibecoder**  
*GL Bajaj Institute of Technology & ABES Engineering College*

⭐ Star this repo if you believe every woman deserves early diagnosis!

</div>
