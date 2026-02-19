# EchoEntry — Speech-to-Digits API

Convert spoken numbers into clean structured digits.

**EchoEntry** is a specialized speech recognition API optimized specifically for **numeric extraction** — not general transcription.

Unlike generic ASR models, EchoEntry is designed for workflows where numbers matter more than sentences.

---

## 🚀 What It Does

✔ Extracts digits directly from spoken audio  
✔ Avoids messy natural language transcripts  
✔ No regex / post-processing required  
✔ Built for automation pipelines

---

## 🎯 Why Not Use Standard Speech-to-Text?

| Generic ASR | EchoEntry |
|-------------|-----------|
Returns full sentences | Returns clean digits only |
Requires parsing | Ready for databases |
High variance | Structured output |
Not optimized for numbers | Built specifically for numbers |

---

## 🔧 Common Use Cases

• Voice → CRM data entry  
• Capturing phone numbers from calls  
• Logistics tracking ID transcription  
• Financial / invoice automation  
• Voice-driven numeric workflows  
• Call-center structured capture systems

---

## 🌐 API Endpoint

POST https://api.echoentry.ai/v1/transcribe-url


---

## 📥 Request Example

```json
{
  "audio_url": "https://echoentry.ai/test_audio.wav"
}
📤 Response Example
{
  "success": true,
  "digits": "418",
  "raw_text": "four one eight"
}
🧪 Try with cURL
curl -X POST https://api.echoentry.ai/v1/transcribe-url \
  -H "Content-Type: application/json" \
  -H "X-Api-Key: YOUR_API_KEY" \
  -d '{"audio_url":"https://echoentry.ai/test_audio.wav"}'
🐍 Python Example
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
📊 Example Output

📦 Available via RapidAPI
EchoEntry is listed on RapidAPI for easy integration and key management.

Search for: EchoEntry

⚙️ Design Philosophy
EchoEntry is intentionally narrow.

It does one job extremely well:

Convert spoken numbers → structured digits.

This makes it suitable for automation systems where traditional speech-to-text creates unnecessary complexity.

🧠 Status
Experimental precision ASR focused on numeric speech extraction.

Feedback and real-world use cases are welcome.
