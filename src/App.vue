<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import parkSmartLogo from "../ParkSmartLogo.png";

import {
  BarChart3,
  Leaf,
  ShieldCheck,
  CalendarDays,
  ParkingCircle,
  MonitorSmartphone,
  Users,
  Car,
} from "lucide-vue-next";

const activeSection = ref("overview");

const sections = [
  "overview",
  "goals",
  "team",
];

const handleScroll = () => {
  let current = "overview";

  for (const id of sections) {
    const section = document.getElementById(id);

    if (section && section.getBoundingClientRect().top <= 180) {
      current = id;
    }
  }

  activeSection.value = current;
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
  handleScroll();
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <div class="page">
    <!-- HEADER -->
    <header class="site-header">
      <div class="nav-container">
        <a class="brand" href="#">
        <img
        :src="parkSmartLogo"
        alt="ParkSmart logo"
        class="nav-logo"
        />
  <div>
    <strong>ParkSmart</strong>
    <span>CSC 375 Project Charter</span>
  </div>
</a>

        <nav>
          <a
            v-for="item in sections"
            :key="item"
            :href="`#${item}`"
            :class="{ active: activeSection === item }"
          >
            {{ item.charAt(0).toUpperCase() + item.slice(1) }}
          </a>
        </nav>
      </div>
    </header>

    <main>
      <!-- HERO -->
    <section class="hero">
      <div class="hero-inner">
        <img
          :src="parkSmartLogo"
          alt="ParkSmart"
          class="hero-logo"
        />

        <div class="uvic-label">
          <span></span>
          University of Victoria
        </div>
        <h1>ParkSmart</h1>

          <h2>
            Automated Parking Capacity Monitoring and Historical Data Analytics
            Solution
          </h2>

          <p>
            A proposed parking availability and data analytics solution for the
            University of Victoria.
          </p>

          <div class="hero-actions">
            <a href="#overview" class="primary-button">
              Explore Project
            </a>

           <a href="#team" class="secondary-button">
            <Users :size="18" />
            Meet the Team
          </a>
          </div>

          <div class="project-meta">
            <span>CSC 375</span>
            <span>October 7, 2026</span>
          </div>
        </div>
      </section>

      <!-- OVERVIEW -->
      <section id="overview" class="content-section">
        <div class="section-heading">
          <span>01</span>

          <div>
            <p>Project Overview</p>
            <h2>Why ParkSmart?</h2>
          </div>
        </div>

        <div class="overview-layout">
          <div class="overview-text">
            <p>
              ParkSmart addresses the limitations of UVic’s current static
              parking information by providing a centralized view of current
              parking availability and historical parking trends.
            </p>

            <p>
              The system is intended to reduce time spent searching for parking,
              decrease congestion and unnecessary vehicle idling, and support
              better administrative planning.
            </p>
          </div>

          <div class="overview-points">
            <article>
              <Car />
              <div>
                <strong>Less Searching</strong>
                <span>Help drivers identify suitable parking faster.</span>
              </div>
            </article>

            <article>
              <Leaf />
              <div>
                <strong>Lower Emissions</strong>
                <span>Reduce unnecessary idling and congestion.</span>
              </div>
            </article>

            <article>
              <BarChart3 />
              <div>
                <strong>Better Planning</strong>
                <span>Use parking data to support future decisions.</span>
              </div>
            </article>
          </div>
        </div>
      </section>

      <!-- GOALS -->
      <section id="goals" class="content-section alt">
        <div class="section-heading">
          <span>02</span>

          <div>
            <p>Project Goals</p>
            <h2>What ParkSmart aims to achieve</h2>
          </div>
        </div>

        <div class="goal-grid">
          <article class="goal-card">
            <div class="icon-box">
              <MonitorSmartphone />
            </div>

            <h3>System Design & Prototyping</h3>

            <p>
              Develop a working prototype showing real-time parking
              availability, available spaces, and historical parking trends
              through a simple interface.
            </p>
          </article>

          <article class="goal-card">
            <div class="icon-box">
              <Leaf />
            </div>

            <h3>Efficiency & Emission Reduction</h3>

            <p>
              Reduce the amount of time spent looking for parking by at least
              30%, while also reducing emissions caused by unnecessary vehicle
              idling.
            </p>
          </article>

          <article class="goal-card">
            <div class="icon-box">
              <BarChart3 />
            </div>

            <h3>Data Driven Administration</h3>

            <p>
              Collect and analyze real-time and historical parking data to
              identify peak hours, popular lots, and common usage patterns.
            </p>
          </article>

          <article class="goal-card">
            <div class="icon-box">
              <ShieldCheck />
            </div>

            <h3>Regulatory Compliance</h3>

            <p>
              Ensure that the system follows appropriate privacy and data
              management guidelines.
            </p>
          </article>
        </div>
      </section>

      <!-- TEAM -->
      <!-- TEAM -->
    <section id="team" class="content-section">
      <div class="section-heading">
        <span>03</span>

        <div>
          <p>Project Organization</p>
          <h2>Team</h2>
        </div>
      </div>

      <div class="team-grid">
        <article>
          <div class="avatar">AT</div>
          <strong>Amanda Tu</strong>
          <span>Project Manager</span>
          <a class="team-email" href="mailto:atu@uvic.ca">
            atu@uvic.ca
          </a>
        </article>

        <article>
          <div class="avatar">JK</div>
          <strong>Jonah Kisakye</strong>
          <span>Frontend Developer</span>
          <a class="team-email" href="mailto:JonahKisakye@uvic.ca">
            JonahKisakye@uvic.ca
          </a>
        </article>

        <article>
          <div class="avatar">EP</div>
          <strong>Echo Parratt</strong>
          <span>Backend Developer</span>
          <a class="team-email" href="mailto:eparratt@uvic.ca">
            eparratt@uvic.ca
          </a>
        </article>

        <article>
          <div class="avatar">JH</div>
          <strong>Jana Hassan</strong>
          <span>UI/UX Designer</span>
          <a class="team-email" href="mailto:jhassan@uvic.ca">
            jhassan@uvic.ca
          </a>
        </article>

        <article>
          <div class="avatar">RD</div>
          <strong>Rob Dimmitt</strong>
          <span>Business Analyst</span>
          <a class="team-email" href="mailto:rdimmitt@uvic.ca">
            rdimmitt@uvic.ca
          </a>
        </article>
      </div>
    </section>

    </main>
    <div class="footer-brand">
      </div>
    </div>
</template>

<style>
:root {
  font-family:
    Inter,
    -apple-system,
    BlinkMacSystemFont,
    "Segoe UI",
    sans-serif;

  --navy: #002754;
  --blue: #005493;
  --green: #008538;
  --yellow: #f5aa1c;

  --text: #17212b;
  --muted: #65727e;
  --border: #dfe5ea;
  --soft-bg: #f6f8fa;

  color: var(--text);
  background: white;
}

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
}

a {
  color: inherit;
  text-decoration: none;
}

/* HEADER */

.site-header {
  position: sticky;
  top: 0;
  z-index: 100;

  background: rgba(0, 39, 84, 0.97);

  backdrop-filter: blur(12px);
}

.nav-container {
  width: min(1100px, 90%);
  min-height: 72px;

  margin: auto;

  display: flex;
  justify-content: space-between;
  align-items: center;
}

.brand {
  display: flex;
  align-items: center;
  gap: 12px;

  color: white;
}

.brand-icon {
  display: flex;
  justify-content: center;
  align-items: center;

  width: 40px;
  height: 40px;

  border-radius: 9px;

  background: var(--blue);
}

.brand > div:last-child {
  display: flex;
  flex-direction: column;
}

.brand strong {
  font-size: 1rem;
}

.brand span {
  margin-top: 2px;

  color: #b9ccdc;

  font-size: 0.72rem;
}

nav {
  display: flex;
  gap: 8px;
}

nav a {
  padding: 8px 12px;

  border-radius: 6px;

  color: #c9d7e3;

  font-size: 0.86rem;

  transition: 0.2s;
}

nav a:hover,
nav a.active {
  background: rgba(255, 255, 255, 0.1);
  color: white;
}

/* HERO */

.hero {
  background:
    radial-gradient(
      circle at 80% 20%,
      rgba(0, 133, 56, 0.07),
      transparent 35%
    ),
    linear-gradient(180deg, #f7f9fb, white);

  border-bottom: 1px solid var(--border);
}

.hero-inner {
  width: min(900px, 90%);
  margin: auto;

  padding: 90px 0;

  text-align: center;
}

.uvic-label {
  display: flex;
  align-items: center;
  justify-content: center;

  gap: 8px;

  color: var(--green);

  font-size: 0.76rem;
  font-weight: 800;

  letter-spacing: 0.12em;
  text-transform: uppercase;
}

.uvic-label span {
  width: 25px;
  height: 3px;

  background: var(--yellow);
}

.hero h1 {
  margin: 15px 0 0;

  color: var(--navy);

  font-size: clamp(4rem, 8vw, 6rem);

  letter-spacing: -0.06em;
  line-height: 1;
}

.hero h2 {
  max-width: 760px;

  margin: 22px auto 0;

  color: #31465d;

  font-size: clamp(1.2rem, 2vw, 1.55rem);
  font-weight: 500;

  line-height: 1.45;
}

.hero > .hero-inner > p {
  max-width: 620px;

  margin: 20px auto 0;

  color: var(--muted);

  line-height: 1.7;
}

.hero-actions {
  display: flex;
  justify-content: center;

  gap: 12px;

  margin-top: 28px;
}

.primary-button,
.secondary-button {
  display: flex;
  align-items: center;

  gap: 8px;

  padding: 11px 18px;

  border-radius: 7px;

  font-size: 0.9rem;
  font-weight: 700;

  transition:
    transform 0.2s,
    box-shadow 0.2s;
}

.primary-button {
  background: var(--navy);
  color: white;
}

.secondary-button {
  background: white;

  border: 1px solid #ccd5dc;

  color: var(--navy);
}

.primary-button:hover,
.secondary-button:hover {
  transform: translateY(-2px);

  box-shadow: 0 8px 20px rgba(0, 39, 84, 0.1);
}

.project-meta {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;

  gap: 22px;

  margin-top: 34px;

  color: #6b7782;

  font-size: 0.78rem;
}

.project-meta span:not(:first-child)::before {
  content: "•";

  margin-right: 22px;

  color: var(--yellow);
}

/* SECTIONS */

.content-section {
  width: min(1050px, 90%);

  margin: auto;

  padding: 85px 0;

  scroll-margin-top: 70px;
}

.content-section.alt {
  width: 100%;

  padding-left: max(5%, calc((100% - 1050px) / 2));
  padding-right: max(5%, calc((100% - 1050px) / 2));

  background: var(--soft-bg);
}

.section-heading {
  display: flex;
  align-items: flex-start;

  gap: 14px;

  margin-bottom: 34px;
}

.section-heading > span {
  margin-top: 5px;

  color: var(--blue);

  font-size: 0.75rem;
  font-weight: 800;
}

.section-heading p {
  margin: 0 0 5px;

  color: var(--green);

  font-size: 0.72rem;
  font-weight: 800;

  letter-spacing: 0.12em;
  text-transform: uppercase;
}

.section-heading h2 {
  margin: 0;

  color: var(--navy);

  font-size: clamp(2rem, 4vw, 2.8rem);

  letter-spacing: -0.035em;
}

/* OVERVIEW */

.overview-layout {
  display: grid;

  grid-template-columns: 1.2fr 0.8fr;

  gap: 65px;
}

.overview-text p {
  margin-top: 0;

  color: #596975;

  line-height: 1.85;
}

.overview-points {
  display: flex;
  flex-direction: column;

  gap: 12px;
}

.overview-points article {
  display: flex;
  align-items: center;

  gap: 14px;

  padding: 17px;

  border: 1px solid var(--border);

  border-radius: 10px;

  background: white;

  transition:
    transform 0.2s,
    box-shadow 0.2s;
}

.overview-points article:hover {
  transform: translateX(4px);

  box-shadow: 0 7px 20px rgba(0, 39, 84, 0.07);
}

.overview-points svg {
  color: var(--blue);
}

.overview-points div {
  display: flex;
  flex-direction: column;
}

.overview-points strong {
  color: var(--navy);

  font-size: 0.88rem;
}

.overview-points span {
  margin-top: 3px;

  color: var(--muted);

  font-size: 0.75rem;
}

/* GOALS */

.goal-grid {
  display: grid;

  grid-template-columns: repeat(2, 1fr);

  gap: 18px;
}

.goal-card {
  padding: 26px;

  background: white;

  border: 1px solid #dce3e8;
  border-radius: 12px;

  transition:
    transform 0.2s,
    box-shadow 0.2s;
}

.goal-card:hover {
  transform: translateY(-4px);

  box-shadow: 0 12px 35px rgba(0, 39, 84, 0.08);
}

.icon-box {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 43px;
  height: 43px;

  margin-bottom: 20px;

  border-radius: 9px;

  background: #eaf2f8;

  color: var(--blue);
}

.goal-card h3 {
  margin: 0 0 10px;

  color: var(--navy);

  font-size: 1.05rem;
}

.goal-card p {
  margin: 0;

  color: var(--muted);

  line-height: 1.7;

  font-size: 0.88rem;
}

/* TIMELINE */

.timeline {
  position: relative;

  max-width: 760px;
}

.timeline::before {
  content: "";

  position: absolute;

  top: 15px;
  bottom: 20px;
  left: 15px;

  width: 2px;

  background: #cfd8df;
}

.timeline-item {
  position: relative;

  display: flex;

  gap: 20px;

  padding-bottom: 28px;
}

.timeline-dot {
  position: relative;
  z-index: 2;

  flex-shrink: 0;

  width: 32px;
  height: 32px;

  border: 8px solid var(--soft-bg);
  border-radius: 50%;

  background: #cdd7de;
}

.timeline-item.completed .timeline-dot {
  background: var(--green);
}

.timeline-content {
  display: flex;
  flex-direction: column;

  padding-top: 2px;
}

.timeline-content span {
  color: var(--blue);

  font-size: 0.74rem;
  font-weight: 700;
}

.timeline-content strong {
  margin-top: 3px;

  color: var(--navy);
}

/* TEAM */

.team-grid {
  display: grid;

  grid-template-columns: repeat(5, 1fr);

  gap: 14px;
}

.team-grid article {
  padding: 24px 15px;

  text-align: center;

  background: white;

  border: 1px solid var(--border);
  border-radius: 10px;

  transition:
    transform 0.2s,
    box-shadow 0.2s;
}

.team-grid article:hover {
  transform: translateY(-4px);

  box-shadow: 0 10px 30px rgba(0, 39, 84, 0.07);
}

.avatar {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 52px;
  height: 52px;

  margin: 0 auto 13px;

  border-radius: 50%;

  background: var(--navy);

  color: white;

  font-size: 0.8rem;
  font-weight: 800;
}

.team-grid strong {
  display: block;

  color: var(--navy);

  font-size: 0.9rem;
}

.team-grid span {
  display: block;

  margin-top: 5px;

  color: var(--muted);

  font-size: 0.72rem;
}

/* FOOTER */

footer {
  padding: 35px 5%;

  background: var(--navy);

  color: white;
}

footer > div {
  width: min(1050px, 100%);

  margin: auto;

  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-brand {
  display: flex;
  align-items: center;

  gap: 8px;
}

footer span {
  color: #aebfd0;

  font-size: 0.76rem;
}

/* RESPONSIVE */
/* LOGOS */

.nav-logo {
  width: 38px;
  height: 38px;
  max-width: 38px;
  object-fit: contain;
  background: white;
  border-radius: 8px;
  padding: 3px;
}

.hero-logo {
  width: 90px;
  height: 90px;
  max-width: 90px;
  object-fit: contain;
  margin: 0 auto 18px;
  background: white;
  border-radius: 18px;
  padding: 6px;
  box-shadow: 0 8px 24px rgba(0, 39, 84, 0.08);
}

.footer-logo {
  width: 30px;
  height: 30px;
  max-width: 30px;
  object-fit: contain;
  background: white;
  border-radius: 6px;
  padding: 2px;
}

.team-email {
  display: block;
  margin-top: 9px;
  color: var(--blue);
  font-size: 0.72rem;
  word-break: break-word;
}

.team-email:hover {
  color: var(--green);
  text-decoration: underline;
}

img {
  max-width: 100%;
  height: auto;
}

/* RESPONSIVE */

@media (max-width: 850px) {
  nav {
    display: none;
  }

  .overview-layout,
  .goal-grid {
    grid-template-columns: 1fr;
  }

  .team-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 550px) {
  .hero-inner {
    padding: 70px 0;
  }

  .hero h1 {
    font-size: 3.8rem;
  }

  .hero-actions {
    flex-direction: column;
    align-items: center;
  }

  .team-grid {
    grid-template-columns: 1fr;
  }

  footer > div {
    flex-direction: column;
    align-items: flex-start;
    gap: 10px;
  }
}

</style>