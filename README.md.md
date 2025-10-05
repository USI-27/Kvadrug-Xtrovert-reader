\#  Kvadrug Extrovert Font OCR + LLM Decryption (WIP)



This project explores the creation of a **custom neural network OCR system** capable of recognizing characters from the **Kvadrug Extrovert font** family and performing **automated text decryption** with the help of a **Large Language Model (LLM)**.



> ⚙️ **Status:** Prototype / In Progress  

> The project demonstrates the full pipeline conceptually and partially functions end-to-end, but requires additional tuning and optimization for production use.



---



\## 🔍 Overview



The goal of this project is to build an **end-to-end AI pipeline** that:

1\. Recognizes Kvadrug Extrovert font characters from images.

2\. Uses an OCR-based algorithm to segment and identify letters.

3\. Integrates an \*\*LLM\*\* to post-process or decrypt the recognized text intelligently.



---



\##  Technical Details



\### 🏗️ Dataset

\- **Custom dataset** manually created with more than **500 images per class** (each letter as a class).

\- Includes all uppercase English alphabets (A–Z).

\- Each image labeled and preprocessed for CNN training.



\### 🤖 Model

\- Implemented a Convolutional Neural Network (CNN) for character classification.

\- Achieved 95%+ accuracy on validation data.

\- Techniques used:

&nbsp; - Data augmentation (rotation, scaling, noise)

&nbsp; - Batch normalization and dropout

&nbsp; - Adam optimizer with categorical cross-entropy loss



\### 🔡 OCR Pipeline

\- Preprocessing using \*\*OpenCV\*\* for binarization, contour detection, and segmentation.

\- Character-level prediction using the trained CNN model.

\- Sequential reconstruction of recognized characters into text.



\### 🧩 LLM Integration

\- After OCR decoding, text is passed through an LLM (e.g., google Gemini) for:

&nbsp; - Context-based correction

&nbsp; - Decryption / normalization of encoded outputs

\- This step allows the system to intelligently handle ambiguities or stylized variations.



---



\## 🚀 Current Capabilities



✅ CNN trained on custom dataset (95%+ accuracy)  

✅ OCR-based segmentation and prediction  

✅ LLM-assisted text refinement  

⚠️ Model still requires improved robustness to noise and real-world inputs  

⚠️ Some pipeline modules are experimental / under refinement  



---



\## 🧪 Example Workflow (Conceptual)

the sentence encoder file you can use it encode any english text this script it will give u a png image of your text at last 



then you can pass that image into the sentence encoder and it will decode it back using the model and it used the predict.py and it at the end to add punctuation and context it uses the post process.py at last to use the gemini 1.5 flash to refine it .





