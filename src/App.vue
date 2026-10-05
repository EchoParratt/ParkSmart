<script setup>
import { ref, onMounted, onUnmounted } from "vue";

import {
  Car,
  MapPin,
  BarChart3,
  Leaf,
  ShieldCheck,
  Users,
  CalendarDays,
  CheckCircle2,
  XCircle,
  ChevronDown,
  ParkingCircle,
  Database,
  MonitorSmartphone,
} from "lucide-vue-next";

const activeSection = ref("overview");

const scopeOpen = ref({
  inScope: true,
  outScope: true,
});

const sections = [
  "overview",
  "goals",
  "scope",
  "milestones",
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
          <div class="brand-icon">
            <ParkingCircle :size="25" />
          </div>

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
        <div class="hero-grid">
          <div class="hero-copy">
            <div class="uvic-label">
              <span></span>
              University of Victoria
            </div>

            <h1>ParkSmart</h1>

            <h2>
              Automated Parking Capacity Monitoring and Historical Data
              Analytics Solution
            </h2>

            <p>
              ParkSmart is a proposed parking availability and data analytics
              solution for the University of Victoria (UVic).
            </p>

            <div class="hero-actions">
              <a href="#overview" class="primary-button">
                Explore Project
              </a>

              <a href="#milestones" class="secondary-button">
                <CalendarDays :size="18" />
                View Timeline
              </a>
            </div>

            <div class="project-meta">
              <span>CSC 375</span>
              <span>October 5, 2026</span>
              <span>Version 1.2</span>
            </div>
          </div>

          <div class="hero-visual">
            <div class="parking-panel">
              <div class="panel-header">
                <div>
                  <span>Parking Overview</span>
                  <strong>UVic Campus</strong>
                </div>

                <div class="live-indicator">
                  <span></span>
                  Concept
                </div>
              </div>

              <div class="parking-stats">
                <div class="parking-stat">
                  <MapPin :size="22" />
                  <div>
                    <strong>3</strong>
                    <span>Lots in Scope</span>
                  </div>
                </div>

                <div class="parking-stat">
                  <BarChart3 :size="22" />
                  <div>
                    <strong>Real-time</strong>
                    <span>Availability</span>
                  </div>
                </div>

                <div class="parking-stat">
                  <Database :size="22" />
                  <div>
                    <strong>Historical</strong>
                    <span>Analytics</span>
                  </div>
                </div>
              </div>

              <div class="lot-list">
                <div class="lot">
                  <div>
                    <Car :size="18" />
                    <span>Parking Lot 1</span>
                  </div>

                  <span class="status available">In Scope</span>
                </div>

                <div class="lot">
                  <div>
                    <Car :size="18" />
                    <span>Parking Lot E</span>
                  </div>

                  <span class="status available">In Scope</span>
                </div>

                <div class="lot">
                  <div>
                    <Car :size="18" />
                    <span>CARSA Parkade</span>
                  </div>

                  <span class="status available">In Scope</span>
                </div>
              </div>
            </div>
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
          <div class="main-copy">
            <p>
              ParkSmart is a proposed parking availability and data analytics
              solution for the University of Victoria (UVic). The project
              addresses limitations in UVic’s current parking information
              system, which mainly provides static information and does not allow
              drivers to easily view current parking availability before or
              while travelling through campus.
            </p>

            <p>
              This can result in drivers spending additional time searching for
              parking, contributing to traffic congestion, delays, unnecessary
              vehicle idling, and frustration for campus users.
            </p>

            <p>
              The proposed solution will provide a centralized interface that
              displays current parking availability and historical parking
              trends, while also supporting administrative analysis of parking
              usage.
            </p>
          </div>

          <div class="problem-cards">
            <article>
              <Car />
              <div>
                <strong>Less Searching</strong>
                <span>Reduce time spent finding available parking.</span>
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
                <strong>Better Data</strong>
                <span>Support long-term parking planning.</span>
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
              Develop a working prototype to display our most important
              features. Things like real-time parking availability, available
              spaces, and historical parking trends through a simple interface.
            </p>
          </article>

          <article class="goal-card">
            <div class="icon-box">
              <Leaf />
            </div>

            <h3>Efficiency & Emission Reduction</h3>

            <p>
              The objective for the new system is to reduce the amount of time
              spent looking for parking by at least 30%, subsequently reducing
              emissions released by this amount as well.
            </p>
          </article>

          <article class="goal-card">
            <div class="icon-box">
              <BarChart3 />
            </div>

            <h3>Data Driven Administration</h3>

            <p>
              Collect and analyze real-time and historical parking data to
              identify things like peak hours, most popular lots, as well as
              common parking usage patterns.
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

      <!-- SCOPE -->
      <section id="scope" class="content-section">
        <div class="section-heading">
          <span>03</span>

          <div>
            <p>Project Scope</p>
            <h2>What's included</h2>
          </div>
        </div>

        <p class="section-intro">
          The ParkSmart project encompasses the analysis, design, prototyping,
          integration planning, and evaluation of a centralized parking
          information solution for UVic.
        </p>

        <div class="scope-grid">
          <article class="scope-card">
            <button
              class="scope-header"
              @click="scopeOpen.inScope = !scopeOpen.inScope"
            >
              <div>
                <CheckCircle2 class="scope-positive" />
                <h3>In Scope</h3>
              </div>

              <ChevronDown
                :class="{ rotated: scopeOpen.inScope }"
              />
            </button>

            <Transition name="expand">
              <ul v-if="scopeOpen.inScope">
                <li>
                  Requirements gathering and analysis for the ParkSmart system.
                </li>

                <li>
                  Design and development of a mobile friendly ParkSmart
                  prototype.
                </li>

                <li>
                  User-facing dashboard for Parking Lots 1, E, and the Carsa
                  Parkade.
                </li>

                <li>
                  Administrative portal for monitoring parking availability and
                  usage patterns.
                </li>

                <li>
                  Mobile-responsive user and web-based administrative
                  interfaces.
                </li>
              </ul>
            </Transition>
          </article>

          <article class="scope-card">
            <button
              class="scope-header"
              @click="scopeOpen.outScope = !scopeOpen.outScope"
            >
              <div>
                <XCircle class="scope-negative" />
                <h3>Out of Scope</h3>
              </div>

              <ChevronDown
                :class="{ rotated: scopeOpen.outScope }"
              />
            </button>

            <Transition name="expand">
              <ul v-if="scopeOpen.outScope">
                <li>
                  Physical deployment of parking-detection hardware.
                </li>

                <li>
                  Full production deployment of ParkSmart across UVic.
                </li>

                <li>
                  Direct processing of parking payments or other financial
                  transactions.
                </li>

                <li>
                  Enforcing UVic parking regulations.
                </li>

                <li>
                  Construction or expansion of physical parking facilities.
                </li>
              </ul>
            </Transition>
          </article>
        </div>
      </section>

      <!-- MILESTONES -->
      <section id="milestones" class="content-section alt">
        <div class="section-heading">
          <span>04</span>

          <div>
            <p>Schedule</p>
            <h2>Project Milestones</h2>
          </div>
        </div>

        <div class="timeline">
          <div class="timeline-item completed">
            <div class="timeline-dot">
              <CheckCircle2 :size="17" />
            </div>

            <div class="timeline-content">
              <span>October 5, 2026</span>
              <strong>Project Charter</strong>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>

            <div class="timeline-content">
              <span>October 11, 2026</span>
              <strong>Requirements</strong>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>

            <div class="timeline-content">
              <span>October 25, 2026</span>
              <strong>Use Cases</strong>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>

            <div class="timeline-content">
              <span>November 1, 2026</span>
              <strong>Data Model</strong>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>

            <div class="timeline-content">
              <span>November 8, 2026</span>
              <strong>Process Model</strong>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>

            <div class="timeline-content">
              <span>November 15, 2026</span>
              <strong>UI Prototype</strong>
            </div>
          </div>

          <div class="timeline-item">
            <div class="timeline-dot"></div>

            <div class="timeline-content">
              <span>Nov 23 – Dec 3, 2026</span>
              <strong>Final Report & Presentation</strong>
            </div>
          </div>
        </div>
      </section>

      <!-- TEAM -->
      <section id="team" class="content-section">
        <div class="section-heading">
          <span>05</span>

          <div>
            <p>Project Organization</p>
            <h2>Meet the Team</h2>
          </div>
        </div>

        <div class="team-grid">
          <article>
            <div class="avatar">AT</div>
            <strong>Amanda Tu</strong>
            <span>Project Manager</span>
          </article>

          <article>
            <div class="avatar">JK</div>
            <strong>Jonah Kisakye</strong>
            <span>Frontend Developer</span>
          </article>

          <article>
            <div class="avatar">EP</div>
            <strong>Echo Parratt</strong>
            <span>Backend Developer</span>
          </article>

          <article>
            <div class="avatar">JH</div>
            <strong>Jana Hassan</strong>
            <span>UI/UX Designer</span>
          </article>

          <article>
            <div class="avatar">RD</div>
            <strong>Rob Dimmitt</strong>
            <span>Business Analyst</span>
          </article>
        </div>
      </section>
    </main>

    <footer>
      <div>
        <div class="footer-brand">
          <ParkingCircle />
          <strong>ParkSmart</strong>
        </div>

        <span>
          CSC 375 · University of Victoria · 2026
        </span>
      </div>
    </footer>
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

button,
a {
  font: inherit;
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
  width: min(1120px, 90%);

  margin: auto;

  min-height: 74px;

  display: flex;
  align-items: center;
  justify-content: space-between;
}

.brand {
  display: flex;
  gap: 12px;

  align-items: center;

  color: white;
}

.brand-icon {
  display: flex;

  align-items: center;
  justify-content: center;

  width: 42px;
  height: 42px;

  border-radius: 10px;

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
      circle at 85% 20%,
      rgba(0, 133, 56, 0.09),
      transparent 35%
    ),
    linear-gradient(180deg, #f8fafc, white);

  border-bottom: 1px solid var(--border);
}

.hero-grid {
  width: min(1120px, 90%);

  margin: auto;

  min-height: 580px;

  display: grid;
  grid-template-columns: 1.15fr 0.85fr;

  align-items: center;

  gap: 70px;

  padding: 70px 0;
}

.uvic-label {
  display: flex;
  align-items: center;

  gap: 8px;

  color: var(--green);

  font-size: 0.76rem;
  font-weight: 800;

  letter-spacing: 0.12em;
  text-transform: uppercase;
}

.uvic-label span {
  width: 28px;
  height: 3px;

  background: var(--yellow);
}

.hero h1 {
  margin: 16px 0 0;

  color: var(--navy);

  font-size: clamp(3.8rem, 7vw, 6.2rem);

  letter-spacing: -0.06em;

  line-height: 0.95;
}

.hero h2 {
  max-width: 680px;

  margin: 22px 0 0;

  color: #31465d;

  font-size: clamp(1.25rem, 2.2vw, 1.65rem);
  font-weight: 500;

  line-height: 1.4;
}

.hero-copy > p {
  max-width: 650px;

  margin: 22px 0 0;

  color: var(--muted);

  font-size: 1rem;

  line-height: 1.75;
}

.hero-actions {
  display: flex;

  gap: 12px;

  margin-top: 30px;
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
  border: 1px solid #ccd5dc;

  background: white;

  color: var(--navy);
}

.primary-button:hover,
.secondary-button:hover {
  transform: translateY(-2px);

  box-shadow: 0 8px 20px rgba(0, 39, 84, 0.1);
}

.project-meta {
  display: flex;

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

/* PARKING CARD */

.parking-panel {
  overflow: hidden;

  background: white;

  border: 1px solid #dce3e8;

  border-radius: 16px;

  box-shadow: 0 24px 70px rgba(0, 39, 84, 0.12);

  transition: transform 0.25s;
}

.parking-panel:hover {
  transform: translateY(-5px);
}

.panel-header {
  display: flex;

  justify-content: space-between;
  align-items: center;

  padding: 22px;

  border-bottom: 1px solid var(--border);
}

.panel-header > div:first-child {
  display: flex;
  flex-direction: column;

  gap: 4px;
}

.panel-header span {
  color: var(--muted);

  font-size: 0.75rem;
}

.panel-header strong {
  color: var(--navy);
}

.live-indicator {
  display: flex;

  align-items: center;

  gap: 6px;

  padding: 6px 9px;

  border-radius: 30px;

  background: #edf8f1;

  color: var(--green);

  font-size: 0.7rem;
  font-weight: 700;
}

.live-indicator span {
  width: 7px;
  height: 7px;

  border-radius: 50%;

  background: var(--green);
}

.parking-stats {
  display: grid;

  grid-template-columns: repeat(3, 1fr);

  border-bottom: 1px solid var(--border);
}

.parking-stat {
  display: flex;

  flex-direction: column;

  gap: 10px;

  padding: 20px;

  color: var(--blue);
}

.parking-stat:not(:last-child) {
  border-right: 1px solid var(--border);
}

.parking-stat > div {
  display: flex;
  flex-direction: column;
}

.parking-stat strong {
  color: var(--navy);

  font-size: 0.85rem;
}

.parking-stat span {
  margin-top: 3px;

  color: var(--muted);

  font-size: 0.68rem;
}

.lot-list {
  padding: 10px;
}

.lot {
  display: flex;

  justify-content: space-between;
  align-items: center;

  padding: 13px 12px;

  border-radius: 7px;

  transition: background 0.2s;
}

.lot:hover {
  background: var(--soft-bg);
}

.lot > div {
  display: flex;

  align-items: center;

  gap: 9px;

  color: #354553;

  font-size: 0.85rem;
}

.status {
  padding: 5px 8px;

  border-radius: 20px;

  font-size: 0.65rem;
  font-weight: 700;
}

.status.available {
  background: #edf8f1;

  color: var(--green);
}

/* MAIN */

.content-section {
  width: min(1120px, 90%);

  margin: auto;

  padding: 95px 0;

  scroll-margin-top: 70px;
}

.content-section.alt {
  width: 100%;

  padding-left: max(5%, calc((100% - 1120px) / 2));
  padding-right: max(5%, calc((100% - 1120px) / 2));

  background: var(--soft-bg);
}

.section-heading {
  display: flex;

  gap: 14px;

  align-items: flex-start;

  margin-bottom: 36px;
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

.overview-layout {
  display: grid;

  grid-template-columns: 1.3fr 0.7fr;

  gap: 65px;
}

.main-copy p,
.section-intro {
  color: #596975;

  line-height: 1.85;
}

.main-copy p:first-child {
  margin-top: 0;
}

.problem-cards {
  display: flex;

  flex-direction: column;

  gap: 12px;
}

.problem-cards article {
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

.problem-cards article:hover {
  transform: translateX(4px);

  box-shadow: 0 7px 20px rgba(0, 39, 84, 0.07);
}

.problem-cards svg {
  color: var(--blue);
}

.problem-cards div {
  display: flex;
  flex-direction: column;
}

.problem-cards strong {
  color: var(--navy);

  font-size: 0.88rem;
}

.problem-cards span {
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

  border: 1px solid #dce3e8;

  border-radius: 12px;

  background: white;

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

/* SCOPE */

.section-intro {
  max-width: 800px;

  margin-bottom: 30px;
}

.scope-grid {
  display: grid;

  grid-template-columns: repeat(2, 1fr);

  gap: 18px;
}

.scope-card {
  overflow: hidden;

  border: 1px solid var(--border);

  border-radius: 12px;

  background: white;
}

.scope-header {
  width: 100%;

  padding: 20px;

  display: flex;

  justify-content: space-between;
  align-items: center;

  border: 0;

  background: transparent;

  cursor: pointer;
}

.scope-header > div {
  display: flex;

  gap: 10px;

  align-items: center;
}

.scope-header h3 {
  margin: 0;

  color: var(--navy);
}

.scope-positive {
  color: var(--green);
}

.scope-negative {
  color: #a54b42;
}

.scope-header > svg {
  color: #79858e;

  transition: transform 0.25s;
}

.scope-header > svg.rotated {
  transform: rotate(180deg);
}

.scope-card ul {
  margin: 0;

  padding: 0 28px 22px 47px;
}

.scope-card li {
  margin-bottom: 12px;

  color: #63717c;

  line-height: 1.55;

  font-size: 0.85rem;
}

.expand-enter-active,
.expand-leave-active {
  transition: all 0.2s ease;
}

.expand-enter-from,
.expand-leave-to {
  opacity: 0;

  transform: translateY(-6px);
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

  display: flex;

  align-items: center;
  justify-content: center;

  flex-shrink: 0;

  width: 32px;
  height: 32px;

  border: 4px solid var(--soft-bg);

  border-radius: 50%;

  background: #cdd7de;
}

.timeline-item.completed .timeline-dot {
  background: var(--green);

  color: white;
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
  width: min(1120px, 100%);

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

/* MOBILE */

@media (max-width: 850px) {
  nav {
    display: none;
  }

  .hero-grid {
    grid-template-columns: 1fr;

    gap: 45px;
  }

  .hero-visual {
    max-width: 550px;
  }

  .overview-layout,
  .goal-grid,
  .scope-grid {
    grid-template-columns: 1fr;
  }

  .team-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 550px) {
  .hero h1 {
    font-size: 3.7rem;
  }

  .hero-actions {
    flex-direction: column;

    align-items: flex-start;
  }

  .parking-stats {
    grid-template-columns: 1fr;
  }

  .parking-stat {
    flex-direction: row;
  }

  .parking-stat:not(:last-child) {
    border-right: 0;

    border-bottom: 1px solid var(--border);
  }

  .team-grid {
    grid-template-columns: 1fr;
  }

  footer > div {
    flex-direction: column;

    gap: 10px;

    align-items: flex-start;
  }
}
</style>
