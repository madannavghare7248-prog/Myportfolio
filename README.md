# 🚀 Madan Navghare - Developer Portfolio

A premium, modern, dark-futuristic personal portfolio website engineered for **Madan Navghare** (Aspiring Software Developer & Java Full-Stack Developer). Built with React 18, Vite, Tailwind CSS v4, Framer Motion, and Lucide React.

---

## 🌟 Key Features

- 🌌 **Dark Futuristic Aesthetics**: Deep slate & cyan glow, grid pattern backdrop, glassmorphic cards, smooth borders, and responsive typography inspired by Vercel, Linear, and GitHub.
- ⚡ **Interactive Developer Visual**: Live IDE Code Playground with interactive code tabs (Java, SQL, React) and 1-click snippet copying.
- 🎯 **Recruiter-Friendly Presentation**: Zero fake companies or stats. Fully accurate profile details with clearly styled `[Editable Placeholder]` cards for future internships, certifications, and hackathons.
- 💡 **Interactive CLI Terminal**: Terminal widget supporting developer shell commands (`whoami`, `role`, `currently_learning`, `skills`, `projects`, `contact`, `clear`, `help`).
- 📊 **Development Activity Heatmap**: Interactive commit activity tracker with hover tooltips displaying daily engineering actions.
- 🛠️ **Categorized Skills Dashboard**: Categorized into 6 core areas with authentic level badges (`Intermediate`, `Learning`, `Familiar`) instead of fake percentage bars.
- 📂 **Filterable Projects Showcase**: 6 featured projects with category filtering (`All`, `Web`, `Java`, `AI`, `IoT`, `Embedded`) and interactive **Project Details Modal** (Problem, Solution, Key Features, Contribution, Challenges, Future Scope).
- 🎓 **Education Timeline**: Vertical node timeline for B.Tech (Electronic and Computer Engineering) and Diploma (Government Polytechnic Hingoli).
- 🏆 **Verified Achievements**: Gold/Bronze medal highlight card with interactive confetti animation.
- 📄 **Resume CTA**: Direct integration for downloading and viewing `assets/Madan_Navghare_Resume.pdf`.
- 📬 **Interactive Contact Form**: Frontend form validation, toast notifications, direct social links, and structure ready for EmailJS / Formspree / backend APIs.
- 🎯 **Custom Desktop Cursor**: Glowing lerp cursor follower on desktop (auto-disabled on touch/mobile devices).

---

## 📂 Project Structure

```text
portfolio/
 ├── public/
 │    └── assets/
 │         ├── Madan_Navghare_Resume.pdf  <-- Place your resume PDF here
 │         └── README_RESUME_GUIDE.txt
 ├── src/
 │    ├── components/
 │    │    ├── Navbar.jsx           # Sticky glassmorphic nav with scrollspy & mobile menu
 │    │    ├── CustomCursor.jsx     # Desktop glowing follower dot
 │    │    ├── GlowingBackground.jsx # Ambient lighting & grid overlay
 │    │    ├── TerminalWidget.jsx   # Interactive CLI terminal widget
 │    │    ├── CodingHeatmap.jsx    # Contribution activity visualization
 │    │    ├── ProjectCard.jsx      # Project card with tags & actions
 │    │    ├── ProjectModal.jsx     # Modal showing full project architecture
 │    │    ├── Toast.jsx            # Floating notification alerts
 │    │    └── Footer.jsx           # Footer with copyright & back-to-top
 │    ├── sections/
 │    │    ├── HeroSection.jsx      # Landing header & Live IDE playground
 │    │    ├── AboutSection.jsx     # Bio narrative & Currently Learning profile card
 │    │    ├── SkillsSection.jsx    # 6-category technical dashboard
 │    │    ├── ProjectsSection.jsx  # Filterable project gallery
 │    │    ├── TimelineSection.jsx  # Education vertical timeline
 │    │    ├── ExperienceSection.jsx # Internship & work experience cards
 │    │    ├── AchievementsSection.jsx # Bronze medal & achievement cards
 │    │    ├── GithubSection.jsx    # GitHub activity overview
 │    │    ├── ResumeSection.jsx    # Resume download & online view CTA
 │    │    └── ContactSection.jsx   # Direct contact form & validation
 │    ├── data/
 │    │    └── portfolioData.js     # Centralized profile, skills, & project data
 │    ├── hooks/
 │    │    └── useScrollSpy.js      # Custom scroll position tracker
 │    ├── App.jsx                   # Layout & modal orchestrator
 │    ├── index.css                 # CSS design system & Tailwind setup
 │    └── main.jsx                  # React DOM entrypoint
 ├── index.html                     # Main HTML with SEO meta tags & fonts
 ├── vite.config.js                 # Vite & Tailwind CSS v4 configuration
 ├── package.json                   # Dependencies manifest
 └── README.md                      # Comprehensive guide
```

---

## 🛠️ How to Run Locally

### Prerequisites
- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- `npm` or `yarn`

### Quick Start Commands

```bash
# 1. Open terminal in the project directory
cd portfolio

# 2. Install dependencies
npm install

# 3. Launch the development server
npm run dev
```

Open your browser and navigate to `http://localhost:5173`.

---

## ⚙️ How to Customize Your Information

All your personal profile data, projects, skills, education, and links are cleanly separated inside **`src/data/portfolioData.js`**. You don't need to touch complex React code to update your details!

### 1. Where to Add Your Resume
Place your actual resume PDF inside the `public/assets/` directory:
- Path: `public/assets/Madan_Navghare_Resume.pdf`
- When users click **Download Resume** or **View Resume**, this PDF will open automatically.

### 2. Where to Change GitHub / LinkedIn / Email
Open `src/data/portfolioData.js` and edit the `profileData.socials` object:
```javascript
export const profileData = {
  name: "Madan Navghare",
  socials: {
    github: "https://github.com/MadanNavghare",     // <-- Replace with your URL
    linkedin: "https://linkedin.com/in/madan-navghare", // <-- Replace with your URL
    email: "madanavghare.dev@gmail.com",           // <-- Replace with your Email
  },
  ...
};
```

### 3. Where to Add Future Projects
Open `src/data/portfolioData.js` and add a new object to the `projectsData` array:
```javascript
{
  id: "my-new-project",
  title: "New Project Name",
  category: "Java", // Category filter: 'Web' | 'Java' | 'AI' | 'IoT' | 'Embedded'
  tags: ["Java", "Spring Boot", "MySQL"],
  shortDesc: "A brief summary of the project...",
  imageBg: "from-cyan-900/40 via-blue-900/30 to-slate-900",
  icon: "Code2",
  github: "https://github.com/MadanNavghare/repository-name",
  liveDemo: "https://your-demo-url.com",
  details: {
    problem: "What problem does this solve?",
    solution: "How did you build the solution?",
    keyFeatures: ["Feature 1", "Feature 2", "Feature 3"],
    contribution: "What was your specific role?",
    challenges: "Technical challenge solved...",
    futureScope: "Planned future enhancements..."
  }
}
```

### 4. Where to Update Internships / Experience
Open `src/data/portfolioData.js` and update `experienceData`:
```javascript
export const experienceData = [
  {
    title: "Software Engineering Intern",
    company: "Acme Tech Solutions",
    duration: "June 2026 – August 2026",
    role: "Full Stack Java Developer Intern",
    location: "Remote / India",
    placeholder: false, // Set to false when adding a real company
    responsibilities: [
      "Built Spring Boot REST endpoints.",
      "Optimized MySQL database queries."
    ]
  }
];
```

---

## 🌐 How to Deploy Your Portfolio

### Deploying to Vercel (Recommended - 1 Click)
1. Push your code to your GitHub repository (`github.com/MadanNavghare/portfolio`).
2. Log into [Vercel](https://vercel.com).
3. Click **Add New Project** -> Select your GitHub repository.
4. Framework Preset: **Vite**.
5. Click **Deploy**. Vercel will build and host your portfolio with an SSL HTTPS domain in seconds!

### Deploying to GitHub Pages
1. Install `gh-pages`:
   ```bash
   npm i -D gh-pages
   ```
2. Add base path in `vite.config.js`:
   ```javascript
   export default defineConfig({
     base: '/portfolio/',
     plugins: [react(), tailwindcss()],
   })
   ```
3. Add scripts to `package.json`:
   ```json
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d dist"
   }
   ```
4. Run `npm run deploy`.

---

## 🔒 Environment Variables

No required environment variables are needed for basic deployment!
If you connect an automated email provider like EmailJS or Formspree in the future:
1. Create a `.env` file in the root directory:
   ```env
   VITE_EMAILJS_SERVICE_ID=your_service_id
   VITE_EMAILJS_TEMPLATE_ID=your_template_id
   VITE_EMAILJS_PUBLIC_KEY=your_public_key
   ```
2. Access them inside `src/sections/ContactSection.jsx` using `import.meta.env.VITE_EMAILJS_SERVICE_ID`.

---

© 2026 **Madan Navghare**. All rights reserved.
