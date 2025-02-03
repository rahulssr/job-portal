# Job Portal - Find Your Dream Job

🚀 **Overview**

Job Portal is a modern job-search application built with React and Node.js, allowing users to explore and apply for job opportunities while enabling companies to post and manage job listings.

---

🎨 **Features**

```mermaid
graph TD;
  A[User Authentication] -->|Clerk| B(Secure Login & Signup);
  C[Job Listings] -->|Search & Filter| D(View Jobs);
  E[Job Applications] -->|Apply & Manage| F(Track Progress);
  G[Company Dashboard] -->|Post & Manage| H(Job Listings);
  I[File Uploads] -->|Cloudinary| J(Company Logos & Profiles);
  K[Responsive UI] -->|TailwindCSS| L(Mobile Friendly);
```

---

🎥 **Demo Preview**

(https://job-portal-client-wine-nine.vercel.app/)

---

📊 **Tech Stack**

```mermaid
graph TD;
  React --> TailwindCSS;
  React --> Axios;
  Node.js --> Express;
  Express --> MongoDB;
  Cloudinary --> FileUploads;
  Clerk --> Authentication;
```

---

📦 **Installation**

### Prerequisites
- Install Node.js and MongoDB

### Setup
```bash
git clone https://github.com/rahulssr/job-portal.git
cd job-portal
```

### Install dependencies
#### Frontend:
```bash
cd client
npm install
```
#### Backend:
```bash
cd server
npm install
```

### Environment Variables

Create `.env` files in both `client` and `server` directories:

#### Backend `.env`
```
MONGODB_URI=...
PORT=5000
JWT_SECRET=...
CLOUDINARY_CLOUD_NAME=...
CLOUDINARY_API_KEY=...
CLOUDINARY_API_SECRET=...
CLERK_API_KEY=...
NODE_ENV=development
```

#### Frontend `.env`
```
REACT_APP_CLERK_FRONTEND_API=...
REACT_APP_BACKEND_URL=http://localhost:5000
```

### Run the Application
#### Backend:
```bash
cd server
npm start
```
#### Frontend:
```bash
cd client
npm start
```

### Access the App
Open [http://localhost:3000](http://localhost:5000) in your browser.

---

---

📝 **Code Snippet (Job Posting API)**

```javascript
router.post("/post-job", async (req, res) => {
  try {
    const { title, description, company, location, salary } = req.body;
    const newJob = new Job({ title, description, company, location, salary });
    await newJob.save();
    res.status(201).json({ message: "Job posted successfully!" });
  } catch (error) {
    res.status(500).json({ error: "Server error" });
  }
});
```

---

📊 **Usage Statistics**

```mermaid
pie
title Job Portal Activity
  "Active Users" : 120
  "Jobs Posted" : 80
  "Applications Submitted" : 250
  "Companies Registered" : 30
```

---

🤝 **Contributing**

1. Fork the repository
2. Create a new branch (`feature-awesome-thing`)
3. Commit your changes
4. Create a Pull Request

---


⭐ **Star this repo if you like it!** ⭐
