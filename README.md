# 📝 Minutes of Meeting Generator

A powerful Streamlit app that uses **Google Gemini AI** to extract and organize handwritten **Minutes of Meeting (MoM)** into a clean, structured table. Just upload a photo of your handwritten notes, and the app will do the rest!

🔗 **Live App**: [minutes-of-meeting.streamlit.app](https://minutes-of-meeting.streamlit.app)

---

## 📌 Features

- ✅ OCR (Optical Character Recognition) for handwritten notes
- ✅ Extracts to-dos, deadlines, and task statuses
- ✅ Detects progress from language and markings (e.g., checkmarks, annotations)
- ✅ Outputs in a clean markdown table format
- ✅ User-friendly interface built with Streamlit

---

## 📸 How It Works

1. **Upload Image**  
   Upload a `.jpg`, `.jpeg`, or `.png` file of your handwritten MoM notes.

2. **Processing**  
   The app uses **Gemini 2.0 Flash** model to analyze the image and extract:
   - Tasks and action items
   - Deadlines (or mark as TBD if not found)
   - Task status: ✅ Completed, 🕒 Pending, ⏳ Not Started
   - Estimated % completion

3. **Output**  
   A structured markdown table is displayed in the app.

---

## 🧠 Output Format

The generated table follows this format:

| Particulars (To-Dos) | Deadline | Status (Completed / Pending / Not Started) | % Completion |
|----------------------|----------|--------------------------------------------|--------------|

---

## 🛠️ Tech Stack

- [Streamlit](https://streamlit.io/) – UI framework
- [Python](https://www.python.org/) – Backend
- [Google Generative AI (Gemini)](https://ai.google/discover/gemini/) – OCR + NLP
- [Pillow (PIL)](https://pillow.readthedocs.io/en/stable/) – Image handling
- [python-dotenv](https://pypi.org/project/python-dotenv/) – Environment variable management

---

## 📂 How to Run Locally

```bash
# 1. Clone the repository
git clone https://github.com/your-username/minutes-of-meeting
cd minutes-of-meeting

# 2. Create virtual environment
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Set up your API key
Create a `.env` file:
GOOGLE_API_KEY=your_google_generative_ai_key

# 5. Run the app
streamlit run app.py
