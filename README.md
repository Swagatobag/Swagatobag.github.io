<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Swagato Bag Portfolio</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap');
    *, *::before, *::after { box-sizing: border-box; }
    html { font-size: 16px; }
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      background: linear-gradient(135deg, #e0f7fa, #c0f0f6);
      color: #0a293d;
      overflow-x: hidden;
      cursor: none;
      min-height: 100vh;
    }
    a { color: #00796b; text-decoration: none; }
    a:hover { text-decoration: underline; }
    .custom-cursor {
      position: fixed; top: 0; left: 0; width: 24px; height: 24px;
      border: 2px solid #00796b; border-radius: 50%;
      pointer-events: none;
      transform: translate(-50%, -50%);
      transition: width 0.2s, height 0.2s, background-color 0.2s, border-color 0.2s;
      z-index: 9999; mix-blend-mode: difference;
    }
    a:hover ~ .custom-cursor, button:hover ~ .custom-cursor {
      width: 40px; height: 40px; background-color: #00796b33; border-color: #004d40;
    }
    header {
      background: linear-gradient(90deg, #00796b, #009688);
      color: white; text-align: center; padding: 2rem 1rem;
      display: flex; align-items: center; justify-content: center; gap: 1.5rem;
      flex-wrap: wrap; box-shadow: 0 4px 12px rgb(0 121 107 / 0.3);
      position: sticky; top: 0; z-index: 1000;
      transition: background-color 0.3s;
      flex-direction: row;
    }
    header.scrolled {
      background: #004d40; box-shadow: 0 2px 8px rgb(0 77 64 / 0.5);
    }
    .logo-img {
      background-color: #a7ffeb;
      border-radius: 50%;
      width: 90px;
      height: 90px;
      object-fit: cover;
      box-shadow: 0 4px 12px rgba(0,121,107,0.3);
      border: 3px solid #fff; flex-shrink: 0;
      transition: transform 0.3s;
      max-width: 22vw;
      max-height: 22vw;
      min-width: 60px;
      min-height: 60px;
    }
    header h1 {
      margin: 0;
      font-size: 2.5rem;
      flex: 1 1 200px;
      font-weight: 700;
      letter-spacing: 1px;
      text-shadow: 0 1px 3px rgba(0,0,0,0.15);
      word-break: break-word;
    }
    header p {
      margin: 0.25rem 0 0;
      font-style: italic;
      font-size: 1.1rem;
      flex: 2 1 320px;
      user-select: text;
      word-break: break-word;
    }
    header p a { color: #b2dfdb; font-weight: 600; }
    header p a:hover { color: #80cbc4; }

    main {
      max-width: 960px;
      margin: 3rem auto 4rem auto;
      background-color: #ffffffcc;
      backdrop-filter: saturate(180%) blur(15px);
      padding: 3rem 3rem 4rem 3rem;
      box-shadow: 0 8px 24px rgb(0 0 0 / 0.1);
      border-radius: 20px;
      overflow: hidden;
    }
    section {
      margin-bottom: 3.5rem;
      opacity: 0;
      transform: translateY(30px);
      animation-fill-mode: forwards;
      animation-timing-function: ease-out;
    }
    section.visible { opacity: 1; transform: translateY(0); }
    section h2 {
      border-bottom: 4px solid #00796b;
      padding-bottom: 0.7rem;
      color: #00796b;
      font-weight: 700;
      font-size: 2rem;
      margin-bottom: 1.5rem;
      letter-spacing: 0.03em;
      text-transform: uppercase;
    }
    ul { list-style-type: none; padding-left: 0; }
    ul li {
      background-color: #b2dfdb;
      margin-bottom: 1rem;
      padding: 1rem 1.3rem;
      border-radius: 12px;
      box-shadow: 2px 2px 12px rgba(0,121,107,0.15);
      font-weight: 500;
      color: #004d40;
      transition: background-color 0.3s;
      cursor: default;
      word-break: break-word;
    }
    ul li:hover { background-color: #80cbc4; color: #00251a; box-shadow: 0 6px 16px rgba(0, 77, 64, 0.3);}
    .about p {
      font-size: 1.15rem;
      font-weight: 400;
      line-height: 1.6;
      max-width: 700px;
      margin: 0 auto;
      position: relative;
      overflow: hidden;
    }
    .typing-highlight {
      display: inline-block; border-right: 3px solid #00796b;
      white-space: nowrap; overflow: hidden;
      animation: typing 3s steps(40, end) forwards, blink 1s infinite step-end alternate;
      max-width: 100%;
    }
    @keyframes typing { from { width: 0 } to { width: 100% } }
    @keyframes blink { 50% { border-color: transparent } 100% { border-color: #00796b } }

    /* Tablet (≤1024px) */
    @media (max-width: 1024px) {
      main {
        padding: 2rem 1.5rem 2.5rem 1.5rem;
        margin: 2.5rem 1rem 3rem 1rem;
      }
      header h1 { font-size: 2rem; }
      .logo-img { width: 70px; height: 70px; max-width: 18vw; max-height: 18vw;}
    }
    /* Mobile (≤700px) */
    @media (max-width: 700px) {
      header {
        flex-direction: column;
        gap: 0.8rem;
        padding: 1.3rem 0.6rem 1.3rem 0.6rem;
        min-width: 0;
      }
      .logo-img { width: 55px; height: 55px; max-width: 30vw; max-height: 30vw;}
      header h1 { font-size: 1.25rem; text-align: center; }
      header p { font-size: 0.97rem; text-align: center; }
      main {
        padding: 1.1rem 0.4rem 1.7rem 0.4rem;
        margin: 1.2rem 0.3rem 2rem 0.3rem;
        border-radius: 10px;
      }
      section h2 { font-size: 1.14rem;}
      ul li { font-size: 0.89rem;}
      .about p { font-size: 0.98rem; }
    }
    /* Extra small mobile (≤420px) */
    @media (max-width: 420px) {
      header h1 { font-size: 1.07rem; }
      .logo-img { width: 40px; height: 40px; }
      section h2 { font-size: 1rem; }
      main { padding: 0.5rem 0.1rem 1rem 0.1rem;}
    }
    footer {
      text-align: center; font-size: 0.87rem; color: #004d40aa;
      padding: 1rem 1rem 2rem; border-top: 1px solid #00796b33;
      background: transparent; font-weight: 500; user-select: none;
    }
  </style>
</head>
<body>
  <header id="pageHeader">
    <img src="assets/logo.jpg" alt="Profile Logo" class="logo-img" />
    <h1>Swagato Bag</h1>
    <p>Diploma in Medical Laboratory Technology (DMLT)</p>
    <p>Email: <a href="mailto:Swagatobag@gmail.com">Swagatobag@gmail.com</a> | Phone: 8759003758</p>
  </header>

  <main>
    <section class="about">
      <h2>Professional Summary</h2>
      <p>
        <span class="typing-highlight">
          Dedicated and detail-oriented Medical Laboratory Technology diploma holder with hands-on experience in clinical laboratory procedures, diagnostics, and quality control. Skilled in various di[...]
        </span>
      </p>
    </section>

    <section class="education">
      <h2>Education</h2>
      <ul>
        <li><strong>Diploma in Medical Laboratory Technology (DMLT)</strong><br/>BMRC Hospital Ltd., West Bengal State Medical Faculty, 2023<br/>- First Year: 64.5%<br/>- Second Year: 66.66%</li>
      </ul>
    </section>

    <section class="training">
      <h2>Training & Internship</h2>
      <ul>
        <li>Internship at BMRC Hospital Ltd.<br/>- Hands on exposure to routine laboratory tests and instrumentation.<br/>- Assisted in Hematology, Biochemistry, Microbiology analyses.</li>
      </ul>
    </section>

    <section class="experience">
      <h2>Work Experience</h2>
      <ul>
        <li><strong>Laboratory Technician</strong> at APOLLO CLINIC BARASAT.<br/>
          - Operated Erba H360 Hematology Analyzer, Erba EM200 Biochemistry Analyzer, Maglumi 800, and other lab equipment.<br/>
          - Performed sample collection, processing, and data entry accurately.<br/>
          - Maintained laboratory safety protocols and assisted in routine maintenance.
        </li>
      </ul>
    </section>

    <section class="skills">
      <h2>Technical Skills</h2>
      <ul>
        <li>Laboratory Instruments: Erba H360 Hematology Analyzer, Erba EM200 Biochemistry Analyzer (FULL AUTO), and other clinical analyzers.</li>
        <li>Diagnostic Techniques: Hematology, Biochemistry, Microbiology testing.</li>
        <li>Sample collection, processing, and accurate data entry.</li>
        <li>Maintained laboratory safety protocols and assisted in routine maintenance.</li>
        <li>Software: Basic knowledge of laboratory data management systems.</li>
        <li>Safety and quality control in laboratory environments.</li>
      </ul>
    </section>

    <section class="languages">
      <h2>Languages</h2>
      <ul>
        <li>English (Fluent)</li>
        <li>Bengali (Native)</li>
      </ul>
    </section>
  </main>

  <footer>
    &copy; 2025 Swagato Bag. Contact: <a href="mailto:Swagatobag@gmail.com">Swagatobag@gmail.com</a>
  </footer>

  <div class="custom-cursor" id="cursor"></div>

  <script>
    // Reveal sections on scroll
    function revealSections() {
      const sections = document.querySelectorAll('section');
      const triggerBottom = window.innerHeight * 0.85;
      sections.forEach(section => {
        const sectionTop = section.getBoundingClientRect().top;
        if(sectionTop < triggerBottom){
          section.classList.add('visible');
        }
      });
    }
    window.addEventListener('scroll', revealSections);
    window.addEventListener('load', () => {
      revealSections();
      const header = document.getElementById('pageHeader');
      window.addEventListener('scroll', () => {
        if(window.scrollY > 50){
          header.classList.add('scrolled');
        } else {
          header.classList.remove('scrolled');
        }
      });
    });

    // Custom cursor movement
    const cursor = document.getElementById('cursor');
    let mouseX = 0, mouseY = 0;
    let posX = 0, posY = 0;
    const speed = 0.15;
    function animateCursor() {
      posX += (mouseX - posX) * speed;
      posY += (mouseY - posY) * speed;
      cursor.style.transform = `translate3d(${posX}px, ${posY}px, 0) translate(-50%, -50%)`;
      requestAnimationFrame(animateCursor);
    }
    animateCursor();
    window.addEventListener('mousemove', (e) => {
      mouseX = e.clientX;
      mouseY = e.clientY;
    });
  </script>
</body>
</html>
