# API Documentation – Skin Analysis and Hazard Detection

### NOTE:
- All URLs require JSON payloads (Content-Type: application/json).
- Responses are returned in JSON format.

---

## 1. OCR for Ingredient Extraction
**Method:**  
`POST {{base_url}}/ocr`

#### Description:
Uploads an image and extracts text using OCR for further processing

#### Request Parameters
| Parameter       | Type    | Description                 |
|-----------------|---------|-----------------------------|
| file            | Binary  | Image file to process (e.g., JPEG, PNG).                |

### Success Response:
```` json
{
  "text": "Extracted and processed ingredient text"
}
````

### Error Response:
#### 400 Bad Request:
```` json
{
  "error": "No file part"
}
````

### Error Response:
#### 500 Internal Server Error:
```` json
{
  "error": "Detailed error message"
}
````
---
## 2. Predict Skin Type and Check Hazardous Materials
**Method:**
`POST {{base_url}}/predict`
**Description:**
Processes input text to detect hazardous materials and predict skin compatibility.









