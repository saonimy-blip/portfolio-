# Khmer Developer & Designer Portfolio (React.jsx)

គេហទំព័រ Portfolio ផ្ទាល់ខ្លួន ទំនើប ស្រស់ស្អាត បង្កើតឡើងដោយ **React.jsx** និង **Tailwind CSS** ដោយប្រើប្រាស់ពុម្ពអក្សរ **Khmer OS Siemreap** សម្រាប់អក្សរខ្មែរ និង **Cambria** សម្រាប់អក្សរអង់គ្លេស។

---

## របៀបដំណើរការលើ Visual Studio Code (How to Run on VS Code)

### ១. តម្រូវការជាមុន (Prerequisites)
មុនពេលចាប់ផ្តើម សូមប្រាកដថាអ្នកបានដំឡើង **Node.js** (កំណែ 18.x ឬខ្ពស់ជាងនេះ) នៅលើកុំព្យូទ័ររបស់អ្នក៖
- ទាញយក Node.js៖ [https://nodejs.org](https://nodejs.org) (ជ្រើសរើសយក LTS Version)

---

### ២. ជំហានដំណើរការលើ VS Code (Step-by-step Guide)

#### ជំហានទី ១៖ បើក Folder គម្រោងក្នុង VS Code
1. បើកកម្មវិធី **Visual Studio Code**។
2. ចុច **File** > **Open Folder...** (ឬចុចកាត់ `Ctrl + K, Ctrl + O`)។
3. ជ្រើសរើស Folder នៃគម្រោងនេះ។

#### ជំហានទី ២៖ បើក Terminal ក្នុង VS Code
- ចុចលើម៉ឺនុយ **Terminal** > **New Terminal** (ឬចុចកាត់ `Ctrl + ` ` ` លើក្តារចុច)។

#### ជំហានទី ៣៖ ដំឡើងកញ្ចប់ Packages (Install Dependencies)
វាយពាក្យបញ្ជាខាងក្រោមក្នុង Terminal រួចចុច Enter៖
```bash
npm install
```
*(រង់ចាំប្រហែល ១-២ នាទីដើម្បីឱ្យ npm ទាញយកកញ្ចប់ចាំបាច់ដូចជា React, Vite, Tailwind CSS, Lucide React...)*

#### ជំហានទី ៤៖ ចាប់ផ្តើមដំណើរការ Dev Server (Run Development Server)
វាយពាក្យបញ្ជា៖
```bash
npm run dev
```

#### ជំហានទី ៥៖ បើកមើលក្នុង Browser
បន្ទាប់ពីដំណើរការចប់ Terminal នឹងបង្ហាញតំណភ្ជាប់៖
```text
  VITE v8.x.x  ready in 250 ms

  ➜  Local:   http://localhost:3000/
  ➜  Network: http://192.168.x.x:3000/
```
- ចុចលើ `Ctrl + Click` លើតំណភ្ជាប់ `http://localhost:3000/` ឬបើក Google Chrome/Edge រួចវាយ `http://localhost:3000` ដើម្បីមើលគេហទំព័រផ្ទាល់។

---

## ៣. ពាក្យបញ្ជាសំខាន់ៗ (Available Scripts)

- `npm run dev` ៖ ចាប់ផ្តើម Local Server សម្រាប់សរសេរកូដ (មាន Auto-refresh/HMR ភ្លាមៗពេលកែសម្រួលកូដ)។
- `npm run build` ៖ បង្កើតឯកសារសម្រាប់ Upload ទៅកាន់ Production Hosting (នៅក្នុង Folder `dist/`)។
- `npm run preview` ៖ សាកល្បងមើល Production Build មុនពេលបង្ហោះលើ Hosting។
- `npm run lint` ៖ ពិនិត្យរកកំហុស syntax ឬបញ្ហាកូដ។

---

## ៤. ផ្នែកបន្ថែមដែលបានណែនាំក្នុង VS Code (Recommended Extensions)

ដើម្បីឱ្យការសរសេរកូដកាន់តែងាយស្រួល សូមដំឡើង Extensions ទាំងនេះក្នុង VS Code៖
1. **Tailwind CSS IntelliSense** (`bradlc.vscode-tailwindcss`) - ជំនួយការ auto-complete ឈ្មោះ class របស់ Tailwind CSS
2. **ES7+ React/Redux/React-Native snippets** (`dsznajder.es7-react-js-snippets`)
3. **Prettier - Code formatter** (`esbenp.prettier-vscode`)
4. **Auto Rename Tag** (`formulahendry.auto-rename-tag`)

---

## ៥. រចនាសម្ព័ន្ធឯកសារ (Folder Structure)

```text
├── index.html                 # HTML Entry Point (កំណត់ពុម្ពអក្សរ Khmer OS Siemreap & Cambria)
├── package.json               # បញ្ជី Dependencies និង Scripts
├── vite.config.ts             # ការកំណត់របស់ Vite Bundler & Tailwind
├── .vscode/                   # ការកំណត់សម្រាប់ VS Code (Auto-format, Extensions)
└── src/
    ├── main.jsx               # React Root Entry Point
    ├── App.jsx                # Layout ចម្បង និង State Management
    ├── index.css              # កូដកំណត់ DualFont (Khmer OS Siemreap + Cambria)
    ├── components/
    │   ├── Navbar.jsx         # របាររុករកខាងលើ (Sticky Navigation)
    │   ├── Hero.jsx           # ផ្ទាំងស្វាគមន៍ (Hero Section & Profile Image)
    │   ├── About.jsx          # ព័ត៌មានអំពីខ្ញុំ និងបទពិសោធន៍
    │   ├── Skills.jsx         # កាតជំនាញបច្ចេកវិទ្យា (អាចកែភាគរយផ្ទាល់បាន)
    │   ├── Projects.jsx       # គម្រោងទាំង ៦ និងប៊ូតុងមើលលម្អិត
    │   ├── Services.jsx       # សេវាកម្មទាំង ៦ ជាមួយប៊ូតុងស្នើសុំ
    │   ├── Contact.jsx        # ទម្រង់ទំនាក់ទំនង និងបណ្តាញសង្គម
    │   ├── Footer.jsx         # ផ្នែកខាងក្រោមគេហទំព័រ
    │   ├── ProjectModal.jsx   # ផ្ទាំងបង្ហាញព័ត៌មានគម្រោងលម្អិត (Lightbox)
    │   └── CvModal.jsx        # ផ្ទាំងមើល និងបោះពុម្ពប្រវត្តិរូប CV (Print PDF)
    └── data/
        └── portfolioData.js   # ទិន្នន័យគម្រោង ជំនាញ និងព័ត៌មានផ្ទាល់ខ្លួន
```
