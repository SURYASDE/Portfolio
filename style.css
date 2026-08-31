:root {
  --bg: #0A0A08;
  --bg2: #111110;
  --bg3: #1A1A18;
  --surface: #1E1E1C;
  --border: #2A2A28;
  --border2: #333330;
  --text: #E8E6DF;
  --text2: #9A9890;
  --text3: #5A5855;
  --accent: #C8F060;
  --accent2: #A8D040;
  --accent-dim: rgba(200, 240, 96, 0.08);
  --accent-dim2: rgba(200, 240, 96, 0.15);
  --teal: #60D0C8;
  --coral: #F08060;
  --font-display: 'Syne', sans-serif;
  --font-mono: 'DM Mono', monospace;
  --font-serif: 'Instrument Serif', serif;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--font-display);
  overflow-x: hidden;
  cursor: none;
}

/* Custom cursor */
.cursor {
  position: fixed;
  width: 8px; height: 8px;
  background: var(--accent);
  border-radius: 50%;
  pointer-events: none;
  z-index: 9999;
  transition: transform 0.1s ease;
  mix-blend-mode: difference;
}
.cursor-ring {
  position: fixed;
  width: 32px; height: 32px;
  border: 1px solid rgba(200,240,96,0.4);
  border-radius: 50%;
  pointer-events: none;
  z-index: 9998;
  transition: all 0.15s ease;
}

/* Noise overlay */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
  pointer-events: none;
  z-index: 1000;
  opacity: 0.4;
}

/* NAV */
nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  padding: 1.25rem 2.5rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid transparent;
  transition: all 0.3s ease;
}
nav.scrolled {
  background: rgba(10,10,8,0.85);
  backdrop-filter: blur(20px);
  border-bottom-color: var(--border);
}
.nav-logo {
  font-family: var(--font-mono);
  font-size: 13px;
  color: var(--accent);
  letter-spacing: 0.05em;
}
.nav-links {
  display: flex;
  gap: 2rem;
  list-style: none;
}
.nav-links a {
  font-family: var(--font-mono);
  font-size: 12px;
  color: var(--text2);
  text-decoration: none;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--accent); }

/* HERO */
.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 2.5rem;
  position: relative;
  overflow: hidden;
}

.hero-grid-bg {
  position: absolute;
  inset: 0;
  background-image:
    linear-gradient(rgba(200,240,96,0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(200,240,96,0.03) 1px, transparent 1px);
  background-size: 60px 60px;
  mask-image: radial-gradient(ellipse 80% 80% at 50% 50%, black, transparent);
}

.hero-orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(80px);
  pointer-events: none;
}
.hero-orb-1 {
  width: 500px; height: 500px;
  background: radial-gradient(circle, rgba(200,240,96,0.12), transparent 70%);
  top: -100px; right: -100px;
}
.hero-orb-2 {
  width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(96,208,200,0.08), transparent 70%);
  bottom: -50px; left: 20%;
}

.hero-content {
  position: relative;
  z-index: 2;
  max-width: 900px;
}

.hero-tag {
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--accent);
  letter-spacing: 0.15em;
  text-transform: uppercase;
  margin-bottom: 2rem;
  display: flex;
  align-items: center;
  gap: 0.75rem;
  opacity: 0;
  animation: fadeUp 0.6s ease 0.2s forwards;
}
.hero-tag::before {
  content: '';
  width: 24px; height: 1px;
  background: var(--accent);
}

.hero-name {
  font-size: clamp(3rem, 8vw, 7rem);
  font-weight: 800;
  line-height: 0.95;
  letter-spacing: -0.03em;
  margin-bottom: 1.5rem;
  opacity: 0;
  animation: fadeUp 0.6s ease 0.4s forwards;
}
.hero-name .line2 {
  color: transparent;
  -webkit-text-stroke: 1px rgba(232,230,223,0.3);
}
.hero-name .accent-word {
  color: var(--accent);
  font-style: italic;
  font-family: var(--font-serif);
}

.hero-desc {
  font-family: var(--font-mono);
  font-size: 14px;
  color: var(--text2);
  line-height: 1.8;
  max-width: 520px;
  margin-bottom: 3rem;
  opacity: 0;
  animation: fadeUp 0.6s ease 0.6s forwards;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  align-items: center;
  opacity: 0;
  animation: fadeUp 0.6s ease 0.8s forwards;
  flex-wrap: wrap;
}

.btn-primary {
  background: var(--accent);
  color: var(--bg);
  padding: 0.875rem 2rem;
  border-radius: 4px;
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 13px;
  letter-spacing: 0.05em;
  text-decoration: none;
  text-transform: uppercase;
  transition: all 0.2s ease;
  border: none;
  cursor: none;
}
.btn-primary:hover {
  background: var(--accent2);
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(200,240,96,0.2);
}

.btn-ghost {
  border: 1px solid var(--border2);
  color: var(--text2);
  padding: 0.875rem 2rem;
  border-radius: 4px;
  font-family: var(--font-mono);
  font-size: 12px;
  letter-spacing: 0.05em;
  text-decoration: none;
  transition: all 0.2s ease;
  cursor: none;
}
.btn-ghost:hover {
  border-color: var(--accent);
  color: var(--accent);
}

.hero-scroll {
  position: absolute;
  bottom: 2.5rem;
  left: 2.5rem;
  display: flex;
  align-items: center;
  gap: 0.75rem;
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--text3);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  opacity: 0;
  animation: fadeUp 0.6s ease 1.2s forwards;
}
.scroll-line {
  width: 40px; height: 1px;
  background: var(--text3);
  animation: scrollLine 2s ease infinite;
}

.hero-stats {
  position: absolute;
  bottom: 2.5rem;
  right: 2.5rem;
  display: flex;
  gap: 2.5rem;
  opacity: 0;
  animation: fadeUp 0.6s ease 1s forwards;
}
.stat { text-align: right; }
.stat-num {
  font-size: 2rem;
  font-weight: 800;
  color: var(--accent);
  line-height: 1;
}
.stat-label {
  font-family: var(--font-mono);
  font-size: 10px;
  color: var(--text3);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  margin-top: 4px;
}

/* SECTIONS */
section {
  padding: 7rem 2.5rem;
  position: relative;
}

.section-header {
  display: flex;
  align-items: baseline;
  gap: 1.5rem;
  margin-bottom: 4rem;
}
.section-num {
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--accent);
  letter-spacing: 0.1em;
}
.section-title {
  font-size: clamp(2rem, 4vw, 3.5rem);
  font-weight: 800;
  letter-spacing: -0.03em;
  line-height: 1;
}
.section-line {
  flex: 1;
  height: 1px;
  background: var(--border);
  margin-left: auto;
  max-width: 200px;
}

/* ABOUT */
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: start;
}

.about-text p {
  font-size: 16px;
  line-height: 1.8;
  color: var(--text2);
  margin-bottom: 1.5rem;
}
.about-text p strong {
  color: var(--text);
  font-weight: 600;
}
.about-text .highlight {
  color: var(--accent);
  font-style: italic;
  font-family: var(--font-serif);
  font-size: 18px;
}

.about-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 2rem;
  position: relative;
  overflow: hidden;
}
.about-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 2px;
  background: linear-gradient(90deg, var(--accent), transparent);
}

.about-card-label {
  font-family: var(--font-mono);
  font-size: 10px;
  color: var(--accent);
  letter-spacing: 0.15em;
  text-transform: uppercase;
  margin-bottom: 1.5rem;
}

.education-item {
  margin-bottom: 1.5rem;
  padding-bottom: 1.5rem;
  border-bottom: 1px solid var(--border);
}
.education-item:last-child { border-bottom: none; margin-bottom: 0; padding-bottom: 0; }
.edu-degree { font-size: 14px; font-weight: 600; color: var(--text); }
.edu-school { font-size: 13px; color: var(--text2); margin: 4px 0; }
.edu-year {
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--text3);
  letter-spacing: 0.05em;
}

.achieve-item {
  display: flex;
  gap: 0.75rem;
  align-items: flex-start;
  margin-bottom: 1rem;
  font-size: 13px;
  color: var(--text2);
  line-height: 1.5;
}
.achieve-dot {
  width: 6px; height: 6px;
  border-radius: 50%;
  background: var(--accent);
  flex-shrink: 0;
  margin-top: 6px;
}

/* SKILLS */
.skills-section { background: var(--bg2); }

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
}

.skill-category {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 1.75rem;
  transition: border-color 0.2s, transform 0.2s;
}
.skill-category:hover {
  border-color: var(--border2);
  transform: translateY(-4px);
}

.skill-cat-header {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 1.5rem;
}
.skill-cat-icon {
  width: 32px; height: 32px;
  border-radius: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 16px;
}
.skill-cat-title {
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--text2);
  letter-spacing: 0.1em;
  text-transform: uppercase;
}

.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}
.skill-tag {
  background: var(--bg3);
  border: 1px solid var(--border);
  color: var(--text2);
  font-family: var(--font-mono);
  font-size: 12px;
  padding: 0.375rem 0.75rem;
  border-radius: 4px;
  transition: all 0.2s;
}
.skill-tag:hover, .skill-tag.highlight {
  background: var(--accent-dim);
  border-color: rgba(200,240,96,0.3);
  color: var(--accent);
}

/* EXPERIENCE */
.exp-timeline {
  position: relative;
  padding-left: 2rem;
}
.exp-timeline::before {
  content: '';
  position: absolute;
  left: 0; top: 8px; bottom: 0;
  width: 1px;
  background: linear-gradient(to bottom, var(--accent), transparent);
}

.exp-item {
  position: relative;
  margin-bottom: 4rem;
  opacity: 0;
  transform: translateX(-20px);
  transition: all 0.6s ease;
}
.exp-item.visible {
  opacity: 1;
  transform: translateX(0);
}

.exp-dot {
  position: absolute;
  left: -2.375rem;
  top: 4px;
  width: 10px; height: 10px;
  border-radius: 50%;
  background: var(--accent);
  border: 2px solid var(--bg);
  box-shadow: 0 0 0 4px var(--accent-dim2);
}

.exp-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 0.5rem;
  flex-wrap: wrap;
  gap: 0.5rem;
}
.exp-role {
  font-size: 20px;
  font-weight: 700;
  letter-spacing: -0.02em;
}
.exp-date {
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--text3);
  letter-spacing: 0.05em;
  background: var(--surface);
  border: 1px solid var(--border);
  padding: 4px 10px;
  border-radius: 999px;
}
.exp-company {
  font-size: 14px;
  color: var(--accent);
  font-family: var(--font-mono);
  margin-bottom: 1.25rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}
.exp-type {
  font-size: 10px;
  color: var(--text3);
  background: var(--surface);
  border: 1px solid var(--border);
  padding: 2px 8px;
  border-radius: 999px;
  letter-spacing: 0.05em;
}

.exp-bullets {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}
.exp-bullets li {
  font-size: 14px;
  color: var(--text2);
  line-height: 1.6;
  padding-left: 1.25rem;
  position: relative;
}
.exp-bullets li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: var(--accent);
  font-size: 12px;
}
.exp-bullets li strong {
  color: var(--text);
  font-weight: 500;
}

/* PROJECTS */
.projects-section { background: var(--bg2); }

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
  gap: 1.5rem;
}

.project-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 2rem;
  position: relative;
  overflow: hidden;
  transition: all 0.3s ease;
}
.project-card:hover {
  border-color: rgba(200,240,96,0.3);
  transform: translateY(-6px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.4), 0 0 0 1px rgba(200,240,96,0.1);
}

.project-card-num {
  font-family: var(--font-mono);
  font-size: 10px;
  color: var(--text3);
  letter-spacing: 0.1em;
  margin-bottom: 1.5rem;
}

.project-card-title {
  font-size: 20px;
  font-weight: 700;
  letter-spacing: -0.02em;
  margin-bottom: 0.75rem;
  color: var(--text);
  transition: color 0.2s;
}
.project-card:hover .project-card-title { color: var(--accent); }

.project-card-desc {
  font-size: 13px;
  color: var(--text2);
  line-height: 1.7;
  margin-bottom: 1.5rem;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
  margin-bottom: 1.5rem;
}
.project-tag {
  font-family: var(--font-mono);
  font-size: 10px;
  letter-spacing: 0.08em;
  padding: 3px 8px;
  border-radius: 3px;
  background: var(--bg3);
  border: 1px solid var(--border);
  color: var(--text3);
}

.project-links {
  display: flex;
  gap: 1rem;
  align-items: center;
}
.project-link {
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--text3);
  text-decoration: none;
  letter-spacing: 0.05em;
  display: flex;
  align-items: center;
  gap: 0.4rem;
  transition: color 0.2s;
}
.project-link:hover { color: var(--accent); }

.project-card-bg {
  position: absolute;
  top: -20px; right: -20px;
  width: 120px; height: 120px;
  border-radius: 50%;
  opacity: 0.04;
  transition: opacity 0.3s;
}
.project-card:hover .project-card-bg { opacity: 0.08; }

/* CONTACT */
.contact-section {
  text-align: center;
  padding: 8rem 2.5rem;
  position: relative;
  overflow: hidden;
}

.contact-orb {
  position: absolute;
  width: 600px; height: 600px;
  border-radius: 50%;
  background: radial-gradient(circle, rgba(200,240,96,0.06), transparent 70%);
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  pointer-events: none;
}

.contact-eyebrow {
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--accent);
  letter-spacing: 0.15em;
  text-transform: uppercase;
  margin-bottom: 1.5rem;
}
.contact-title {
  font-size: clamp(2.5rem, 6vw, 5rem);
  font-weight: 800;
  letter-spacing: -0.04em;
  line-height: 1;
  margin-bottom: 1.5rem;
}
.contact-title em {
  font-family: var(--font-serif);
  font-weight: 400;
  color: var(--accent);
}
.contact-sub {
  font-size: 15px;
  color: var(--text2);
  line-height: 1.7;
  max-width: 480px;
  margin: 0 auto 3rem;
  font-family: var(--font-mono);
}

.contact-links {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
  margin-bottom: 4rem;
}

.contact-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 1rem 1.5rem;
  display: flex;
  align-items: center;
  gap: 0.75rem;
  text-decoration: none;
  color: var(--text2);
  font-family: var(--font-mono);
  font-size: 13px;
  transition: all 0.2s;
  cursor: pointer;
}
.contact-card:hover {
  border-color: rgba(200,240,96,0.3);
  color: var(--accent);
  transform: translateY(-2px);
}
.contact-card-icon { font-size: 18px; }

/* FOOTER */
footer {
  border-top: 1px solid var(--border);
  padding: 2rem 2.5rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--text3);
  letter-spacing: 0.05em;
  flex-wrap: wrap;
  gap: 1rem;
}

/* ANIMATIONS */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes scrollLine {
  0%, 100% { transform: scaleX(1); opacity: 1; }
  50% { transform: scaleX(0.5); opacity: 0.5; }
}

.reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.7s ease;
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* FLOATING BADGE */
.availability-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: rgba(200,240,96,0.08);
  border: 1px solid rgba(200,240,96,0.2);
  border-radius: 999px;
  padding: 0.4rem 1rem;
  font-family: var(--font-mono);
  font-size: 11px;
  color: var(--accent);
  letter-spacing: 0.08em;
  margin-bottom: 2rem;
  opacity: 0;
  animation: fadeUp 0.6s ease 0.1s forwards;
}
.badge-dot {
  width: 6px; height: 6px;
  border-radius: 50%;
  background: var(--accent);
  animation: pulse 2s ease infinite;
}
@keyframes pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.5; transform: scale(0.8); }
}

/* MARQUEE */
.marquee-section {
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
  padding: 1.25rem 0;
  overflow: hidden;
  background: var(--bg2);
}
.marquee-track {
  display: flex;
  gap: 3rem;
  animation: marquee 20s linear infinite;
  white-space: nowrap;
}
.marquee-item {
  font-family: var(--font-mono);
  font-size: 12px;
  color: var(--text3);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  display: flex;
  align-items: center;
  gap: 1rem;
  flex-shrink: 0;
}
.marquee-sep { color: var(--accent); }
@keyframes marquee {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

/* MOBILE */
@media (max-width: 768px) {
  nav { padding: 1rem 1.25rem; }
  .nav-links { display: none; }
  section { padding: 5rem 1.25rem; }
  .hero { padding: 0 1.25rem; }
  .hero-stats { display: none; }
  .about-grid { grid-template-columns: 1fr; gap: 2rem; }
  .projects-grid { grid-template-columns: 1fr; }
  .skills-grid { grid-template-columns: 1fr; }
  footer { flex-direction: column; text-align: center; }
}
