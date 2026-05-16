# Free Fire Like API  

A simple API for **Send Like to Garena Free Fire Accounts**  
Built with **Flask** for lightweight, fast, and reliable performance.

# ⚠️IMPORTANT
Make Your Repo private! Otherwise, your guest ID password may be stolen
---

## 🌟 Features
- Decode **Free Fire JWT tokens** instantly to find player region.
- Fetch **player details** and automatically manage `lock_region`.
- Automatically send requested Likes using dynamically updated tokens.
- Fully **asynchronous** internal requests for maximum speed.
- Easy deployment on **Vercel** (serverless, free hosting)  

---

## 🚀 Deploy to Vercel  

Click below to deploy directly to **Vercel**:  

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/itz-paglu/Free-Fire-Like-API)  

### After Deploying
1. Your project will automatically rely on `uidpass.json` and `tokens.json`.
2. Ensure you have run the update script or set up the GitHub Workflow to periodically refresh `tokens.json`.
3. Your Vercel domain (e.g., `https://free-fire-like-api.vercel.app`) is now serving your API endpoints!

✅ Save changes and redeploy if necessary. Your API is now ready!

---

## 🔗 Endpoint Usage

After deploying to Vercel (or running locally), you can hit your API via simple HTTP requests:

**GET** `/like`

**Query Parameters:**
- `uid` (Required): The Free Fire Player ID to send likes to.
- `server_name` (Optional): Force a specific region (e.g., `IND`, `BD`, `BR`). If omitted, it will automatically parse the `lock_region` from your active token!

### Example Request:
```bash
https://your-domain.com/like?uid=123456789
```

### Example Response:
```json
{
  "credit": "https://t.me/paglu_dev",
  "LikesGivenByAPI": 100,
  "LikesafterCommand": 200,
  "LikesbeforeCommand": 100,
  "PlayerNickname": "PlayerName",
  "Region": "ID",
  "UID": 123456789,
  "status": 1
}
```

---
