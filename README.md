

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jed Moore — GIS Analyst</title>
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"/>
<style>
  :root{--bg:#0f1419;--card:#1a222c;--txt:#e8edf2;--mut:#9fb0c0;--acc:#4ea1d3}
  *{box-sizing:border-box}
  body{margin:0;font:16px/1.5 system-ui,Segoe UI,Arial,sans-serif;background:var(--bg);color:var(--txt)}
  header{padding:48px 20px;text-align:center;background:linear-gradient(135deg,#13202c,#1a2b3a)}
  header h1{margin:0 0 8px;font-size:2rem}
  header p{margin:0;color:var(--acc);font-size:1.05rem}
  main{max-width:820px;margin:0 auto;padding:20px}
  section{margin:34px 0}
  h2{border-bottom:2px solid var(--acc);padding-bottom:6px;font-size:1.3rem}
  .card{background:var(--card);border:1px solid #26323f;border-radius:10px;margin:14px 0;overflow:hidden}
  .card>button{width:100%;text-align:left;background:none;border:0;color:var(--txt);
    font:inherit;font-weight:600;padding:16px;cursor:pointer;display:flex;justify-content:space-between;align-items:center}
  .card>button span{color:var(--acc)}
  .body{display:none;padding:0 16px 16px;color:var(--mut)}
  .card.open .body{display:block}
  .body h4{color:var(--txt);margin:14px 0 4px}
  ul{margin:0 0 8px;padding-left:20px}
  .map{height:300px;border-radius:8px;margin-top:10px}
  .exp{margin:12px 0}
  .exp b{color:var(--txt)}
  .exp em{color:var(--mut);font-style:normal;float:right;font-size:.9rem}
  a{color:var(--acc)}
  .tags span{display:inline-block;background:#22303d;border-radius:14px;padding:4px 11px;margin:3px;font-size:.85rem}
  footer{text-align:center;color:var(--mut);padding:30px 20px;font-size:.9rem}
  @media(max-width:600px){header h1{font-size:1.6rem}.exp em{float:none;display:block}}
</style>
</head>
<body>
<header>
  <h1>Jed Moore</h1>
  <p>GIS &amp; Geospatial Analyst — remote sensing, GIS automation, and web mapping</p>
</header>

<main>
  <section id="about">
    <h2>About</h2>
    <p>I'm Jed Moore, currently studying Geographic Information Science &amp; Technology at
    Texas A&amp;M University. Through school and internships, I've developed experience working
    with spatial databases, remote sensing, GIS automation, and web mapping. I'm particularly
    interested in applying geospatial technology to complex problems in engineering, intelligence,
    and national security.</p>
  </section>

  <section id="projects">
    <h2>Projects</h2>

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
    <h2>Resume</h2>
    <h3>Education</h3>
    <div class="exp">
      <b>Texas A&amp;M University</b> <em>Expected December 2026</em><br>
      B.S. in Geographic Information Science and Technology — College Station, TX
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

    <h3>Leadership &amp; Involvement</h3>
    <div class="exp">
      <b>Philanthropy Chair — Century Men's Society at Texas A&amp;M</b> <em>January 2023 – Present</em>
      <ul>
        <li>Chaired external philanthropy competitions, managed budgets and schedules, and won
        over $11,000 for Camp Kesem.</li>
        <li>Chaired and developed a 5k philanthropy race, organizing 100+ members and raising
        over $4,000 for Camp Kesem.</li>
      </ul>
    </div>
    <div class="exp">
      <b>Treasurer — Freshman Leaders in Progress</b> <em>August 2023 – May 2024</em>
      <ul><li>Managed a $16,000 annual budget.</li></ul>
    </div>

    <h3>Skills</h3>
    <div class="tags">
      <span>ArcGIS Pro</span><span>ESRI Suite</span><span>ENVI</span><span>AWS</span><span>Azure</span>
      <span>Microsoft Office Suite</span><span>Databricks</span><span>Python</span><span>SQL</span>
      <span>R</span><span>Arcade</span><span>Spanish (Intermediate)</span>
    </div>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:jedemoore@gmail.com">jedemoore@gmail.com</a></p>
    <p>Phone: (458) 202-4336</p>
    <p>LinkedIn: <a href="https://www.linkedin.com/in/jedemoore">linkedin.com/in/jedemoore</a></p>
  </section>
</main>

<footer>© 2026 Jed Moore</footer>

<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script>
  // Map data (stored inside this file).
  // NOTE: Precise project coordinates were not provided in the source files.
  // The point below marks the general South China Sea artificial-islands region
  // (Spratly Islands area) for illustration. Replace with verified coordinates. [ADD]
  var points = [
    { lat: 9.55, lng: 112.9, title: "Spratly Islands region",
      note: "General South China Sea artificial-islands study area (2013–2024). Exact coordinates: [ADD]" }
  ];

  var map = L.map('map').setView([9.55, 112.9], 5);
  L.tileLayer('https://server.arcgisonline.com/ArcGIS/rest/services/World_Topo_Map/MapServer/tile/{z}/{y}/{x}',
    { attribution: 'Tiles © Esri' }).addT
