README: Medical Prescription Information Extraction
🧠 Project Title
Multimodal Model for Structured Information Extraction from Handwritten Medical Prescriptions

📌 Objective
This project aims to extract structured information such as Patient Name, Doctor's Name, Date, Medicines, Dosage, and Frequency from handwritten medical prescriptions using a combination of OCR (Tesseract) and BLIP (Bootstrapped Language-Image Pretraining) models.

🛠️ Technologies Used
Python 3.11+

Google Colab

Tesseract OCR

Transformers (HuggingFace)

BLIP Vision-Language Model

PyTorch

PIL / OpenCV

📁 File Structure
bash
Copy
Edit
├── prescription_sample.png           # Sample handwritten prescription image
├── ocr_blip_extractor.ipynb          # Main Colab notebook
├── README.md                         # Project documentation (this file)
🚀 How to Run the Code
Upload the Prescription Image:

Upload any handwritten prescription as .png or .jpg.

Run the Notebook:

The notebook uses:

Tesseract OCR to extract raw text.

BLIP model to describe the image semantically.

A combination of both outputs to generate a JSON with structured fields.

Output: The model will output:

json
Copy
Edit
{
  "Patient_Name": "patient name",
  "Doctor_Name": "doctor's name",
  "Date": "date",
  "Medicines": ["medicine 1", "medicine 2"],
  "Dosage": ["dosage 1", "dosage 2"],
  "Frequency": ["frequency 1", "frequency 2"],
  "Raw_OCR_Text": "raw text extracted via OCR",
  "Raw_BLIP_Text": "caption extracted from BLIP"
}
📊 Evaluation Strategy
We evaluate the model using:

✅ Ground truth comparisons on manually annotated data

✅ Precision, Recall, F1 Score

✅ Entity-level accuracy for each field

✅ Comparison between OCR-only, BLIP-only, and hybrid approaches

✅ Manual qualitative analysis for edge cases

🧪 Future Improvements
Integrate Named Entity Recognition (NER) for better parsing.

Use language models like GPT-3.5-turbo or fine-tuned T5 for refined formatting.

Improve segmentation of multiple medicine entries.
