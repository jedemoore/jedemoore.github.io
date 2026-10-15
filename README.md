<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jed Moore — GIS Analyst</title>
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"/>
<style>
  :root{--bg:#f7f8fa;--ink:#111;--mut:#6b7280;--acc:#1a73e8;--line:#e2e5ea;--card:#fff;--dark:#0a0a0a}
  *{box-sizing:border-box}
  body{margin:0;font:16px/1.6 Inter,system-ui,Segoe UI,Arial,sans-serif;background:var(--bg);color:var(--ink)}
  a{color:inherit;text-decoration:none}
  /* nav */
  nav{position:sticky;top:0;z-index:999;background:var(--dark);color:#fff;display:flex;
    align-items:center;justify-content:space-between;padding:16px 32px}
  .brand{display:flex;align-items:center;gap:12px;font-weight:700;font-size:1.1rem}
  .dot{width:26px;height:26px;border-radius:50%;background:var(--acc);display:inline-block}
  .nav-links a{margin-left:34px;font-weight:600;color:#fff}
  .nav-links a:hover{color:var(--acc)}
  main{max-width:1180px;margin:0 auto;padding:0 32px}
  .eyebrow{color:var(--acc);font-weight:700;letter-spacing:.12em;font-size:.8rem;margin:64px 0 20px}
  .display{font-size:clamp(2rem,6vw,4rem);font-weight:800;line-height:1.05;letter-spacing:-.02em;margin:0 0 32px;max-width:1000px}
  .lead{font-size:clamp(1.1rem,2.3vw,1.6rem);color:var(--mut);max-width:860px;margin:0 0 80px}
  h2{font-size:1.9rem;font-weight:800;margin:0}
  .sub{color:var(--mut);margin:6px 0 10px}
  .head-row{display:flex;justify-content:space-between;align-items:flex-start;border-bottom:1px solid var(--line);padding-bottom:14px;margin-bottom:36px}
  .arrow{font-size:1.6rem}
  section{margin:72px 0}
  /* project cards */
  .card{background:var(--card);border:1px solid var(--line);border-radius:14px;margin:16px 0;overflow:hidden;box-shadow:0 1px 3px rgba(0,0,0,.04)}
  .card>button{width:100%;text-align:left;background:none;border:0;color:var(--ink);
    font:inherit;font-weight:700;font-size:1.15rem;padding:22px 24px;cursor:pointer;
    display:flex;justify-content:space-between;align-items:center}
  .card>button span{color:var(--acc);font-size:1.5rem}
  .body{display:none;padding:0 24px 24px;color:var(--mut)}
  .card.open .body{display:block}
  .body h4{color:var(--ink);margin:16px 0 4px;font-size:1rem}
  ul{margin:0 0 8px;padding-left:20px}
  .map{height:320px;border-radius:10px;margin-top:12px}
  /* resume */
  .exp{margin:14px 0;padding-bottom:14px;border-bottom:1px solid var(--line)}
  .exp b{color:var(--ink)}
  .exp em{color:var(--mut);font-style:normal;float:right;font-size:.9rem}
  h3{margin:34px 0 6px;font-size:1.25rem}
  .tags span{display:inline-block;background:#eef1f6;border:1px solid var(--line);
    border-radius:999px;padding:6px 14px;margin:4px;font-size:.9rem}
  .contact a{color:var(--acc);font-weight:600}
  footer{border-top:1px solid var(--line);text-align:center;color:var(--mut);padding:40px 20px;font-size:.9rem}
  @media(max-width:600px){
    nav{padding:14px 18px}.nav-links a{margin-left:18px;font-size:.9rem}
    main{padding:0 18px}.exp em{float:none;display:block}
  }
</style>
</head>
<body>

<nav>
  <a class="brand" href="#top"><span class="dot"></span>Jed Moore</a>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#works">Works</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<main id="top">

  <section id="about">
    <div class="eyebrow">ABOUT</div>
    <h1 class="display">Geospatial Technology · GIS · Remote Sensing</h1>
    <p class="lead">I'm Jed Moore, and I'm currently studying Geographic Information Science
    &amp; Technology at Texas A&amp;M University. Through school and internships, I've developed
    experience working with spatial databases, remote sensing, GIS automation, and web mapping.
    I'm particularly interested in applying geospatial technology to complex problems in
    engineering, intelligence, and national security.</p>

    <div class="head-row">
      <div>
        <h2>More About Me</h2>
        <div class="sub">Outside of work and class!</div>
      </div>
      <span class="arrow">↗</span>
    </div>
    <ul>
      <li>Philanthropy Chair, Century Men's Society at Texas A&amp;M — won over $11,000 for
      Camp Kesem and organized a 5k race raising over $4,000.</li>
      <li>Treasurer, Freshman Leaders in Progress — managed a $16,000 annual budget.</li>
      <li>Activities: The Big Event, Fish Camp Counselor, 250+ volunteer hours.</li>
      <li>Spanish speaker (intermediate).</li>
    </ul>
  </section>

  <section id="works">
    <div class="head-row"><h2>Works</h2></div>

    <div class="card">
      <button onclick="this.parentElement.classList.toggle('open')">
        Change Detection of Artificial Islands <span>+</span></button>
      <div class="body">
        <h4>Problem</h4>
        <p>Understanding how artificial islands in the South China Sea expanded over time (2013–2024).</p>
        <h4>What I did</h4>
        <ul>
          <li>Performed temporal geospatial analysis using Landsat 8 and Sentinel-2 imagery.</li>
          <li>Developed an image preprocessing workflow in ArcGIS Pro: band compositing,
          cloud masking, raster clipping, and NDWI spectral generation.</li>
        </ul>
        <h4>What I found</h4>
        <p>[ADD — specific findings/results were not included in your source files]</p>
        <h4>What I would do differently</h4>
        <p>[ADD]</p>
        <div id="map" class="map"></div>
      </div>
    </div>

    <div class="card">
      <button onclick="this.parentElement.classList.toggle('open')">
        Lunar Colony Site Suitability <span>+</span></button>
      <div class="body">
        <h4>Problem</h4>
        <p>Identifying and grading potential lunar colony sites.</p>
        <h4>What I did</h4>
        <ul>
          <li>Created StoryMap and Dashboard visualizations of Lunar Reconnaissance Orbiter
          DEM and temperature data.</li>
          <li>Mapped and graded candidate sites based on proximity to crater ice and
          communication visibility with Earth.</li>
        </ul>
        <h4>What I found</h4>
        <p>[ADD — specific findings/results were not included in your source files]</p>
        <h4>What I would do differently</h4>
        <p>[ADD]</p>
        <!-- No Earth-basemap Leaflet map (lunar data). ArcGIS/StoryMap iframe: [ADD link] -->
      </div>
    </div>

    <div class="card">
      <button onclick="this.parentElement.classList.toggle('open')">
        Handicap Parking Compliance Audit <span>+</span></button>
      <div class="body">
        <h4>Problem</h4>
        <p>Assessing handicap parking compliance across the Texas A&amp;M campus.</p>
        <h4>What I did</h4>
        <ul>
          <li>Conducted site visits and collected over 40,000 field data points for spatial analysis.</li>
          <li>Automated geoprocessing workflows with Python and SQL, reducing manual
          processing time by 80%.</li>
        </ul>
        <h4>What I found</h4>
        <p>[ADD — specific findings/results were not included in your source files]</p>
        <h4>What I would do differently</h4>
        <p>[ADD]</p>
      </div>
    </div>
  </section>

  <section id="resume">
    <div class="head-row"><h2>Resume</h2></div>

    <h3>Education</h3>
    <div class="exp">
      <b>Texas A&amp;M University</b> <em>Expected December 2026</em><br>
      B.S. in Geographic Information Science and Technology — College Station, TX<br>
      <small>Coursework: GIS Programming, Geodatabases, Remote Sensing, Digital Image Processing,
      Data Analysis, GNSS, Cartography &amp; Visualization, Information Science, Geography of Terrorism.</small>
    </div>

    <h3>Experience</h3>
    <div class="exp">
      <b>GIS Intern — Quiddity Engineering</b> <em>June 2026 – August 2026</em><br>
      Katy, TX
      <ul>
        <li>Supported migration of enterprise GIS infrastructure from AWS to Azure for utility
        clients, helping modernize cloud-hosted Web GIS and Utility Network architecture.</li>
        <li>Developed standardized GIS basemap datasets from county sources (district boundaries,
        tax parcels, plats, sections, street centerlines, county ownership, commercial properties,
        and LiDAR-derived building footprints).</li>
      </ul>
    </div>
    <div class="exp">
      <b>GIS Student Technician — Transportation Services</b> <em>August 2025 – May 2026</em><br>
      College Station, TX
      <ul>
        <li>Digitized campus road paint features, corrected existing data onto a new projection,
        and overhauled geodatabase infrastructure to support adding campus bike lanes.</li>
        <li>Produced layouts, Operations Dashboards, and StoryMap visualizations supporting
        infrastructure planning and situational awareness.</li>
      </ul>
    </div>
    <div class="exp">
      <b>GIS Intern — Transportation Services</b> <em>May 2025 – August 2025</em><br>
      College Station, TX
      <ul>
        <li>Audited handicap parking compliance on campus, collecting over 40,000 field data points.</li>
        <li>Automated geoprocessing workflows with Python and SQL, reducing manual processing time by 80%.</li>
      </ul>
    </div>

    <h3>Skills</h3>
    <div class="tags">
      <span>Ar
