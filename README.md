# EchoEntry — Speech-to-Digits API

Convert spoken numbers into clean structured digits.

Unlike generic speech-to-text models, EchoEntry is optimized specifically for:
✔ Phone numbers  
✔ Tracking IDs  
✔ Invoice values  
✔ Spoken numeric data pipelines

---

## 🚀 Example

### Request

POST https://api.echoentry.ai/v1/transcribe-url

```json
{
  "audio_url": "https://echoentry.ai/test_audio.wav"
}
Response
{
  "success": true,
  "digits": "418",
  "raw_text": "four one eight"
}
🎯 Why Not Use Regular Whisper?
General ASR:

Returns messy text

Requires parsing logic

Fails on structured numbers

EchoEntry:

Extracts digits directly

No regex needed

Built for automation workflows

🔧 Use Cases
• Voice → CRM entry
• Logistics call automation
• Voice-driven data entry
• Call center transcription pipelines
• Financial input capture

📦 RapidAPI Listing
Available on RapidAPI:
👉 https://rapidapi.com/

Search: EchoEntry

🧪 Try Instantly (cURL)
curl -X POST https://api.echoentry.ai/v1/transcribe-url \
  -H "Content-Type: application/json" \
  -H "X-Api-Key: YOUR_KEY" \
  -d '{"audio_url":"https://echoentry.ai/test_audio.wav"}'
⚙️ Status
This is an experimental precision ASR tool focused on numeric extraction.

Feedback welcome.


---

# ✅ Step 2 — Add “Topics” (This Is HUGE For Discovery)

On the repo page → click ⚙️ (About section) → add topics:

speech-recognition
whisper
speech-to-text
voice-api
asr
fastapi
ai-api
audio-processing
automation
machine-learning


This is how GitHub SEO actually works.

---

# ✅ Step 3 — Add ONE Example Folder (Developers Trust Examples)

Create folder:

/examples


Add file:

python_example.py


Content:

```python
import requests

url = "https://api.echoentry.ai/v1/transcribe-url"

payload = {
    "audio_url": "https://echoentry.ai/test_audio.wav"
}

headers = {
    "Content-Type": "application/json",
    "X-Api-Key": "YOUR_API_KEY"
}

response = requests.post(url, json=payload, headers=headers)

print(response.json())
