# GCP-KMS-Key-Management-with-MongoDB

GCP-MongoKeyVault-Manager is a comprehensive solution for managing cryptographic keys using Google Cloud KMS and MongoDB. This project provides functionalities for creating, rotating, encrypting, decrypting, listing, and disabling keys via an intuitive UI in Google Colab.

## Features
**Key Management:** Create, rotate, list, and disable cryptographic keys.

**Encryption & Decryption:** Encrypt and decrypt data using the managed keys.

**Intuitive UI:** User-friendly UI for managing keys and performing encryption/decryption operations.

**Prerequisites**
- Google Cloud Project with KMS API enabled.

- MongoDB instance for storing key metadata.

- Google Colab environment.

Step 1: Install required packages

```bash
!pip install google-cloud-kms pymongo
```
Step 2: Clone the repository
```bash
git clone https://github.com/your-username/GCP-MongoKeyVault-Manager.git

```

Usage
- Initialize the KeyManager
   -- Mount Google Drive:

(python)
```
drive.mount('/content/drive', force_remount=True)
```
Setup Credentials:

(python)
```
setup_credentials()
```
Create Key Management UI:

(python)
```
create_key_management_ui()
```

## Key Management Operations
Create Key: Add a new key to the KMS and store its metadata in MongoDB.

Rotate Key: Create a new version of an existing key.

List Keys: View all managed keys and their metadata.

Encrypt Data: Encrypt plaintext data using a specified key.

Decrypt Data: Decrypt ciphertext data.

Disable Key: Disable a key, making it unusable for new encryption operations.


-------------------------------------------------------------------------------------------------------------


# GCP KMS Key Management with MongoDB (Visual Studio Code)

This application provides a Streamlit web interface for managing encryption keys using Google Cloud Platform's Key Management Service (KMS) with MongoDB as a metadata store.

## Features

- Set up GCP and MongoDB credentials
- Create new encryption keys with custom descriptions and aliases
- List all keys with detailed metadata
- Rotate keys to improve security
- Encrypt and decrypt data using selected keys
- Disable keys when no longer needed

## Installation

1. Clone the repository to your local machine
2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Set up your GCP service account and MongoDB instance

## Usage

1. Run the Streamlit application:

```bash
streamlit run key_management_app.py
```

2. Navigate to `http://localhost:8501` in your web browser
3. First, complete the "Setup" step to configure your GCP and MongoDB credentials
4. Use the sidebar to navigate between different key management operations

## Requirements

- Python 3.7+
- Google Cloud Platform account with KMS enabled
- MongoDB database (local or cloud-based)
- GCP service account with appropriate permissions

## Configuration

The application uses environment variables loaded from a `.env` file:

- `GCP_PROJECT_ID`: Your Google Cloud Project ID
- `GCP_LOCATION_ID`: Location of your KMS resources (default: 'global')
- `GCP_KEY_RING_ID`: ID for the key ring (default: 'vscode-key-ring')
- `GOOGLE_APPLICATION_CREDENTIALS`: Path to your GCP service account JSON file
- `MONGO_URI`: MongoDB connection string (default: 'mongodb://localhost:27017/')
- `MONGO_DB_NAME`: MongoDB database name (default: 'key_management')
- `MONGO_COLLECTION_NAME`: MongoDB collection name (default: 'keys')

You can set these variables either through the setup UI or by creating a `.env` file manually.

## Security Considerations

- Store your GCP service account credentials securely
- Use appropriate IAM permissions for the KMS service
- Ensure your MongoDB instance is properly secured
- Consider using MongoDB Atlas for a managed MongoDB solution with built-in security features

## Development with Visual Studio Code

This application is designed to work well with Visual Studio Code:

1. Open the project folder in VS Code
2. Install the recommended extensions:
   - Python extension
   - MongoDB extension
   - Google Cloud extension
3. Use VS Code's integrated terminal to run the application
4. Debug using VS Code's debugging tools

## License

This project is licensed under the MIT License - see the LICENSE file for details.


**Acknowledgements**
- Google Cloud KMS
- MongoDB
