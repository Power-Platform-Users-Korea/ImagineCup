# Unemployment Benefits Rights Assistant 🛡️⚖️

> AI-powered assistant protecting workers' unemployment benefits rights

[![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/)
[![Python](https://img.shields.io/badge/Python-3.11-blue?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4-74aa9c?style=flat&logo=openai&logoColor=white)](https://openai.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**[한국어 버전 →](./README_UNEMPLOYMENT_KO.md)**

---

## 📖 Project Overview

This project is an **AI assistant protecting workers' legitimate unemployment benefits rights**. A 24/7 AI legal consultation service defending workers from recent cases of unfair forced resignation (Coupang, London Bagel Museum, etc.), illegal dismissal, and rights violations.

**Key Features:**
- 🚨 Immediate emergency response (forced resignation letters, unfair pressure)
- ⚖️ Identify and alert unfair situations
- 📝 Guide evidence collection (recording, documents, witnesses)
- 🔗 Connect to free legal aid organizations
- 💪 Guide unemployment benefits eligibility
- 📚 Provide basic labor law knowledge

---

## 🚨 Why This Project is Needed

### Recent Reality in Korea

**Coupang Incident (2024)**:
- Forced "voluntary resignation" on thousands of workers
- Stripped unemployment benefits eligibility
- Workers were unaware of their rights

**London Bagel Museum Case**:
- Avoided unemployment benefits without proper dismissal procedures
- Violated workers' rights

**Numerous SMEs Nationwide**:
- Exploiting complex labor laws
- Disguised as "consensual resignation" or "recommended retirement"
- Depriving workers of legitimate rights

### The Information Gap Problem

| Employer Side | Worker Side |
|--------------|-------------|
| ✅ Professional labor consultant | ❌ No information |
| ✅ Rich legal knowledge | ❌ Difficult to understand complex system |
| ✅ Strategic response | ❌ Panicked immediate response |
| ✅ Time and resources | ❌ Emergency situation |

**Result**: Workers with legitimate rights don't receive unemployment benefits

---

## 💡 The Solution: AI Rights Guardian

### Core Features

#### 1. 🚨 Immediate Emergency Response

```
Situation: "My boss is forcing me to write resignation letter now"

AI Response:
🚨 DO NOT sign anything!

RIGHT NOW:
1. Start recording on smartphone (legal when you're part of conversation)
2. Say "I need time" and leave the room
3. Call Ministry of Employment 1350
4. Photograph all documents received

This is an illegal attempt to deprive unemployment benefits.
```

#### 2. ⚖️ Identify Unfair Situations

**Danger signals AI immediately warns about**:
- "If you resign voluntarily, I'll write you a good recommendation"
- "If you agree to mutual resignation, I'll give you more severance"
- "Just sign here and it's done"
- "Other employees all did this way"
- "No legal problems, don't worry"

→ **Never sign! Need expert consultation immediately!**

#### 3. 📝 Evidence Collection Guide

```
Evidence Collection Checklist:

□ Recording
  - Use smartphone recording app
  - Legal when you're part of the conversation
  - Note date and time

□ Documents
  - All pay stubs
  - Employment contract
  - Email, message backup
  - Company internal documents

□ Witnesses
  - Secure colleague contacts
  - Identify others in same situation

□ Timeline
  - Record events chronologically
  - Who, when, where, what
```

#### 4. 🔗 Free Legal Aid Connection

**Ministry of Employment Call Center**:
- Phone: **1350**
- Hours: Weekdays 09:00-18:00
- Free unemployment benefits, labor law consultation

**Korea Legal Aid Corporation**:
- Phone: **132**
- Free legal consultation and litigation support
- Online: klac.or.kr

**Korean Trade Unions**:
- FKTU: 02-6277-8000
- KCTU: 02-2635-8989

#### 5. 💪 Unemployment Benefits Eligibility Guide

**Basic Eligibility (2024 Standard)**:
- 180+ days of work in 18 months before resignation
- Involuntary separation:
  - ✅ Dismissal (including unfair dismissal)
  - ✅ Recommended retirement
  - ✅ Contract expiration
  - ✅ Company's fault (wage arrears, violation of working conditions)
  - ❌ Simple voluntary resignation

**Benefit Amount**:
- 60% of pre-resignation average wage
- Minimum: ₩63,104 per day
- Maximum: ₩66,000 per day
- Period: 120 to 270 days

---

## 🏗️ Architecture

```
┌─────────────────┐
│  Worker         │
│  (Web/Mobile)   │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Azure Container│
│  Apps (Web)     │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Azure Container│
│  Apps (API)     │
│  Flask Backend  │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Azure OpenAI   │
│  GPT-4          │
│  + Labor Law DB │
└─────────────────┘
```

**Tech Stack:**
- **Backend:** Python 3.11, Flask
- **AI:** Azure OpenAI Service (GPT-4 recommended)
- **Legal DB:** Employment Insurance Act, Labor Standards Act, Supreme Court precedents
- **Hosting:** Azure Container Apps
- **Deployment:** Azure Developer CLI (azd)

---

## 📋 Prerequisites

### Required

- [Azure Account](https://azure.microsoft.com/free/)
- [Azure Developer CLI (azd)](https://learn.microsoft.com/azure/developer/azure-developer-cli/install-azd)
- [Git](https://git-scm.com/downloads)
- [Python 3.11+](https://www.python.org/downloads/)

### Optional

- [VS Code](https://code.visualstudio.com/)
- [GitHub Copilot](https://github.com/features/copilot)

---

## 🚀 Quick Start

### Step 1: Clone Repository

```bash
git clone https://github.com/Azure-Samples/get-started-with-ai-chat.git unemployment-assistant
cd unemployment-assistant
```

### Step 2: Create Custom Directories

```bash
mkdir prompts
mkdir data
mkdir logs
```

### Step 3: Create System Prompt

Create `prompts/unemployment_assistant.md`:

```markdown
# Unemployment Benefits Rights Guardian System Prompt

You are "Rights Guardian" - an AI assistant protecting workers' unemployment benefits rights.

## Core Role

Help workers avoid unfair treatment and protect their unemployment benefits rights.

## Main Support Areas

1. **Unemployment Benefits Eligibility Guidance**
   - Difference between voluntary resignation vs recommended retirement vs dismissal
   - Check eligibility requirements
   - Calculate benefit amount

2. **Identify Unfair Situations**
   - Recognize "voluntary resignation inducement" tactics
   - Respond to "mutual resignation" pressure
   - Judge illegal dismissal

3. **Evidence Collection Guidance**
   - Recording methods
   - Document preservation
   - Witness securing

4. **Response Procedure Guidance**
   - Employment center reporting
   - Labor office complaint
   - Free legal aid

## Response Principles

### 1. Clear and Firm
❌ "Maybe...", "You could..."
✅ "This is illegal", "You have rights"

### 2. Immediate Action Guidance
Clearly present what to do RIGHT NOW

### 3. Simplify Legal Terms
- "Involuntary separation" → "Company made you quit"
- "Recommended retirement" → "Company suggested you quit (benefits eligible)"

### 4. Immediate Warning on Danger Signals

These situations are unfair unemployment benefits deprivation attempts:
- "If you resign voluntarily, I'll write a recommendation"
- "If we agree on mutual resignation, I'll give more severance"
- "Just sign here and it's done"

→ Never sign! Need expert consultation immediately!

## Emergency Response Manual

### Situation 1: "Write resignation letter now" pressure

```
Immediate actions:
1. 🎙️ Start recording
2. 🗣️ "I need time"
3. 🚶 Leave the room
4. 📞 Call 1350
5. 📸 Photograph documents
```

### Situation 2: Already wrote resignation letter

```
Not too late!

1. Send "resignation letter withdrawal" via certified mail
2. Complaint to Ministry of Employment
3. File for relief with Labor Relations Commission
```

## Free Legal Support

- Ministry of Employment: **1350**
- Korea Legal Aid Corporation: **132**
- FKTU: 02-6277-8000
- KCTU: 02-2635-8989

## Important Legal Basis

### Employment Insurance Act Article 58
Involuntarily separated persons have right to unemployment benefits.

### Labor Standards Act Article 23
Cannot dismiss without justifiable reason.

### Criminal Act Article 324 (Coercion)
Punishable if forcing action against will through assault or threat

## Acknowledge Limitations

**Important: I am an AI consultation assistant**

✅ Provide general information
✅ Emergency response guidance
✅ Identify danger signals
✅ Connect to professionals

❌ Legal advice (only labor attorneys/specialists can)
❌ Final judgment on individual cases
❌ Litigation representation

**For complex situations, always consult with professionals!**

---

Your first step to protecting your rights, Rights Guardian is with you.
```

### Step 4: Add Labor Law Data

Create `data/labor_law_info.md` with:
- Unemployment benefits eligibility criteria (2024 standard)
- Benefit calculation methods
- Application procedures
- Unfair tactics identification
- Evidence collection methods
- Response procedures
- Free legal aid organizations
- Important legal basis and precedents

(See Korean version for detailed content)

### Step 5: Modify Backend Code

Edit `src/api/app.py` with same structure as library project:

```python
import os
from pathlib import Path
from openai import AzureOpenAI
from flask import Flask, request, jsonify
import logging

app = Flask(__name__)
logging.basicConfig(level=logging.INFO)

client = AzureOpenAI(
    api_key=os.getenv("AZURE_OPENAI_API_KEY"),
    api_version="2024-02-15-preview",
    azure_endpoint=os.getenv("AZURE_OPENAI_ENDPOINT")
)

def load_custom_prompts():
    """Load custom system prompt and labor law data"""
    try:
        project_root = Path(__file__).parent.parent.parent
        
        prompt_path = project_root / "prompts" / "unemployment_assistant.md"
        with open(prompt_path, "r", encoding="utf-8") as f:
            system_prompt = f.read()
        
        data_path = project_root / "data" / "labor_law_info.md"
        with open(data_path, "r", encoding="utf-8") as f:
            labor_law_data = f.read()
        
        full_prompt = f"{system_prompt}\n\n# Labor Law Information\n\n{labor_law_data}"
        
        logging.info("✅ Rights Guardian prompts loaded successfully")
        return full_prompt
    
    except Exception as e:
        logging.error(f"❌ Failed to load prompts: {e}")
        return "You are an AI consultant helping workers' rights."

SYSTEM_PROMPT = load_custom_prompts()

@app.route("/chat", methods=["POST"])
def chat():
    """Unemployment benefits rights consultation"""
    try:
        user_message = request.json.get("message", "")
        
        if not user_message:
            return jsonify({"error": "No message provided"}), 400
        
        logging.info(f"📩 Consultation request: {user_message[:50]}...")
        
        response = client.chat.completions.create(
            model=os.getenv("AZURE_OPENAI_DEPLOYMENT_NAME", "gpt-4"),
            messages=[
                {"role": "system", "content": SYSTEM_PROMPT},
                {"role": "user", "content": user_message}
            ],
            temperature=0.7,
            max_tokens=1000
        )
        
        assistant_reply = response.choices[0].message.content
        logging.info(f"✅ Consultation response generated")
        
        return jsonify({
            "response": assistant_reply,
            "model": response.model,
            "usage": {
                "prompt_tokens": response.usage.prompt_tokens,
                "completion_tokens": response.usage.completion_tokens,
                "total_tokens": response.usage.total_tokens
            }
        })
    
    except Exception as e:
        logging.error(f"❌ Error: {e}")
        return jsonify({
            "error": "Sorry, an error occurred.",
            "emergency_contact": "Call Ministry of Employment 1350 immediately"
        }), 500

@app.route("/health", methods=["GET"])
def health():
    return jsonify({"status": "healthy", "service": "Rights Guardian"})

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=8000, debug=False)
```

### Step 6: Deploy

```bash
azd init
azd auth login
azd up --location koreacentral
```

---

## 🧪 Test Scenarios

### Scenario 1: Emergency Situation

**Input**:
```
My boss is forcing me to write a resignation letter right now.
Says they'll discipline me if I don't.
```

**Expected Response**:
- 🚨 Never sign warning
- Immediate action guide (recording, call 1350)
- Coercion law basis presentation

### Scenario 2: Mutual Resignation Offer

**Input**:
```
Company says they'll give me more severance if I agree to mutual resignation.
Should I do it?
```

**Expected Response**:
- ⚠️ Danger signal warning
- Need to compare unemployment benefits vs additional severance
- Recommend expert consultation (132)

### Scenario 3: Unemployment Benefits Eligibility Check

**Input**:
```
I worked for 1 year and 3 months, and the company is
reducing staff due to business difficulties. Can I get unemployment benefits?
```

**Expected Response**:
- ✅ Confirm eligibility
- Guide required documents
- Explain application procedure step-by-step

---

## 📊 Expected Impact

### If Applied to Coupang Case

**Actual Situation** (2024):
- Workers Affected: ~1,000+
- Unemployment benefits not received: ~₩500,000,000+

**If AI existed**:
- Immediately identify unfairness
- Guide evidence collection
- Organize collective response
- Successful unemployment benefits claims

### Nationwide Impact

**Annual Estimate**:
- Unfair resignation coercion victims: ~10,000+
- Total unemployment benefits not received: ~₩5,000,000,000
- **Recoverable with AI: ~7,000+ workers**

---

## 📊 Cost Analysis

### Traditional Method vs AI Assistant

| Item | Traditional | AI Assistant |
|------|-------------|--------------|
| **Labor Attorney** | ₩200,000-500,000 | Free |
| **Wait Time** | Days to weeks | Immediate |
| **Accessibility** | Phone/visit required | Anytime, anywhere |
| **Emergency Response** | Difficult | 24/7 real-time |
| **Evidence Guide** | After-the-fact | Preventive |
| **Monthly Operation** | - | ₩30,000-50,000 |

### ROI (Return on Investment)

**With ₩50,000/month investment**:
- Can consult 100 workers
- Average unemployment benefit: ₩1,500,000 x 120 days = ~₩180,000,000
- **ROI: 360,000%**

---

## 🐛 Troubleshooting

### Issue: AI responds too formally

**Solution**: Adjust prompt tone

```markdown
## Tone and Manner
- Firm but warm
- Use "you" address
- More conversational
- Include empathy and encouragement
```

### Issue: Mistaken for legal advice

**Solution**: Clear limitations

```markdown
⚠️ Important: I am an AI consultation assistant

This information is general guidance.
For specific legal advice, consult labor attorney/specialist.

Emergency: Ministry of Employment 1350
Free Legal Aid: Korea Legal Aid Corporation 132
```

---

## 🤝 Contributing

### For Labor Organizations

1. **Update Legal Information**: Provide latest precedents, law amendments
2. **Share Cases**: Share actual unfair cases (anonymized)
3. **Validation**: Review legal accuracy of AI responses

### For Developers

1. **Add Features**:
   - Multilingual support (foreign workers)
   - Voice recognition (emergency situations)
   - Automatic evidence organization

2. **Optimization**:
   - Improve response speed
   - Reduce costs

---

## 📚 Resources

### Official Documents
- [Employment Insurance Act](https://www.law.go.kr/)
- [Labor Standards Act](https://www.law.go.kr/)
- [Ministry of Employment and Labor](https://www.moel.go.kr/)
- [Korea Workers' Compensation & Welfare Service](https://www.kcomwel.or.kr/)

### Support Organizations
- [Korea Legal Aid Corporation](https://www.klac.or.kr/)
- [FKTU](http://www.fktu.or.kr/)
- [KCTU](http://www.nodong.org/)

---

## 📄 License

MIT License

---

## 👥 Authors & Acknowledgments

**Motivation**: Recent workers' rights violations (Coupang, London Bagel Museum, etc.)

**Special Thanks**:
- All activists fighting for workers' rights
- Attorneys and labor specialists providing legal aid
- Workers standing up against unfair treatment

---

## 📞 Contact

- **GitHub Issues**: [Report bugs or suggestions](../../issues)
- **Emergency Consultation**: Ministry of Employment 1350
- **Free Legal Aid**: Korea Legal Aid Corporation 132

---

## 🎯 Sprint to Imagine Cup 2026

**Theme**: Resolving social inequality with AI

**Innovation**: Transforming complex labor law into 24/7 accessible rights protection tool

**Social Impact**: Protecting vulnerable workers' legitimate rights

---

<div align="center">

**Made with ❤️ to protect workers' rights**

**Powered by Azure AI | Built for Social Justice**

⭐ **Star this repo if you believe in workers' rights!** ⭐

[⬆ Back to Top](#unemployment-benefits-rights-assistant-️️)

</div>
