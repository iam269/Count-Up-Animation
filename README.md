# 🎯 Count-Up Animation

A simple and elegant **count-up animation** built with **HTML, CSS, and JavaScript**.  
It smoothly animates numbers increasing from 0 to a target value — perfect for showcasing statistics like *Happy Customers*, *Meals Delivered*, or *Five Stars*.

🔗 **Live Demo:** [Count-Up Animation](https://iam269.github.io/Count-Up-Animation/)

---

## 📖 Overview

This project demonstrates how to create a clean count-up animation without external libraries.  
The numbers increase dynamically when the page loads, providing a smooth and modern effect for landing pages or portfolio sites.

---

## 🚀 Features

- Smooth number animation using pure JavaScript  
- Fully responsive and lightweight  
- Easy to customize (target values, speed, and style)  
- Works on all modern browsers  

---

## 🛠️ Built With

- **HTML5** – Structure of the page  
- **CSS3** – Styling and layout  
- **JavaScript (Vanilla)** – Animation logic  

---

## 💻 How to Use

1. **Clone the repository:**
   ```bash
   git clone https://github.com/iam269/Count-Up-Animation.git
Open the project folder:


cd Count-Up-Animation
Run the project:
Simply open the index.html file in your browser.

Or use a local development server (optional):

npx live-server
Customize the counters:

Open index.html and modify the values in the data-target attributes:

<div class="counter" data-target="500">0</div>
Adjust animation speed or timing inside script.js.

Change the design and layout in style.css.

⚙️ How It Works
Each number element has a data-target attribute that defines the final value.
The JavaScript script gradually increments the displayed value from 0 to that target, creating a smooth counting effect.

Example:

<div class="counter" data-target="1200">0</div>
JavaScript logic snippet:

const counters = document.querySelectorAll('.counter');

counters.forEach(counter => {
  const target = +counter.getAttribute('data-target');
  const speed = 200; // Lower = faster

  const updateCount = () => {
    const current = +counter.innerText;
    const increment = target / speed;

    if (current < target) {
      counter.innerText = Math.ceil(current + increment);
      setTimeout(updateCount, 10);
    } else {
      counter.innerText = target;
    }
  };

  updateCount();
});
🎨 Customization
You can easily modify the following:

Target values → edit in HTML (data-target)

Speed and timing → adjust in JavaScript

Fonts, colors, layout → edit in CSS

📁 Project Structure
Count-Up-Animation/
├── index.html
├── style.css
├── script.js
└── README.md
🤝 Contributing
Contributions are welcome!
If you’d like to improve the project:

Fork the repository

Create a new branch (feature/your-feature)

Commit your changes

Open a Pull Request

🪪 License
This project is licensed under the MIT License.
You’re free to use, modify, and distribute it for personal or commercial projects.

👨‍💻 Author
Developed by iam269
