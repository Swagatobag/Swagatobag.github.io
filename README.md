<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Swagato Bag Portfolio</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap');

    /* Reset and base */
    *, *::before, *::after {
      box-sizing: border-box;
    }
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      background: linear-gradient(135deg, #e0f7fa, #c0f0f6);
      color: #0a293d;
      overflow-x: hidden;
      cursor: none;
    }
    a {
      color: #00796b;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }

    /* Custom cursor */
    .custom-cursor {
      position: fixed;
      top: 0;
      left: 0;
      width: 24px;
      height: 24px;
      border: 2px solid #00796b;
      border-radius: 50%;
      pointer-events: none;
      transform: translate(-50%, -50%);
      transition: width 0.2s ease, height 0.2s ease, background-color 0.2s ease, border-color 0.2s ease;
      z-index: 9999;
      mix-blend-mode: difference;
    }
    a:hover ~ .custom-cursor,
    button:hover ~ .custom-cursor {
      width: 40px;
      height: 40px;
      background-color: #00796b33;
      border-color: #004d40;
    }

    /* Header styles, etc. (unchanged, omitted for brevity for this answer) */
    /* ... (keep the previous styles here) ... */

    /* Main content styles, animations, etc. (unchanged, omitted for brevity) */
    /* ... (keep the previous styles here) ... */
  </style>
</head>
<body>

  <header id="pageHeader">
    <!-- Replaced with public image URL for logo -->
    <img src="https://images.unsplash.com/photo-1581093588401-6c84a57b5fab?ixlib=rb-4.0.3&auto=format&fit=crop&w=80&q=80" alt="Profile Logo" class="logo-img" />
    <h1>Swagato Bag</h1>
    <p>Diploma in Medical Laboratory Technology (DMLT)</p>
    <p>Email: <a href="mailto:Swagatobag@gmail.com">Swagatobag@gmail.com</a> | Phone: 8759003758</p>
  </header>

  <main>
    <section class="about">
      <h2>Professional Summary</h2>
      <p><span class="typing-highlight">Dedicated and detail-oriented Medical Laboratory Technology diploma holder with hands-on experience in clinical laboratory procedures, diagnostics, and quality control. Skilled in various diagnostic instruments and committed to maintaining accuracy and safety standards. Seeking to contribute technical and interpersonal skills in a challenging healthcare environment.</span></p>
      <div class="image-wrapper">
        <!-- Replace with public URL -->
        <img src="https://images.unsplash.com/photo-1581092160610-4504beebb57f?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Medical lab technician at work" loading="lazy" />
      </div>
    </section>

    <section class="education">
      <h2>Education</h2>
      <ul>
        <li><strong>Diploma in Medical Laboratory Technology (DMLT)</strong><br/>BMRC Hospital Ltd., West Bengal State Medical Faculty, 2023<br/>- First Year: 64.5%<br/>- Second Year: 66.66%</li>
      </ul>
      <div class="image-wrapper">
        <img src="https://images.unsplash.com/photo-1576765607927-030e9c2a1fdd?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Graduate certificate diploma" loading="lazy" />
      </div>
    </section>

    <section class="training">
      <h2>Training & Internship</h2>
      <ul>
        <li>Internship at BMRC Hospital Ltd.<br/>- Hands on exposure to routine laboratory tests and instrumentation.<br/>- Assisted in Hematology, Biochemistry, Microbiology analyses.</li>
      </ul>
      <div class="image-wrapper">
        <img src="https://images.unsplash.com/photo-1579154203451-76478e2b53c0?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Lab internship" loading="lazy" />
      </div>
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
      <div class="image-wrapper">
        <img src="https://images.unsplash.com/photo-1581093889799-465d4a3a2ef3?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Lab instruments and technician" loading="lazy" />
      </div>
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
    // Scroll reveal, cursor animation code remains unchanged
    // (omit here for brevity, same as previous script)
  </script>
</body>
</html>
