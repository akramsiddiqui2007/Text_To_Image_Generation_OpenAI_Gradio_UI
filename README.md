# Text_To_Image_Generation_OpenAI_Gradio_UI
Hypothetical scenarios to demonstrate AI's ability to generate images from text prompts using OpenAI and Gradio_UI 

# 🎨 Text-to-Image Generator using OpenAI & Gradio

This project demonstrates how to generate images from text prompts using **OpenAI’s DALL·E (gpt-image-1)** model and a simple **Gradio UI**.  
It is designed to work in both **local Python environments** and **pre-configured cloud labs** (like Simplilearn or Coursera).

---

## 🧠 Project Overview

Users enter a text prompt describing an image, and the app generates the corresponding image using OpenAI’s API.  
If API access or billing is restricted, the app gracefully shows a fallback “mock image” instead of crashing.

---

## ⚙️ Architecture

<img width="1536" height="1024" alt="Architecture" src="https://github.com/user-attachments/assets/ca37ef6e-2c89-4610-9725-ce178a1cdc7d" />


**Components:**
| Component | Description |
|------------|--------------|
| `Gradio` | Provides the web UI for prompt input and image display |
| `OpenAI API` | Generates the image from the user’s prompt |
| `Pillow (PIL)` | Handles image processing and fallback rendering |
| `Requests` | Downloads generated images from URL |
| `Error Handling` | Displays friendly placeholder messages when API errors occur |

---

## 🧩 Key Features

- ✅ Simple **text → image** generation workflow  
- ✅ Works in **lab environments** with built-in OpenAI API keys  
- ✅ Supports **local execution** with custom API keys  
- ✅ Robust **error handling** for billing, quota, or connection issues  
- ✅ Includes **fallback mock image** for demos without internet or credits  

---

## 🚀 How to Run

### 🧪 **In a Pre-Configured Lab**
1. Open the provided Jupyter/VS Code lab.
2. Copy the final lab-compatible code cell into your notebook.
3. Run the cell.
4. Click the generated **Gradio link** (e.g., `https://xxxx.gradio.live`).
5. Type a prompt, e.g.: A futuristic city skyline at sunset
6. View your generated image!

---

### 💻 **Run Locally (With Your Own Key)**
1. Clone or download this repository.
2. Install dependencies:
```bash
pip install -r requirements.txt
```

Add your OpenAI API key in the code:
api_key = "sk-proj-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
client = OpenAI(api_key=api_key)

Run the notebook or Python file.
Open Gradio’s local or public link.

🛡️ Error Handling Summary
| Error Type                               | Message Displayed                        | Resolution        |
| ---------------------------------------- | ---------------------------------------- | ----------------- |
| **No prompt entered**                    | “⚠️ Please enter a valid prompt”         | Enter text        |
| **Insufficient credits / Billing limit** | “⚠️ Your OpenAI API key has no credits.” | Add billing funds |
| **Network or timeout**                   | “⚠️ API unreachable or network issue”    | Check internet    |
| **Unknown structure (lab return)**       | “⚠️ Unexpected response”                 | Auto-handled      |
| **API success**                          | Displays the generated image 🎨          | Enjoy!            |


#### 🧱 Project Structure
```text
text_to_image/
│
├── text_to_image.ipynb      # Main Jupyter notebook
├── README.md                # Project documentation
├── requirements.txt         # Dependencies
└── sample_output/           # (Optional) Generated image examples
```







