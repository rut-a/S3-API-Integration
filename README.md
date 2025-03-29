# Integrating an External API with Amazon S3 Using Python  

## Description  
This project fetches data from an external API, saves it as a JSON file locally, and uploads it to an Amazon S3 bucket using Python and `boto3`.  

## Features  
✅ Fetches real-time data from an external API  
✅ Saves API response as a JSON file  
✅ Uploads the JSON file to an S3 bucket  
✅ Uses environment variables for security  

## Technologies Used  
- **Python** – Core programming language  
- **Boto3** – AWS SDK for S3 integration  
- **Requests** – Fetching data from an external API  
- **Dotenv** – Loading environment variables  

## Prerequisites  
Ensure you have the following installed:  
✅ **Python 3.x**  
✅ **AWS account** with S3 bucket access  
✅ **IAM credentials** with **S3 write permissions**  

## Installation & Setup  

### 1️⃣ Clone this repository:  
```sh
git clone https://github.com/rut-a/S3-API-Integration.git
cd api-to-s3
```
  
### 2️⃣ Install dependencies:  
```sh
pip install -r requirements.txt
```

### 3️⃣ Set up environment variables:  
Create a `.env` file and add:  
```env
AWS_ACCESS_KEY=your-access-key
AWS_SECRET_KEY=your-secret-key
AWS_REGION=your-region
BUCKET_NAME=your-bucket-name
CURRENCY_API_KEY=your-currency-api-key
```

### 4️⃣ Modify `API_URL` in `script.py` with your API endpoint.  

---

## 📜 Usage  
Run the script with:  
```sh
python script.py
```

### What Happens?  
✔ Fetches data from an API  
✔ Saves it locally as a JSON file  
✔ Uploads the file to an S3 bucket  

## Error Handling  
- **Failed API Request?**  
  → Ensure `CURRENCY_API_KEY` is correct and active.  
  → Check your internet connection and API availability.  

- **S3 Upload Fails?**  
  → Verify `BUCKET_NAME` exists and you have correct S3 permissions.  
  → Ensure `AWS_ACCESS_KEY`, `AWS_SECRET_KEY`, and `AWS_REGION` are correctly set in `.env`.  
  → Check if the IAM policy allows `s3:PutObject`.  

- **File Not Uploading?**  
  → Run the script with `print(rates)` before uploading to debug API response.  
  → Add exception handling to catch specific upload errors.  


## Future Improvements  
✅ Add support for multiple file formats (CSV, XML)  
✅ Automate uploads using AWS Lambda  
