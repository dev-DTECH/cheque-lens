# Cheque Lens
> Automated Cheque Processing and Fraud Detection using Deep Learning

## RBI's "CTS-2010 Standard" for Cheque Forms
!["CTS-2010 Standard" for Cheque Forms](https://github.com/dev-DTECH/cheque-lens/raw/main/idea/img/CTS-10.png)

---

## Bank of Baroda - Automated Cheque Processing Hackathon

### Problem Statement
> Bank handles large volumes of cheques in the clearing process. The process involves many technical verifications including signature verification. Some of these steps are manual and require human intervention to complete the process. The current process requires the high human capital deployment and longer processing time.

### Goals
1. **Detecting Potential Frauds:** Automate the verification of security features given by RBI’s
["CTS-2010 Standard" for Cheque Forms – Specifications](https://rbidocs.rbi.org.in/rdocs/content/PDFs/SCFR220210.pdf) using different Neural Network
techniques and image processing.
2. **Signature Verification:** Extract and match the signature in the cheque with the signature
in the bank database. Also check for signature forgery using convolutional neural
network.
3. **Automatic Data Entry:** Extract the data from the cheque using [Google’s Tesseract-OCR
Engine](https://github.com/tesseract-ocr/tesseract)(configured for Multiple Languages) and entry the data to process the transaction.
4. **Optimise the Neural Network models:** Use different optimisation techniques to make the
verification process faster with high accuracy.
5. **Minimize Human effort:** Minimize human effort by minimizing false positive of fraud
detection and signation verification. With accurate OCR.

### [Flow Chart](https://github.com/dev-DTECH/cheque-lens/raw/main/idea/img/cheque-flow.jpg)

### Implementation Plan
- **Scan the cheque:** Make a fontend in python that can take a picture from camera/scanner
attached to the computer or import from file with support to import a large number of
images together.
- **UV Light Check:** UV light check will be done using a external device with human
intervention or automated with some IOT device and should be matched with bank logo
with the help of neural networks.
- **Extract different parts of Cheque:** Extract different parts of cheque using RBI’s
["CTS-2010 Standard" for Cheque Forms – Specifications](https://rbidocs.rbi.org.in/rdocs/content/PDFs/SCFR220210.pdf) for verification.
Match Signature from bank database: Match the signature from cheque with signature
from bank database. Also check for forge signature using neural networks.
Check the Pantograph: The pantograph will be checked for words like “VOID” / “COPY”
- **Check for clutter free background:** The background will be check for clutter free
background(the writings in background should be distin) using canny edge detection
algorithm.
- **Check for watermark:** The cheque should be checked for “CTS-INDIA” watermark.
- **Validating the cheque:** If all checks passes then proceed to next step else detection of
potential frauds.
- **Check for overwriting/correction:** The writing should be checked for overwriting/correct
using neural networks if found bounce the cheque.
- **Data Entry:** After all the verification is done the details of the cheque will be extracted
using [Google’s Tesseract-OCR
Engine](https://github.com/tesseract-ocr/tesseract)(configured for Multiple Languages) and start
transaction process.
