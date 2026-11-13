# Exp 1 – React Lab Exercise: Understanding React File Structure

## NAME: kunam poorna chandra rao
## REG NO: 2305001012

## Aim
To create a basic React application using Vite and understand the purpose of important files and folders in the React project structure.

## Objectives
- Create a React project using Vite.
- Identify important React files and folders.
- Understand the role of `main.jsx`, `App.jsx`, `index.html`, and `package.json`.
- Create and use simple React components.
- Run and test a React application.

## Program

### Step 1: Create a React Project

```bash
npm create vite@latest student-app
cd student-app
npm install
npm run dev
```

Select React as the framework and JavaScript as the variant.

### Step 2: Understand the File Structure

```text
student-app/
│
├── node_modules/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   │   ├── Student.jsx
│   │   ├── Course.jsx
│   │   └── Faculty.jsx
│   │
│   ├── App.css
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
│
├── index.html
├── package.json
├── package-lock.json
└── vite.config.js
```

### Step 3: Understand index.html

The `index.html` file contains the root element where the React application is displayed.

```html
<div id="root"></div>
```

### Step 4: Understand main.jsx

The `main.jsx` file is the entry point of the React application. It connects React with the HTML root element and renders the App component.

### Step 5: Create App.jsx

```jsx
import './App.css'

function App() {
  return (
    <div className="container">
      <h1>Student Information System</h1>

      <Student />
      <Course />
      <Faculty />
    </div>
  )
}

export default App
```

### Step 6: Create Student.jsx

Create a `components` folder inside `src` and add `Student.jsx`.

```jsx
import '../App.css'

function Student() {
  return (
    <div className="student">
      <h2>Student Details</h2>

      <p>Name: kunam poorna chandra rao</p>
      <p>Register Number: 2305001012</p>
      <p>Department: CSE</p>
    </div>
  )
}

export default Student
```

### Step 7: Create Course.jsx

```jsx
import '../App.css'

function Course() {
  return (
    <div className="student">
      <h2>Course Details</h2>

      <p>Course:Modern Web Application Development</p>
      <p>Semester: 7</p>
      <p>Credits: 3</p>
    </div>
  )
}

export default Course
```

### Step 8: Create Faculty.jsx

```jsx
import '../App.css'

function Faculty() {
  return (
    <div className="student">
      <h2>Faculty Details</h2>

      <p>Name: AJITH KUMAR </p>
      <p>Designation: PROFESSOR</p>
      <p>Department: CSE</p>
    </div>
  )
}

export default Faculty
```

### Step 9: Import Components in App.jsx

```jsx

import './App.css'
import Student from './components/Student'
import Course from './components/Course'
import Faculty from './components/Faculty'

function App() {
  return (
    <div className="container">
      <h1>Student Information System</h1>

      <Student />
      <Course />
      <Faculty />
    </div>
  )
}

export default App

```

### Step 10: Add CSS in App.css
```
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f4f6f9;
}

.container {
  text-align: center;
  padding: 30px;
}

.container h1 {
  color: #4a47a3;
  font-size: 36px;
  margin-bottom: 50px;
}

/* Cards in one horizontal row */
.cards-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: stretch;
  gap: 25px;
  width: 100%;
}

/* All three cards */
.student,
.faculty,
.course {
  flex: 1;
  max-width: 300px;
  min-width: 0;
  box-sizing: border-box;
  padding: 25px;
  background: white;
  border-radius: 15px;
  transition: 0.3s;
  text-align: left;
}

.student {
  border: 2px solid #4a90e2;
}

.faculty {
  border: 2px solid #e67e22;
}

.course {
  border: 2px solid #27ae60;
}

.student h2 {
  color: #4a90e2;
}

.faculty h2 {
  color: #e67e22;
}

.course h2 {
  color: #27ae60;
}

.student p,
.faculty p,
.course p {
  color: #555;
  line-height: 1.8;
}

.student:hover,
.faculty:hover,
.course:hover {
  transform: translateY(-8px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
}
```
## Output

### Student Information System

<img width="818" height="412" alt="image" src="https://github.com/user-attachments/assets/4c0a79ed-efe4-402a-b2ad-419ff0844777" />



## Result

Thus, a basic React application was successfully created using Vite. The React file structure was understood, and reusable components were created and displayed successfully.
