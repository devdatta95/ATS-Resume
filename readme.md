# Resume Tracking using Gemini Model

## Objective
This project leverages Google's **Gemini model** to extract text data from resumes in PDF format and compare it with a given job description (JD). By analyzing key qualifications, skills, and experience, the system provides insights into the compatibility between a resume and a job posting, aiding recruiters in quick and efficient candidate screening.

## Features
- **Extract Resume Data:** Uses OCR and text extraction techniques to retrieve structured information from resumes.
- **JD Matching:** Compares extracted data with a job description to analyze the match percentage.
- **PDF to Image/Text Processing:** Supports both PDF-to-image-based extraction and direct PDF-to-text processing.
- **Streamlit Web Interface:** Provides a user-friendly interface for recruiters to upload resumes and job descriptions.
- **Google Gemini API Integration:** Enhances text analysis for resume-JD comparison.

## Project Setup

### 1. Get Google API Key
To use the **Google Gemini API**, obtain your API key from the following link:
- [Google API Key](https://aistudio.google.com/app/apikey)

### 2. Create a Conda Environment
Run the following command to create a new Conda environment:
```sh
conda create --name resume_tracking python==3.10
```

### 3. Activate the Conda Environment
```sh
conda activate resume_tracking
```

### 4. Install Dependencies
Make sure you install all required dependencies by running:
```sh
pip install -r requirements.txt
```

### 5. Install and Configure Poppler
Poppler is required for PDF processing. Follow these steps to install and configure it correctly:

#### **Download and Install Poppler**
- Visit the official [Poppler for Windows releases](https://github.com/oschwartz10612/poppler-windows/releases).
- Download the latest ZIP file (e.g., `Release-21.11.0-0.zip`).
- Extract the files to a directory, such as `C:\Poppler`.

#### **Add Poppler to System PATH**
1. Open the Start menu, search for **Environment Variables**, and select **Edit the system environment variables**.
2. In the **System Properties** window, click **Environment Variables**.
3. Under **System variables**, locate and select the `Path` variable, then click **Edit**.
4. Click **New** and add the path to the `bin` folder inside the Poppler directory (e.g., `C:\Poppler\bin`).
5. Click **OK** to close all dialogs and apply the changes.

#### **Verify Installation**
Run the following command in the terminal to confirm Poppler is installed:
```sh
pdftoppm -h
```
If the installation was successful, the command will display help information for `pdftoppm`.

## Running the Application
The application supports two modes: **PDF to Image** and **PDF to Text** processing.

### **1. Run the PDF to Image Version**
```sh
streamlit run app.py
```

### **2. Run the PDF to Text Version**
```sh
streamlit run app-modified.py
```

## How It Works
1. **Upload a Resume (PDF format).**
2. **Upload a Job Description (Text or PDF format).**
3. **Processing:**
   - The system extracts text from the resume using OCR or direct PDF parsing.
   - Uses **Google Gemini AI** to compare extracted resume data with the job description.
   - Analyzes key skills, experience, and qualifications.
4. **Result:**
   - Displays a similarity score and highlights matching and missing skills.
   - Provides a recommendation on whether the resume is a good fit for the job.

## Future Enhancements
- **Automated Resume Ranking** based on JD requirements.
- **Skill Gap Analysis** to suggest courses or certifications.
- **Multi-format Support** (Word, PNG, JPG) for resume parsing.
- **Database Integration** for storing and retrieving candidate details.

## Contributing
If you want to improve this project, feel free to submit pull requests or raise issues.

## License
This project is licensed under the MIT License.

---

Now, you can copy and paste this directly into your `README.md` file!

