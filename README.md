# Book Showcase

## Deployment Link
[Visit the Project](https://inspiring-scone-d72a24.netlify.app/)

## 🎯 Key Complex Features

### 1. Animated Gradient Background
**Code:**
css
body {
  background: linear-gradient(45deg, #ff9a9e, #fad0c4, #fbc2eb, #fda085, #f6d365, #c9ffbf, #9be2fe, #e6c1c1);
  background-size: 300% 300%;
  animation: backgroundAnimation 15s infinite;
}

@keyframes backgroundAnimation {
  0% { background-position: 0% 50%; }
  25% { background-position: 50% 100%; }
  50% { background-position: 100% 50%; }
  75% { background-position: 50% 0%; }
  100% { background-position: 0% 50%; }
}

**Explanation:**
Creates a continuously moving gradient using CSS animations. The 8-color gradient shifts positions using keyframe animation, creating a dynamic background effect. The background-size (300% 300%) enables smooth color transitions across the viewport.

---

### 2. 3D Book Flip Animation

#### HTML Structure:
html
<div class="book">
  <div class="book-inner">
    <div class="book-front">
      <img src="/images/bookfront.jpeg">
    </div>
    <div class="book-back">Click for Details</div>
  </div>
</div>

#### CSS Implementation:
css
.book {
  perspective: 1000px;
}

.book-inner {
  transform-style: preserve-3d;
  transition: transform 0.8s;
}

.book:hover .book-inner {
  transform: rotateY(180deg);
}

.book-front, .book-back {
  backface-visibility: hidden;
}

.book-back {
  transform: rotateY(180deg);
}


**Key Techniques:**
- `perspective` creates 3D space.
- `transform-style: preserve-3d` maintains 3D positioning.
- `backface-visibility` hides the reverse side during rotation.
- Smooth transition with 0.8s timing.

---

### 3. Responsive Navigation & Layout

#### Flexbox Implementation:
css
nav {
  display: flex;
  justify-content: flex-end;
}

.books-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}

body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}


**Features:**
- Mobile-responsive navigation using Flexbox.
- Wrapping book container for different screen sizes.
- Sticky footer using min-height: 100vh and margin-top: auto.

---

### 4. Interactive Details Dropdown

#### HTML Semantic Structure:
html
<details>
  <summary>Purchase Links</summary>
  <ul>
    <li><a href="https://www.amazon.com">Amazon</a></li>
    <li><a href="https://www.flipkart.com">Flipkart</a></li>
  </ul>
</details>

#### CSS Enhancements:
css
details {
  cursor: pointer;
  transition: all 0.3s ease;
}

summary {
  font-weight: bold;
  padding: 0.5rem;
}

details[open] {
  background-color: #f8f9fa;
  border-radius: 5px;
}


**Features:**
- Native HTML disclosure element with custom styling.
- Smooth transitions for interactive elements.
- Semantic markup for accessibility.

---

## 🖥️ Project Structure
book-showcase/
├── index.html
├── book1.html
├── styles.css
└── images/
    ├── bookfront.jpeg
    ├── book2.jpeg
    └── book3.jpeg

---

## 💻 Quick Start
1. Clone the repository:
   ```bash
   git clone https://github.com/JaferaliPW/book-outlook.git
   ```
2. Open `index.html` in a browser.

---

## 📝 License
MIT License © 2025 Book Showcase

