# Armenian handwriting text recognition system
<i>Look more about the project in the <b>presentation</b> in Armenian.</i>

<b>Steps for solving the problem։</b>
1. Find individual symbols (in this case, letters) on the picture.
2. Put the found symbol into the rectangle and separate from the picture.
3. The neural network model is trained on the dataset of the Armenian handwritten letters.
4. The trained model receives a rectangle received in the second paragraph and predicts the letter.

<b>Methods of obtaining individual characters (both methods were implemented in the project):</b>
- OCR system (in project is used the Tesseract system using the Pytesseract module).
- Contour detection.

To build a recognition model of Armenian handwritten letters was used <b>Armenian handwritten letters dataset</b> (<u><b>Mashtots dataset</b></u>).
Mashtots dataset was created in the Basic Research Laboratory of "Automation Systems & Modeling" of the National Polytechnic University of Armenia. 
Further additions and corrections were made at the Science and Technology Foundation of Armenia (FAST).

Dataset contains an average of **887** images from each uppercase and lowercase letters.
In the total number, the dataset contains **68280** images (size of image - **64x64x1**).

To clean the obtained rectangles from extra points or signs and leave only the letter on the image, the <b><u>DBSCAN</u> clustering model</b> was used.
