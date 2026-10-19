# 📐 AI-Powered Class 10 Maths Exam Paper Slicer & Google Drive Sorter

An automated serverless pipeline built with **Python**, **Google Colab**, and the **Google Gemini Vision API** to help educators instantly crop and sort mixed school exam papers into structured chapter-wise Google Drive folders.

---

## 🚀 The Problem
School question papers contain a mix of questions from multiple chapters. Manually taking a photo, cropping every single question, and filing them into 14+ chapter folders (`Trigonometry`, `Triangles`, `Polynomials`, etc.) plus special assessment folders (`MCQs`, `Case Study`, `Assertion Reason`) takes hours of repetitive manual labor.

## 🛠️ The Solution
This automated workflow reduces hours of sorting into a single click:
1. **Inbox Trigger:** Upload a photo of any school exam paper to a designated Google Drive inbox folder.
2. **AI Vision Classification:** The script sends the image to the **Gemini 2.5 Flash API**, which detects the bounding box coordinates (`[ymin, xmin, ymax, xmax]`) of every individual question (including geometry diagrams) and classifies it by chapter/question type.
3. **Auto-Cropping & Filing:** Using Python (`PIL` and `Pydantic`), the script slices the master image into high-resolution individual question cards and saves them directly into their respective Google Drive folders.

---

## 🧰 Tech Stack
- **Google Gemini Vision API:** Computer vision object detection & curriculum syllabus classification.
- **Python (PIL, Pydantic):** Structured JSON outputs and precision image cropping with dynamic safety margins.
- **Google Drive API / Google Colab:** 100% cloud-based execution (zero local device storage or RAM required).

---

## ⚙️ How to Use
1. Open the `.ipynb` notebook inside **Google Colab**.
2. Paste your free Gemini API Key (obtained from [Google AI Studio](https://aistudio.google.com/)).
3. Mount your Google Drive and point the folder paths to your Maths repository.
4. Run the cells and drop your exam paper photos into `00_Inbox`!
