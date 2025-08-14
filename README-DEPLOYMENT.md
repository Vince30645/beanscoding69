# BeansCoding - Environment Variable Version

This version uses environment variables to securely store API keys.

## Setup Instructions

### 1. Environment Variables
Create a `.env.local` file in the root directory:
```
GROQ_API_KEY=your_groq_api_key_here
```

### 2. Local Development
```bash
npm install
npm run dev
```

### 3. Vercel Deployment
1. Push this folder to GitHub
2. Connect to Vercel
3. Add environment variable in Vercel dashboard:
   - Go to Project Settings → Environment Variables
   - Add: `GROQ_API_KEY` = `your_actual_api_key`
4. Redeploy

## File Structure
- `api/chat.js` - Serverless function that handles API calls
- `index2.html` - Updated frontend that calls the serverless function
- `.env.example` - Template for environment variables

## Security Benefits
- ✅ API key is hidden from client-side code
- ✅ API key is only accessible server-side
- ✅ No exposed secrets in GitHub repository
- ✅ Safe for production deployment