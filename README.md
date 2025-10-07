<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Swagato Bag Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&family=Roboto&display=swap" rel="stylesheet" />
  <style>
    /* Root colors and fonts */
    :root {
      --primary-gradient: linear-gradient(135deg, #7f00ff 0%, #e100ff 100%);
      --secondary-gradient: linear-gradient(135deg, #00c6ff 0%, #0072ff 100%);
      --accent-color: #ff4d6d;
      --text-dark: #222222;
      --text-light: #fafafa;
      --bg-light: #fefefe;
      --shadow-light: rgba(0, 0, 0, 0.1);
      --shadow-hover: rgba(255, 77, 109, 0.3);
    }

    /* Global reset */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Poppins', 'Roboto', sans-serif;
      background: var(--primary-gradient);
      color: var(--text-dark);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 2rem 1rem;
    }

    a {
      color: var(--accent-color);
      text-decoration: none;
      font-weight: 600;
      transition: color 0.3s ease;
    }

    a:hover,
    a:focus {
      color: var(--text-light);
    }

    /* Header styles */
    header {
      background: var(--secondary-gradient);
      color: var(--text-light);
      width: 100%;
      max-width: 960px;
      padding: 1.5rem 2rem;
      border-radius: 16px;
      box-shadow: 0 8px 20px var(--shadow-light);
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      gap: 1.5rem;
      animation: slideFadeIn 1s ease forwards;
      position: sticky;
      top: 1rem;
      z-index: 10;
    }

    .logo-img {
      background-color: #a884ee;
      border-radius: 50%;
      width: 96px;
      height: 96px;
      object-fit: cover;
      box-shadow: 0 3px 12px rgba(128, 0, 255, 0.4);
      border: 4px solid var(--text-light);
      flex-shrink: 0;
      animation: bounceIn 1.2s ease forwards;
    }

    header h1 {
      font-size: 2.8rem;
      font-weight: 700;
      flex: 1 1 280px;
      filter: drop-shadow(0 1px 2px rgba(0,0,0,0.15));
      animation: fadeInUp 1.3s 0.2s ease forwards;
    }

    header p {
      font-style: italic;
      font-size: 1.3rem;
      flex: 2 1 360px;
      line-height: 1.3;
      display: flex;
      flex-direction: column;
      gap: 0.2rem;
      animation: fadeInUp 1.3s 0.3s ease forwards;
    }

    header p a {
      display: inline-block;
      font-size: 1.05rem;
      font-weight: 600;
      position: relative;
      animation: pulse 2.5s infinite;
    }

    /* Main content container */
    main {
      width: 100%;
      max-width: 900px;
      margin-top: 2.5rem;
      background: var(--bg-light);
      padding: 2rem 3rem;
      border-radius: 24px;
      box-shadow: 0 10px 30px var(--shadow-light);
      animation: fadeInUp 1.5s 0.5s ease forwards;
    }

    /* Section styling */
    section {
      margin-bottom: 3rem;
    }

    section h2 {
      font-weight: 700;
      font-size: 2rem;
      color: var(--accent-color);
      border-bottom: 4px solid var(--accent-color);
      padding-bottom: 0.6rem;
      margin-bottom: 1.3rem;
      position: relative;
      overflow: hidden;
      animation: underlineGrow 1.2s ease forwards;
    }

    ul {
      list-style: none;
      padding-left: 0;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    ul li {
      background: #e4eafc;
      border-radius: 12px;
      padding: 1rem 1.4rem;
      box-shadow: 3px 4px 12px rgba(0, 0, 255, 0.1);
      font-size: 1.1rem;
      line-height: 1.5;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: default;
    }

    ul li:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 25px var(--shadow-hover);
      background: #fff0f3;
    }

    strong {
      color: var(--primary-gradient);
    }

    /* Footer styles */
    footer {
      margin-top: auto;
      width: 100%;
      max-width: 900px;
      text-align: center;
      padding: 1rem 0 2rem;
      font-size: 0.9rem;
      color: #444;
      letter-spacing: 0.02em;
      user-select: none;
      border-top: 1px solid #ddd;
      background: transparent;
      animation: fadeInUp 1.8s 0.7s ease forwards;
    }

    footer a {
      font-weight: 600;
      color: var(--accent-color);
      animation: pulse 3s infinite;
    }

    /* Responsive adjustments */
    @media (max-width: 900px) {
      main {
        padding: 1.5rem 2rem;
      }
    }

    @media (max-width: 600px) {
      header {
        flex-direction: column;
        padding: 1.5rem 1.5rem;
        gap: 1rem;
        border-radius: 20px;
      }

      .logo-img {
        width: 80px;
        height: 80px;
        box-shadow: 0 2px 10px rgba(128, 0, 255, 0.3);
      }

      header h1 {
        font-size: 1.9rem;
        text-align: center;
        flex: none;
      }

      header p {
        font-size: 1rem;
        text-align: center;
        flex: none;
      }

      main {
        margin-top: 1.5rem;
        padding: 1.5rem 1.5rem;
        border-radius: 20px;
      }

      section h2 {
        font-size: 1.5rem;
        border-bottom-width: 3px;
      }

      ul li {
        font-size: 1rem;
      }
    }

    /* Animations */
    @keyframes slideFadeIn {
      0% { opacity: 0; transform: translateY(-20px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(12px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    @keyframes bounceIn {
      0% { opacity: 0; transform: scale(0.6) translateY(-40px);}
      60% { opacity: 1; transform: scale(1.05) translateY(10px);}
      100% { transform: scale(1) translateY(0);}
    }

    @keyframes underlineGrow {
      0% { width: 0; }
      100% { width: 100%; }
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.6; }
    }
  </style>
</head>
<body>
  <header>
    <img src="https://user-gen-media-assets.s3.amazonaws.com/gemini_images/b81be427-8820-4357-9b61-f88ea87c753c.png" alt="Profile Logo" class="logo-img" />
    <h1>Swagato Bag</h1>
    <p>
      Diploma in Medical Laboratory Technology (DMLT)<br />
      Email: <a href="mailto:Swagatobag@gmail.com">Swagatobag@gmail.com</a> | Phone: <a href="tel:+918759003758">8759003758</a>
    </p>
  </header>
  <main>
    <section class="about">
      <h2>Professional Summary</h2>
      <p>Dedicated and detail-oriented Medical Laboratory Technology diploma holder with hands-on experience in clinical laboratory procedures, diagnostics, and quality control. Skilled in various diagnostic instruments and committed to maintaining accuracy and safety standards. Seeking to contribute technical and interpersonal skills in a challenging healthcare environment.</p>
    </section>
    <section class="education">
      <h2>Education</h2>
      <ul>
        <li><strong>Diploma in Medical Laboratory Technology (DMLT)</strong><br />BMRC Hospital Ltd., West Bengal State Medical Faculty, 2023<br />- First Year: 64.5%<br />- Second Year: 66.66%</li>
      </ul>
    </section>
    <section class="training">
      <h2>Training & Internship</h2>
      <ul>
        <li>Internship at BMRC Hospital Ltd.<br />- Hands on exposure to routine laboratory tests and instrumentation.<br />- Assisted in Hematology, Biochemistry, Microbiology analyses.</li>
      </ul>
    </section>
    <section class="experience">
      <h2>Work Experience</h2>
      <ul>
        <li><strong>Laboratory Technician</strong> at APOLLO CLINIC BARASAT.<br />- Operated Erba H360 Hematology Analyzer, Erba EM200 Biochemistry Analyzer, Maglumi 800 and other lab equipment.<br />- Performed sample collection, processing, and data entry accurately.<br />- Maintained laboratory safety protocols and assisted in routine maintenance.</li>
      </ul>
    </section>
    <section class="skills">
      <h2>Technical Skills</h2>
      <ul>
        <li>Laboratory Instruments: Erba H360 Hematology Analyzer, Erba EM200 Biochemistry Analyzer(FULL AUTO), and other clinical analyzers.</li>
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
</body>
</html>
