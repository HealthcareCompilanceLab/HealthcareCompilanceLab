<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Healthcare Compliance Lab</title>
  <meta name="description" content="Academic capstone profile for the Healthcare Data Security Compliance Checker project." />
  <link href="https://api.fontshare.com/v2/css?f[]=satoshi@400,500,700&f[]=zodiak@400,700&display=swap" rel="stylesheet">
  <style>
    :root, [data-theme="light"] {
      --text-xs: clamp(0.75rem, 0.72rem + 0.2vw, 0.875rem);
      --text-sm: clamp(0.875rem, 0.82rem + 0.24vw, 1rem);
      --text-base: clamp(1rem, 0.96rem + 0.22vw, 1.125rem);
      --text-lg: clamp(1.125rem, 1.03rem + 0.45vw, 1.45rem);
      --text-xl: clamp(1.45rem, 1.2rem + 1vw, 2.1rem);
      --text-2xl: clamp(2rem, 1.35rem + 2vw, 3.3rem);
      --space-1: .25rem; --space-2: .5rem; --space-3: .75rem; --space-4: 1rem; --space-5: 1.25rem; --space-6: 1.5rem; --space-8: 2rem; --space-10: 2.5rem; --space-12: 3rem; --space-16: 4rem; --space-20: 5rem;
      --color-bg: #f7f6f2; --color-surface: #fbfaf7; --color-surface-2:#f2efe8; --color-border:#d8d3ca; --color-text:#24211c; --color-text-muted:#69665f; --color-text-faint:#9c9890; --color-primary:#0e6671; --color-primary-hover:#0b525b; --color-primary-soft:#d8e8ea; --color-success:#3f6d2c; --color-warning:#8a5820; --color-danger:#8d305d; --shadow-sm:0 1px 3px rgba(0,0,0,.05); --shadow-md:0 10px 30px rgba(26,28,29,.08); --radius-sm:.5rem; --radius-md:.85rem; --radius-lg:1.25rem; --radius-xl:1.5rem; --content:1120px;
      --font-body:'Satoshi', system-ui, sans-serif; --font-display:'Zodiak', Georgia, serif;
    }
    [data-theme="dark"] {
      --color-bg: #151513; --color-surface: #1d1d1a; --color-surface-2:#23231f; --color-border:#383833; --color-text:#ece8e1; --color-text-muted:#b7b2aa; --color-text-faint:#807c75; --color-primary:#69a8b0; --color-primary-hover:#88b9c0; --color-primary-soft:#21353a; --shadow-sm:0 1px 3px rgba(0,0,0,.25); --shadow-md:0 14px 32px rgba(0,0,0,.3);
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body { font-family: var(--font-body); font-size: var(--text-base); line-height: 1.7; background: radial-gradient(circle at top right, rgba(14,102,113,.08), transparent 28%), var(--color-bg); color: var(--color-text); }
    img, svg { max-width: 100%; display: block; }
    a { color: inherit; text-decoration: none; }
    button { font: inherit; border: 0; background: none; cursor: pointer; }
    .container { width: min(calc(100% - 2rem), var(--content)); margin: 0 auto; }
    .skip-link { position: absolute; left: -999px; top: 1rem; background: var(--color-primary); color: white; padding: .75rem 1rem; border-radius: var(--radius-sm); }
    .skip-link:focus { left: 1rem; z-index: 1000; }
    .site-header { position: sticky; top: 0; z-index: 20; backdrop-filter: blur(12px); background: color-mix(in srgb, var(--color-bg) 88%, transparent); border-bottom: 1px solid color-mix(in srgb, var(--color-text) 12%, transparent); }
    .nav { display: flex; align-items: center; justify-content: space-between; gap: var(--space-4); min-height: 4.5rem; }
    .brand { display: flex; align-items: center; gap: .9rem; font-weight: 700; }
    .brand-mark { width: 2.5rem; height: 2.5rem; border-radius: .8rem; display: grid; place-items: center; background: linear-gradient(135deg, var(--color-primary), color-mix(in srgb, var(--color-primary) 65%, white)); color: white; box-shadow: var(--shadow-sm); }
    .brand-text small { display: block; color: var(--color-text-muted); font-weight: 500; font-size: var(--text-xs); }
    .nav-links { display: flex; gap: 1rem; flex-wrap: wrap; font-size: var(--text-sm); color: var(--color-text-muted); }
    .nav-links a:hover, .nav-links a:focus-visible { color: var(--color-primary); }
    .theme-toggle { width: 2.75rem; height: 2.75rem; border: 1px solid color-mix(in srgb, var(--color-text) 10%, transparent); border-radius: 999px; display: grid; place-items: center; background: var(--color-surface); }
    main { padding: var(--space-12) 0 var(--space-20); }
    .hero { display: grid; grid-template-columns: 1.25fr .9fr; gap: var(--space-8); align-items: stretch; padding-top: var(--space-10); }
    .panel { background: color-mix(in srgb, var(--color-surface) 92%, white); border: 1px solid color-mix(in srgb, var(--color-text) 10%, transparent); border-radius: var(--radius-xl); box-shadow: var(--shadow-md); }
    .hero-copy { padding: clamp(1.5rem, 3vw, 3rem); }
    .eyebrow { display: inline-flex; align-items: center; gap: .5rem; padding: .45rem .8rem; border-radius: 999px; background: var(--color-primary-soft); color: var(--color-primary); font-size: var(--text-xs); font-weight: 700; letter-spacing: .04em; text-transform: uppercase; }
    h1, h2, h3 { font-family: var(--font-display); line-height: 1.12; }
    h1 { font-size: var(--text-2xl); margin-top: var(--space-5); max-width: 12ch; }
    .hero-copy p { color: var(--color-text-muted); margin-top: var(--space-5); max-width: 62ch; }
    .cta-row { display: flex; flex-wrap: wrap; gap: .9rem; margin-top: var(--space-6); }
    .btn { display: inline-flex; align-items: center; justify-content: center; min-height: 2.9rem; padding: .8rem 1.1rem; border-radius: 999px; font-size: var(--text-sm); font-weight: 700; }
    .btn-primary { background: var(--color-primary); color: white; }
    .btn-primary:hover { background: var(--color-primary-hover); }
    .btn-secondary { border: 1px solid color-mix(in srgb, var(--color-text) 12%, transparent); background: var(--color-surface); }
    .hero-card { padding: clamp(1.25rem, 2vw, 2rem); display: grid; gap: 1rem; }
    .stat-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1rem; }
    .stat { padding: 1rem; border-radius: var(--radius-lg); background: var(--color-surface-2); border: 1px solid color-mix(in srgb, var(--color-text) 8%, transparent); }
    .stat strong { display: block; font-size: var(--text-lg); font-family: var(--font-display); }
    section { padding-top: var(--space-16); }
    .section-intro { display: grid; gap: .65rem; margin-bottom: var(--space-6); }
    .section-intro p { color: var(--color-text-muted); max-width: 75ch; }
    .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: var(--space-6); }
    .card { padding: 1.4rem; background: var(--color-surface); border: 1px solid color-mix(in srgb, var(--color-text) 10%, transparent); border-radius: var(--radius-lg); box-shadow: var(--shadow-sm); }
    .card h3 { font-size: var(--text-lg); margin-bottom: .7rem; }
    .muted { color: var(--color-text-muted); }
    .pill-list, .simple-list { list-style: none; display: grid; gap: .8rem; }
    .pill-list li { padding: .9rem 1rem; background: var(--color-surface-2); border-radius: var(--radius-md); border: 1px solid color-mix(in srgb, var(--color-text) 8%, transparent); }
    .simple-list li { padding-left: 1.1rem; position: relative; }
    .simple-list li::before { content: ""; position: absolute; left: 0; top: .72em; width: .42rem; height: .42rem; border-radius: 50%; background: var(--color-primary); }
    table { width: 100%; border-collapse: collapse; overflow: hidden; border-radius: var(--radius-lg); border: 1px solid color-mix(in srgb, var(--color-text) 10%, transparent); background: var(--color-surface); }
    th, td { text-align: left; padding: .95rem 1rem; vertical-align: top; border-bottom: 1px solid color-mix(in srgb, var(--color-text) 8%, transparent); }
    th { font-size: var(--text-sm); color: var(--color-text-muted); background: var(--color-surface-2); }
    tr:last-child td { border-bottom: 0; }
    .timeline { display: grid; gap: .9rem; }
    .timeline-item { padding: 1rem 1.1rem; border-left: 3px solid var(--color-primary); background: var(--color-surface); border-radius: 0 var(--radius-md) var(--radius-md) 0; }
    .roles { display: grid; gap: 1rem; }
    .role-title { font-weight: 700; }
    footer { padding: var(--space-16) 0 var(--space-8); color: var(--color-text-muted); }
    .footer-box { padding: 1.2rem 1.4rem; border: 1px solid color-mix(in srgb, var(--color-text) 10%, transparent); border-radius: var(--radius-lg); background: var(--color-surface); }
    code { font-family: ui-monospace, SFMono-Regular, Menlo, monospace; font-size: .95em; }
    @media (max-width: 900px) {
      .hero, .grid-2 { grid-template-columns: 1fr; }
      .nav { padding: .8rem 0; align-items: start; }
      .nav-links { display: none; }
    }
  </style>
</head>
<body>
  <a class="skip-link" href="#content">Skip to content</a>
  <header class="site-header">
    <div class="container nav">
      <div class="brand" aria-label="Healthcare Compliance Lab">
        <div class="brand-mark" aria-hidden="true">
          <svg viewBox="0 0 24 24" width="22" height="22" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round">
            <path d="M12 3l7 4v5c0 4.6-2.7 7.8-7 9-4.3-1.2-7-4.4-7-9V7l7-4Z"></path>
            <path d="M9 12h6"></path><path d="M12 9v6"></path>
          </svg>
        </div>
        <div class="brand-text">Healthcare Compliance Lab<small>Academic cybersecurity capstone</small></div>
      </div>
      <nav class="nav-links" aria-label="Primary">
        <a href="#overview">Overview</a>
        <a href="#completion">Progress</a>
        <a href="#feedback">Feedback</a>
        <a href="#mapping">Control Map</a>
        <a href="#milestones">Milestones</a>
        <a href="#roles">Roles</a>
      </nav>
      <button class="theme-toggle" data-theme-toggle aria-label="Switch theme">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path></svg>
      </button>
    </div>
  </header>

  <main id="content" class="container">
    <section class="hero">
      <div class="panel hero-copy">
        <span class="eyebrow">Healthcare security • compliance automation</span>
        <h1>Healthcare Data Security Compliance Checker</h1>
        <p>This capstone project presents a lightweight compliance support tool designed to help healthcare organizations assess whether foundational technical safeguards are in place. The prototype does not collect or store live patient information; instead, it evaluates security-related configurations and operational indicators against healthcare security expectations informed by HIPAA, PHIPA, and NIST guidance.</p>
        <div class="cta-row">
          <a class="btn btn-primary" href="#overview">Read project overview</a>
          <a class="btn btn-secondary" href="https://github.com/HealthcareCompilanceLab/healthcare-compliance-checker" target="_blank" rel="noopener noreferrer">View repository</a>
        </div>
      </div>
      <aside class="panel hero-card" aria-label="Project highlights">
        <div class="stat-grid">
          <div class="stat"><span class="muted">Institution</span><strong>Sheridan College</strong></div>
          <div class="stat"><span class="muted">Program</span><strong>Information Sciences</strong></div>
          <div class="stat"><span class="muted">Phase</span><strong>Phase 2</strong></div>
          <div class="stat"><span class="muted">Focus</span><strong>Evidence-based validation</strong></div>
        </div>
        <div class="card">
          <h3>Core safeguard areas</h3>
          <ul class="simple-list">
            <li>Access control</li>
            <li>Encryption and transmission security</li>
            <li>Logging and audit controls</li>
            <li>Backup and contingency planning</li>
          </ul>
        </div>
      </aside>
    </section>

    <section id="overview">
      <div class="section-intro">
        <h2>Project overview</h2>
        <p>The Healthcare Data Security Compliance Checker has been developed to help healthcare organizations evaluate whether key technical safeguards are properly implemented. Rather than processing protected health information, the tool monitors security-related metadata such as login attempts, multifactor authentication status, role-based access settings, audit log availability, encryption posture, backup protection, and suspicious access indicators.</p>
      </div>
      <div class="grid-2">
        <article class="card">
          <h3>How the tool works</h3>
          <p class="muted">The system is intended to operate as a lightweight background monitoring and compliance support tool while staff access systems that may contain sensitive information. It evaluates collected signals against predefined control expectations and produces both plain-language and technical reports that describe risk level, evidence, compliance gaps, and recommended remediation steps.</p>
        </article>
        <article class="card">
          <h3>Academic objective</h3>
          <p class="muted">The project demonstrates how regulatory expectations can be translated into technical validation logic. It also supports the broader capstone goal of connecting information science, cybersecurity, and regulatory analysis in a practical proof-of-concept suitable for smaller healthcare environments that may lack enterprise compliance platforms.</p>
        </article>
      </div>
    </section>

    <section id="completion">
      <div class="section-intro">
        <h2>Winter 2026 completion</h2>
        <p>Phase 1 established the original project idea, proposal, literature review, prototype concept, and early implementation. The initial proposal highlighted a recurring gap between high-level regulatory requirements and their practical technical implementation in healthcare cybersecurity.</p>
      </div>
      <div class="grid-2">
        <div class="card">
          <h3>Completed in Phase 1</h3>
          <ul class="pill-list">
            <li>Defined the research problem and academic scope.</li>
            <li>Reviewed HIPAA, PHIPA, ISO/IEC 27001, and NIST SP 800-53A as supporting frameworks.</li>
            <li>Built an initial Python-based prototype.</li>
            <li>Implemented selected checks for MFA, TLS/HTTPS, audit logging, encrypted backups, and password policy strength.</li>
          </ul>
        </div>
        <div class="card">
          <h3>Prototype capabilities</h3>
          <p class="muted">The current implementation uses a control bank, sample system data, weighted risk scoring, attack-detection logic, and HTML report generation. During Week 14, the prototype was tested under stronger and weaker compliance scenarios by varying responses across access control, encryption, audit logging, backup protection, and suspicious activity indicators.</p>
        </div>
      </div>
    </section>

    <section id="feedback">
      <div class="section-intro">
        <h2>Feedback and response</h2>
        <p>For the spring and summer 2026 semester, the project is being refined to improve both technical depth and compliance alignment. The main feedback emphasized clearer standards mapping, better explanation of configuration evaluation, stronger healthcare usability, greater awareness of common cyberattacks, and the addition of a system architecture diagram.</p>
      </div>
      <div class="grid-2">
        <div class="card">
          <h3>Key feedback received</h3>
          <ul class="simple-list">
            <li>Explain how configurations are evaluated against HIPAA and NIST expectations.</li>
            <li>Map technical checks to recognizable standards and security areas.</li>
            <li>Make the system understandable for medical staff, not only technical users.</li>
            <li>Reflect common cyberattack risks within the compliance logic.</li>
            <li>Add an overall system diagram and maintain weekly GitHub updates.</li>
          </ul>
        </div>
        <div class="card">
          <h3>Phase 2 response plan</h3>
          <ul class="simple-list">
            <li>Expand each control to include an ID, category, expected value, evidence, remediation, risk level, and regulatory mapping.</li>
            <li>Improve the questionnaire for both healthcare staff and IT or security users.</li>
            <li>Add explanatory content for weak passwords, missing MFA, repeated failed logins, suspicious IP activity, missing audit logs, and unencrypted backups.</li>
            <li>Strengthen documentation and update the repository on a weekly basis.</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="mapping">
      <div class="section-intro">
        <h2>Illustrative control map</h2>
        <p>The table below reframes the example control mapping in a cleaner academic format, connecting each technical check with a safeguard area, expected evidence, and practical risk level.</p>
      </div>
      <div class="card" style="padding:0; overflow:auto;">
        <table>
          <thead>
            <tr>
              <th>Tool check</th>
              <th>Category</th>
              <th>Related standard area</th>
              <th>Evidence needed</th>
              <th>Risk</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>MFA enabled for administrative accounts</td>
              <td>Access control</td>
              <td>HIPAA technical safeguards; NIST access control</td>
              <td>Configuration screenshot or policy evidence showing MFA is enabled</td>
              <td>High</td>
            </tr>
            <tr>
              <td>Audit logging enabled</td>
              <td>Audit controls</td>
              <td>HIPAA audit controls; NIST logging-related controls</td>
              <td>Log settings and sample audit records</td>
              <td>Medium to high</td>
            </tr>
            <tr>
              <td>TLS or HTTPS enforced</td>
              <td>Transmission security</td>
              <td>HIPAA transmission security</td>
              <td>Certificate details and TLS configuration</td>
              <td>High</td>
            </tr>
            <tr>
              <td>Backups encrypted</td>
              <td>Contingency planning</td>
              <td>HIPAA backup and security practices</td>
              <td>Backup policy and encryption configuration</td>
              <td>High</td>
            </tr>
            <tr>
              <td>Failed login detection</td>
              <td>Detect and respond</td>
              <td>NIST CSF detect and respond functions</td>
              <td>Login logs or alert records</td>
              <td>Medium to high</td>
            </tr>
          </tbody>
        </table>
      </div>
    </section>

    <section id="milestones">
      <div class="section-intro">
        <h2>Weekly milestones</h2>
        <p>The following plan presents a structured Phase 2 schedule. It is suitable for README documentation, a project proposal appendix, or a capstone progress page, while still noting that milestones may change in response to faculty feedback.</p>
      </div>
      <div class="card" style="padding:0; overflow:auto;">
        <table>
          <thead>
            <tr><th>Week</th><th>Planned milestone</th><th>Evidence</th></tr>
          </thead>
          <tbody>
            <tr><td>1</td><td>Submit revised project plan and update GitHub README</td><td>Revised plan report and repository update</td></tr>
            <tr><td>2</td><td>Update system architecture diagram and finalize Phase 2 scope</td><td>Architecture diagram and GitHub update</td></tr>
            <tr><td>3</td><td>Improve questionnaires and usability flow</td><td>User-interface screenshots</td></tr>
            <tr><td>4</td><td>Expand control bank with regulatory mappings</td><td>Updated control bank or JSON structure</td></tr>
            <tr><td>5</td><td>Add HIPAA, PHIPA, and NIST mappings to each major control</td><td>Mapping table and technical documentation</td></tr>
            <tr><td>6</td><td>Build background monitoring logic for access events</td><td>Code commit and test data</td></tr>
            <tr><td>7</td><td>Add suspicious activity detection for failed logins, unusual access, and missing MFA</td><td>Alert screenshots and test results</td></tr>
            <tr><td>8</td><td>Improve scoring by category and severity</td><td>Sample reports</td></tr>
            <tr><td>9</td><td>Improve plain-language and technical report output</td><td>HTML or PDF report screenshots</td></tr>
            <tr><td>10</td><td>Test multiple healthcare scenarios</td><td>Testing notes and screenshots</td></tr>
            <tr><td>11</td><td>Prepare final report, slides, and demo script</td><td>Draft report and slides</td></tr>
            <tr><td>12</td><td>Finalize project, repository, demo, and submission</td><td>Final repository and presentation</td></tr>
          </tbody>
        </table>
      </div>
    </section>

    <section id="roles">
      <div class="section-intro">
        <h2>Group roles</h2>
        <p>The project structure below presents responsibilities in a more formal and natural academic style while preserving the division of work already established by the group.</p>
      </div>
      <div class="grid-2 roles">
        <article class="card">
          <div class="role-title">Carleen — Research and Compliance Lead</div>
          <p class="muted">Responsible for HIPAA, PHIPA, and NIST mapping; compliance documentation; scenario testing; and support for formal report writing.</p>
        </article>
        <article class="card">
          <div class="role-title">Kasi — Technical and Prototype Lead</div>
          <p class="muted">Responsible for code implementation, Streamlit interface development, monitoring logic, scoring features, and report generation.</p>
        </article>
        <article class="card">
          <div class="role-title">Hartej — Project Management and Presentation Lead</div>
          <p class="muted">Responsible for weekly coordination, GitHub evidence tracking, slide preparation, diagrams, and overall integration support.</p>
        </article>
        <article class="card">
          <div class="role-title">Risks and challenges</div>
          <p class="muted">Anticipated risks include difficulty mapping checks accurately to HIPAA, NIST, and PHIPA; scope growth; complexity in background monitoring; inconsistent weekly repository updates; uneven group contribution; and unrealistic testing scenarios.</p>
        </article>
      </div>
    </section>

    <section>
      <div class="section-intro">
        <h2>Academic positioning</h2>
        <p>This project aligns with a Sheridan cybersecurity-oriented information sciences pathway and reflects applied learning in healthcare security evaluation. It also fits broader Ontario and U.S. healthcare privacy and security expectations that emphasize safeguarding personal health information, risk management, and implementation-oriented security guidance.</p>
      </div>
      <div class="grid-2">
        <div class="timeline">
          <div class="timeline-item"><strong>Sheridan context:</strong> Sheridan's Honours Bachelor of Information Sciences (Cyber Security) emphasizes areas such as intrusion detection, network security, ethical hacking, and database security, making it a relevant academic environment for this capstone.</div>
          <div class="timeline-item"><strong>Ontario context:</strong> PHIPA requires health information custodians to take precautions against theft, loss, and unauthorized collection, use, disclosure, copying, modification, or disposal of personal health information.</div>
          <div class="timeline-item"><strong>NIST context:</strong> NIST SP 800-66 Rev. 2 provides guidance to help organizations understand and implement HIPAA Security Rule safeguards and maps HIPAA standards to NIST Cybersecurity Framework subcategories and SP 800-53 controls.</div>
        </div>
        <div class="card">
          <h3>Suggested README tone</h3>
          <p class="muted">For a GitHub profile or repository landing page, aim for concise academic language, avoid overstating compliance claims, and describe the system as a proof-of-concept or compliance support tool. Phrases such as <code>supports evaluation</code>, <code>maps technical checks to safeguard areas</code>, and <code>generates evidence-based reports</code> sound more natural and credible than marketing-heavy wording.</p>
        </div>
      </div>
    </section>

    <footer>
      <div class="footer-box">Prepared as a refined academic-style project page for the Healthcare Compliance Lab capstone. Last updated for Spring/Summer 2026 planning.</div>
    </footer>
  </main>

  <script>
    (function(){
      const root = document.documentElement;
      const toggle = document.querySelector('[data-theme-toggle]');
      let theme = window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light';
      root.setAttribute('data-theme', theme);
      const renderIcon = () => {
        toggle.innerHTML = theme === 'dark'
          ? '<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="5"></circle><path d="M12 1v2M12 21v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M1 12h2M21 12h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42"></path></svg>'
          : '<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"></path></svg>';
      };
      renderIcon();
      toggle.addEventListener('click', function(){
        theme = theme === 'dark' ? 'light' : 'dark';
        root.setAttribute('data-theme', theme);
        renderIcon();
      });
    })();
  </script>
</body>
</html>
