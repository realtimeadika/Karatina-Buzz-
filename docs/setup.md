# Setup Guide

## Prerequisites

Before you begin, ensure you have the following installed:

- **Git** (v2.0 or above)
- **Node.js** (v14.x or above)
- **npm** (v6.x or above)
- **Firebase CLI** (latest version)
- **MongoDB** (optional, for local testing)

## Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/realtimeadika/Karatina-Buzz-.git
cd Karatina-Buzz-
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Setup Firebase

```bash
npm install -g firebase-tools
firebase login
firebase init
```

Follow the prompts to initialize Firebase in your project.

### 4. Configure Environment Variables

Create a `.env` file in the root directory:

```bash
CONSUMER_KEY=your_m_pesa_consumer_key
CONSUMER_SECRET=your_m_pesa_consumer_secret
BUSINESS_SHORT_CODE=174379
PASSKEY=your_m_pesa_passkey
CALLBACK_URL=https://yourdomain.com/callback
WHATSAPP_TOKEN=your_whatsapp_token
FIREBASE_API_KEY=your_firebase_api_key
```

### 5. Deploy to Firebase

```bash
firebase deploy --only functions
```

### 6. Start Development Server

```bash
npm run dev
```

The application will be available at `http://localhost:5000`

## Project Structure

```
Karatina-Buzz-/
├── functions/              # Firebase Cloud Functions
├── flutter_app/            # Flutter mobile application
├── admin_dashboard/        # React admin dashboard
├── docs/                   # Documentation files
├── .env.example            # Environment variables template
├── package.json            # Project dependencies
└── README.md               # Project overview
```

## Running Tests

```bash
npm test
```

## Troubleshooting

### Firebase Connection Issues
- Ensure Firebase CLI is logged in: `firebase login`
- Check your `.env` file for correct credentials
- Verify Firebase project ID in `firebase.json`

### M-Pesa API Errors
- Check Consumer Key and Secret
- Verify Business Short Code is correct
- Ensure Callback URL is accessible

### WhatsApp Integration Issues
- Verify WhatsApp token is valid
- Check WhatsApp Cloud API rate limits
- Ensure webhook URL is properly configured

## Next Steps

1. Review the [Architecture](architecture.md) documentation
2. Check the [Contributing Guidelines](../CONTRIBUTING.md)
3. Explore the Firebase dashboard
4. Set up your M-Pesa Daraja account

---

**Last Updated**: April 20, 2026