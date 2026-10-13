# novadesigns
this is my website

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#10100f">
<title>Print Atelier | Creative Design Catalogue</title>
<meta name="description" content="Explore a curated catalogue of digital printing, leather, glass, wood, wallpaper and artistic surface designs.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@500;600;700&display=swap" rel="stylesheet">

<style>
:root {
  --bg:#10100f;
  --panel:#191917;
  --text:#f5f0e7;
  --muted:#a6a096;
  --gold:#d5b477;
  --line:#34322d;
}
* {box-sizing:border-box;margin:0;padding:0}
html {scroll-behavior:smooth;scroll-padding-top:90px}
body {
  background:var(--bg);color:var(--text);
  font-family:'DM Sans',sans-serif;line-height:1.6;
}
a {color:inherit;text-decoration:none}
button,input {font:inherit}
button {cursor:pointer}
img {display:block;width:100%;height:100%;object-fit:cover}
.wrap {width:min(1240px,91%);margin:auto}
header {
  position:sticky;top:0;z-index:20;
  background:#10100fee;backdrop-filter:blur(16px);
  border-bottom:1px solid var(--line);
}
.nav {
  min-height:76px;display:flex;align-items:center;
  justify-content:space-between;gap:20px;
}
.brand {font-size:20px;font-weight:700;letter-spacing:1px}
.brand span {color:var(--gold)}
.navlinks {display:flex;align-items:center;gap:28px;font-size:13px;color:var(--muted)}
.navlinks a:hover {color:var(--gold)}
.eyebrow {
  text-transform:uppercase;letter-spacing:3px;
  font-size:11px;color:var(--gold);font-weight:700;
}
.hero {
  min-height:590px;display:grid;grid-template-columns:1.05fr .95fr;
  align-items:center;gap:40px;padding-top:65px;padding-bottom:75px;
}
h1,h2,h3 {font-family:'Playfair Display',serif;font-weight:500;line-height:1.12}
h1 {font-size:clamp(43px,6.2vw,79px);margin:22px 0}
h1 em {font-weight:500;color:var(--gold)}
.hero p,.section-intro {color:var(--muted);max-width:500px;font-size:15px}
.actions {display:flex;gap:13px;flex-wrap:wrap;margin-top:30px}
.btn {
  border:1px solid var(--gold);padding:12px 20px;
  display:inline-flex;align-items:center;justify-content:center;
  font-size:12px;font-weight:700;transition:.25s;
}
.btn.primary {background:var(--gold);color:#15130e}
.btn:hover {transform:translateY(-3px);background:var(--text);color:#111;border-color:var(--text)}
.hero-art {height:440px;position:relative}
.hero-art img {border-radius:3px}
.hero-art:after {
  content:"SURFACE • COLOUR • CREATIVITY";
  position:absolute;bottom:18px;left:18px;
  background:#111c;color:white;padding:11px 14px;
  font-size:10px;letter-spacing:2px;
}
.hero-note {font-size:11px;color:var(--muted);margin-top:14px}
.stats {
  display:grid;grid-template-columns:repeat(3,1fr);
  border-top:1px solid var(--line);border-bottom:1px solid var(--line);
  padding:25px 0;margin-bottom:100px;
}
.stat {text-align:center;border-right:1px solid var(--line)}
.stat:last-child {border:0}
.stat strong {display:block;font-size:25px;color:var(--gold);font-family:'Playfair Display',serif}
.stat span {font-size:11px;color:var(--muted)}
section {padding-bottom:100px}
.section-head {
  display:flex;justify-content:space-between;align-items:end;
  gap:25px;margin-bottom:32px;
}
h2 {font-size:clamp(32px,4vw,48px);margin-top:12px}
.section-intro {font-size:13px;max-width:350px}
.categories {
  display:flex;gap:10px;flex-wrap:wrap;margin-bottom:25px;
}
.chip {
  padding:9px 15px;border:1px solid var(--line);
  background:transparent;color:var(--muted);font-size:12px;
  transition:.2s;
}
.chip:hover,.chip.active {background:var(--gold);border-color:var(--gold);color:#16130e}
.search {
  width:100%;max-width:350px;background:var(--panel);
  border:1px solid var(--line);padding:12px 15px;
  color:var(--text);outline:none;margin-bottom:28px;
}
.search:focus {border-color:var(--gold)}
.gallery {
  display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:22px;
}
.card {min-width:0;animation:appear .5s both}
.card.hidden {display:none}
.card-image {height:320px;overflow:hidden;position:relative;background:var(--panel)}
.card-image img {transition:transform .7s cubic-bezier(.2,.7,.2,1)}
.card:hover .card-image img {transform:scale(1.07)}
.card-tag {
  position:absolute;top:13px;left:13px;background:#111d;
  padding:6px 10px;font-size:10px;letter-spacing:1px;
}
.view {
  position:absolute;right:13px;bottom:13px;
  background:var(--gold);color:#111;border:0;padding:10px 14px;
  font-size:11px;font-weight:700;opacity:0;transition:.25s;
}
.card:hover .view,.view:focus {opacity:1}
.card-info {display:flex;justify-content:space-between;gap:12px;padding:15px 0;border-bottom:1px solid var(--line)}
.card-info h3 {font-size:19px}
.card-info p {color:var(--muted);font-size:11px;margin-top:5px}
.card-number {color:var(--gold);font-size:12px}
.empty {display:none;color:var(--muted);padding:40px 0}
.process {
  display:grid;grid-template-columns:repeat(3,1fr);gap:24px;margin-top:35px;
}
.process article {padding:27px;border:1px solid var(--line);background:var(--panel)}
.process small {color:var(--gold);letter-spacing:2px}
.process h3 {font-size:24px;margin:17px 0 10px}
.process p {font-size:13px;color:var(--muted)}
.contact {
  padding:55px;background:linear-gradient(120deg,#252117,#171614);
  border:1px solid #51442d;display:flex;
  align-items:center;justify-content:space-between;gap:30px;
}
.contact h2 {max-width:650px}
.contact p {color:var(--muted);font-size:13px;margin-top:15px}
footer {
  padding:28px 0;border-top:1px solid var(--line);
  color:var(--muted);font-size:11px;
}
.footer-inner {display:flex;justify-content:space-between;gap:15px;flex-wrap:wrap}
.reveal {opacity:0;transform:translateY(22px);transition:opacity .7s,transform .7s}
.reveal.visible {opacity:1;transform:none}
.modal {
  display:none;position:fixed;inset:0;z-index:50;
  background:#000e;align-items:center;justify-content:center;padding:22px;
}
.modal.open {display:flex}
.modal-box {
  width:min(900px,100%);max-height:90vh;overflow:auto;
  background:var(--panel);position:relative;padding:20px;
}
.modal-box img {height:min(62vh,600px);object-fit:contain;background:#111}
.modal-box h3 {font-size:26px;margin:17px 0 6px}
.modal-box p {color:var(--muted);font-size:13px}
.close {
  position:absolute;top:10px;right:10px;z-index:2;
  background:var(--gold);color:#111;border:0;
  width:38px;height:38px;font-size:23px;
}
@keyframes appear {from{opacity:0;transform:translateY(14px)}to{opacity:1;transform:none}}
@media(max-width:800px) {
  .hero {grid-template-columns:1fr;padding-top:55px}
  .hero-art {height:350px}
  .gallery {grid-template-columns:repeat(2,minmax(0,1fr));gap:15px}
  .card-image {height:260px}
  .process {grid-template-columns:1fr}
  .contact {padding:30px;align-items:flex-start;flex-direction:column}
  .navlinks {gap:13px}
}
@media(max-width:480px) {
  .nav {min-height:65px}
  .navlinks {font-size:11px;gap:10px}
  .brand {font-size:16px}
  .hero-art {height:280px}
  .gallery {grid-template-columns:1fr}
  .card-image {height:330px}
  .stats {margin-bottom:70px}
  section {padding-bottom:70px}
  .section-head {align-items:flex-start;flex-direction:column}
  .view {opacity:1}
}
@media(prefers-reduced-motion:reduce) {
  *,*::before,*::after {scroll-behavior:auto!important;animation:none!important;transition:none!important}
  .reveal {opacity:1;transform:none}
}
</style>
</head>
<body>

<header>
  <div class="wrap nav">
    <a class="brand" href="#home">PRINT<span>ATELIER.</span></a>
    <nav class="navlinks">
      <a href="#home">Home</a>
      <a href="#gallery">Catalogue</a>
      <a href="#process">Our Approach</a>
      <a href="#contact">Contact</a>
    </nav>
  </div>
</header>

<main>
<section class="wrap hero" id="home">
  <div class="reveal">
    <div class="eyebrow">Digital printing · Creative surfaces</div>
    <h1>Where surfaces<br>meet <em>artistry.</em></h1>
    <p>A curated showcase of patterns, colours and surface applications. Discover creative directions for leather, glass, wood, wallpapers and artistic finishes.</p>
    <div class="actions">
      <a class="btn primary" href="#gallery">EXPLORE CATALOGUE ↗</a>
      <a class="btn" href="#contact">DISCUSS A PROJECT</a>
    </div>
    <div class="hero-note">A creative portfolio for surface design and digital printing.</div>
  </div>
  <div class="hero-art reveal">
    <img src="https://images.unsplash.com/photo-1494438639946-1ebd1d20bf85?auto=format&fit=crop&w=1100&q=85" alt="Elegant interior with artistic surfaces">
  </div>
</section>

<div class="wrap stats reveal">
  <div class="stat"><strong>01</strong><span>Creative concepts</span></div>
  <div class="stat"><strong>06</strong><span>Design categories</span></div>
  <div class="stat"><strong>∞</strong><span>Ideas to explore</span></div>
</div>

<section class="wrap" id="gallery">
  <div class="section-head reveal">
    <div>
      <div class="eyebrow">The collection</div>
      <h2>Explore the catalogue.</h2>
    </div>
    <p class="section-intro">Browse different materials and visual styles. Select any design to open a larger preview.</p>
  </div>

  <div class="categories reveal" id="filters">
    <button class="chip active" data-category="all">All designs</button>
    <button class="chip" data-category="Leather">Leather</button>
    <button class="chip" data-category="Glass">Glass</button>
    <button class="chip" data-category="Wood">Wood</button>
    <button class="chip" data-category="Wallpaper">Wallpaper</button>
    <button class="chip" data-category="Hand Painting">Hand painting</button>
    <button class="chip" data-category="Patterns">Patterns</button>
  </div>

  <input class="search reveal" id="search" type="search" placeholder="Search designs or materials..." aria-label="Search designs">

  <div class="gallery" id="galleryGrid">

    <article class="card" data-category="Leather" data-name="botanical leather floral">
      <div class="card-image">
        <img loading="lazy" src="https://images.unsplash.com/photo-1490750967868-88aa4486c946?auto=format&fit=crop&w=800&q=80" alt="Botanical floral colour inspiration">
        <span class="card-tag">LEATHER</span>
        <button class="view" data-title="Botanical Expressions" data-category="Leather" data-description="Floral colour inspiration for exploring printed leather and fashion accessories.">VIEW DESIGN ↗</button>
      </div>
      <div class="card-info"><div><h3>Botanical Expressions</h3><p>Floral · Nature inspired</p></div><span class="card-number">01</span></div>
    </article>

    <article class="card" data-category="Glass" data-name="glass architecture modern interior">
      <div class="card-image">
        <img loading="lazy" src="https://images.unsplash.com/photo-1600210492486-724fe5c67fb0?auto=format&fit=crop&w=800&q=80" alt="Modern interior and glass design inspiration">
        <span class="card-tag">GLASS</span>
        <button class="view" data-title="Modern Transparency" data-category="Glass" data-description="Contemporary interior inspiration for decorative glass applications.">VIEW DESIGN ↗</button>
      </div>
      <div class="card-info"><div><h3>Modern Transparency</h3><p>Interior · Contemporary</p></div><span class="card-number">02</span></div>
    </article>

    <article class="card" data-category="Wood" data-name="wood natural grain texture">
      <div class="card-image">
        <img loading="lazy" src="https://images.unsplash.com/photo-1513519245088-0e12902e5a38?auto=format&fit=crop&w=800&q=80" alt="Wood and natural interior textures">
        <span class="card-tag">WOOD</span>
        <button class="view" data-title="Natural Textures" data-category="Wood" data-description="Natural material and grain inspiration for decorative wood surfaces.">VIEW DESIGN ↗</button>
      </div>
      <div class="card-info"><div><h3>Natural Textures</h3><p>Wood · Organic</p></div><span class="card-number">03</span></div>
    </article>

    <article class="card" data-category="Wallpaper" data-name="wallpaper botanical interior">
      <div class="card-image">
        <img loading="lazy" src="https://images.unsplash.com/photo-1616486338812-3dadae4b4ace?auto=format&fit=crop&w=800&q=80" alt="Decorative interior wallpaper inspiration">
        <span class="card-tag">WALLPAPER</span>
        <button class="view" data-title="Interior Stories" data-category="Wallpaper" data-description="Interior styling inspiration for wallpaper and wallcovering collections.">VIEW DESIGN ↗</button>
      </div>
      <div class="card-info"><div><h3>Interior Stories</h3><p>Walls · Refined living</p></div><span class="card-number">04</span></div>
    </article>

    <article class="card" data-category="Hand Painting" data-name="hand painting art canvas">
      <div class="card-image">
        <img loading="lazy" src="https://images.unsplash.com/photo-1541961017774-22349e4a1262?auto=format&fit=crop&w=800&q=80" alt="Colourful artistic painting">
        <span class="card-tag">HAND PAINTING</span>
        <button class="view" data-title="Art in Colour" data-category="Hand Painting" data-description="Expressive artwork and colour inspiration for hand-painted creative projects.">VIEW DESIGN ↗</button>
      </div>
      <div class="card-info"><div><h3>Art in Colour</h3><p>Artwork · Expression</p></div><span class="card-number">05</span></div>
    </article>

    <article class="card" data-category="Patterns" data-name="patterns textile geometric design">
      <div class="card-image">
        <img loading="lazy" src="https://images.unsplash.com/photo-1490481651871-ab68de25d43d?auto=format&fit=crop&w=800&q=80" alt="Textile and fashion pattern inspiration">
        <span class="card-tag">PATTERNS</span>
        <button class="view" data-title="Pattern Language" data-category="Patterns" data-description="Pattern and colour references for textile and surface design development.">VIEW DESIGN ↗</button>
      </div>
      <div class="card-info"><div><h3>Pattern Language</h3><p>Repeats · Colour stories</p></div><span class="card-number">06</span></div>
    </article>

    <article class="card" data-category="Leather" data-name="leather luxury accessories texture">
      <div class="card-image">
        <img loading="lazy" src="https://images.unsplash.com/photo-1548036328-c9fa89d128fa?auto=format&fit=crop&w=800&q=80" alt="Luxury leather accessory inspiration">
        <span class="card-tag">LEATHER</span>
        <button class="view" data-title="Luxury Surface" data-category="Leather" data-description="Luxury accessory styling and material inspiration for leather print concepts.">VIEW DESIGN ↗</button>
      </div>
      <div class="card-info"><div><h3>Luxury Surface</h3><p>Accessories · Premium</p></div><span class="card-number">07</span></div>
    </article>

    <article class="card" data-category="Wallpaper" data-name="wallpaper abstract architecture">
      <div class="card-image">
        <img loading="lazy" src="https://images.unsplash.com/photo-1600607687939-ce8a6c25118c?auto=format&fit=crop&w=800&q=80" alt="Minimal modern architectural interior">
        <span class="card-tag">WALLPAPER</span>
        <button class="view" data-title="Quiet Geometry" data-category="Wallpaper" data-description="Minimal architectural inspiration for modern wallcovering concepts.">VIEW DESIGN ↗</button>
      </div>
      <div class="card-info"><div><h3>Quiet Geometry</h3><p>Minimal · Architecture</p></div><span class="card-number">08</span></div>
    </article>

    <article class="card" data-category="Patterns" data-name="patterns colours abstract art">
      <div class="card-image">
        <img loading="lazy" src="https://images.unsplash.com/photo-1549490349-8643362247b5?auto=format&fit=crop&w=800&q=80" alt="Abstract artwork and bold colours">
        <span class="card-tag">PATTERNS</span>
        <button class="view" data-title="Colour in Motion" data-category="Patterns" data-description="Abstract shapes and bold colour ideas for experimental surface collections.">VIEW DESIGN ↗</button>
      </div>
      <div class="card-info"><div><h3>Colour in Motion</h3><p>Abstract · Modern</p></div><span class="card-number">09</span></div>
    </article>

  </div>
  <p class="empty" id="empty">No designs found. Try another search or category.</p>
  <p class="hero-note">Sample imagery is for visual inspiration. Replace it with your own approved office designs before presenting this as your actual production catalogue.</p>
</section>

<section class="wrap" id="process">
  <div class="eyebrow">From idea to application</div>
  <h2>Designed with purpose.</h2>
  <div class="process reveal">
    <article><small>01 / DISCOVER</small><h3>Explore</h3><p>Browse patterns, colours, materials and creative directions for new projects.</p></article>
    <article><small>02 / DEVELOP</small><h3>Refine</h3><p>Prepare artwork, review colour references and evaluate material suitability.</p></article>
    <article><small>03 / PRODUCE</small><h3>Realise</h3><p>Move from approved artwork to sampling and production after the necessary tests.</p></article>
  </div>
</section>

<section class="wrap" id="contact">
  <div class="contact reveal">
    <div>
      <div class="eyebrow">Have a project in mind?</div>
      <h2>Let's create something distinctive.</h2>
      <p>Interested in a design, custom pattern or printing application? Get in touch to discuss the requirements.</p>
    </div>
    <a class="btn primary" href="mailto:YOUR-EMAIL@example.com?subject=Digital%20Printing%20Enquiry">SEND AN ENQUIRY ↗</a>
  </div>
</section>
</main>

<footer>
  <div class="wrap footer-inner">
    <span>PRINT ATELIER. · Digital Printing & Surface Design</span>
    <span>Creative portfolio · © <span id="year"></span></span>
  </div>
</footer>

<div class="modal" id="modal" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
  <div class="modal-box">
    <button class="close" id="close" aria-label="Close preview">×</button>
    <img id="modalImage" src="" alt="">
    <h3 id="modalTitle"></h3>
    <p id="modalDescription"></p>
  </div>
</div>

<script>
const cards = [...document.querySelectorAll('.card')];
const chips = [...document.querySelectorAll('.chip')];
const search = document.getElementById('search');
const empty = document.getElementById('empty');
let activeCategory = 'all';

function filterCards() {
  const query = search.value.trim().toLowerCase();
  let count = 0;

  cards.forEach(card => {
    const matchesCategory =
      activeCategory === 'all' ||
      card.dataset.category === activeCategory;
    const matchesSearch =
      card.dataset.name.toLowerCase().includes(query) ||
      card.querySelector('h3').textContent.toLowerCase().includes(query);

    const show = matchesCategory && matchesSearch;
    card.classList.toggle('hidden', !show);
    if (show) count++;
  });

  empty.style.display = count ? 'none' : 'block';
}

chips.forEach(chip => {
  chip.addEventListener('click', () => {
    activeCategory = chip.dataset.category;
    chips.forEach(item => item.classList.toggle('active', item === chip));
    filterCards();
  });
});

search.addEventListener('input', filterCards);

const modal = document.getElementById('modal');
const modalImage = document.getElementById('modalImage');
const modalTitle = document.getElementById('modalTitle');
const modalDescription = document.getElementById('modalDescription');
const closeButton = document.getElementById('close');

cards.forEach(card => {
  card.querySelector('.view').addEventListener('click', event => {
    const button = event.currentTarget;
    modalImage.src = card.querySelector('img').src;
    modalImage.alt = button.dataset.title;
    modalTitle.textContent = button.dataset.title;
    modalDescription.textContent =
      button.dataset.category + ' · ' + button.dataset.description;
    modal.classList.add('open');
    closeButton.focus();
  });
});

function closeModal() {
  modal.classList.remove('open');
}

closeButton.addEventListener('click', closeModal);
modal.addEventListener('click', event => {
  if (event.target === modal) closeModal();
});
document.addEventListener('keydown', event => {
  if (event.key === 'Escape') closeModal();
});

const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
      observer.unobserve(entry.target);
    }
  });
}, {threshold: 0.12});

document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
document.getElementById('year').textContent = new Date().getFullYear();
</script>

</body>
</html>
