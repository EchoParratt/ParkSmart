<template>
  <div>
    <header class="site-header">
      <div class="header-inner">
        <div>
          <h1>ParkSmart</h1>
          <p>CSC 375 Project Charter</p>
        </div>

        <nav>
          <a href="#overview">Overview</a>
          <a href="#goals">Goals</a>
          <a href="#scope">Scope</a>
          <a href="#milestones">Milestones</a>
          <a href="#team">Team</a>
        </nav>
      </div>
    </header>

    <main>
      <!-- INTRO -->
      <section class="intro">
        <p class="label">University of Victoria</p>

        <h2>
          Automated Parking Capacity Monitoring and Historical Data Analytics
          Solution
        </h2>

        <p>
          ParkSmart is a proposed parking availability and data analytics
          solution for the University of Victoria (UVic).
        </p>

        <div class="meta">
          <span>CSC 375</span>
          <span>October 5, 2026</span>
          <span>Version 1.2</span>
        </div>
      </section>

      <!-- OVERVIEW -->
      <section id="overview">
        <h2>Project Overview</h2>

        <p>
          ParkSmart is a proposed parking availability and data analytics
          solution for the University of Victoria (UVic). The project addresses
          limitations in UVic’s current parking information system, which mainly
          provides static information and does not allow drivers to easily view
          current parking availability before or while travelling through
          campus. This can result in drivers spending additional time searching
          for parking, contributing to traffic congestion, delays, unnecessary
          vehicle idling, and frustration for campus users.
        </p>

        <p>
          The proposed solution will provide a centralized interface that
          displays current parking availability and historical parking trends,
          while also supporting administrative analysis of parking usage.
        </p>
      </section>

      <!-- GOALS -->
      <section id="goals">
        <h2>Project Goals</h2>

        <div class="cards">
          <article>
            <h3>System Design and Prototyping</h3>
            <p>
              Develop a working prototype to display our most important
              features. Things like real-time parking availability, available
              spaces, and historical parking trends through a simple interface.
            </p>
          </article>

          <article>
            <h3>Efficiency and Emission Reduction</h3>
            <p>
              The objective for the new system is to reduce the amount of time
              spent looking for parking by at least 30%, subsequently reducing
              emissions released by this amount as well.
            </p>
          </article>

          <article>
            <h3>Data Driven Administration</h3>
            <p>
              Collect and analyze real-time and historical parking data to
              identify things like peak hours, most popular lots, as well as
              common parking usage patterns.
            </p>
          </article>

          <article>
            <h3>Regulatory Compliance</h3>
            <p>
              Ensure that the system follows appropriate privacy and data
              management guidelines.
            </p>
          </article>
        </div>
      </section>

      <!-- SCOPE -->
      <section id="scope">
        <h2>Project Scope</h2>

        <p>
          The ParkSmart project encompasses the analysis, design, prototyping,
          integration planning, and evaluation of a centralized parking
          information solution for UVic.
        </p>

        <div class="scope-grid">
          <div>
            <h3>In Scope</h3>

            <ul>
              <li>
                Requirements gathering and analysis for the ParkSmart system.
              </li>
              <li>
                Design and development of a mobile friendly ParkSmart prototype.
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
                Mobile-responsive user and web-based administrative interfaces.
              </li>
            </ul>
          </div>

          <div>
            <h3>Out of Scope</h3>

            <ul>
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
          </div>
        </div>
      </section>

      <!-- MILESTONES -->
      <section id="milestones">
        <h2>Project Milestones</h2>

        <div class="milestones">
          <div>
            <strong>Project Charter</strong>
            <span>October 5, 2026</span>
          </div>

          <div>
            <strong>Requirements</strong>
            <span>October 11, 2026</span>
          </div>

          <div>
            <strong>Use Cases</strong>
            <span>October 25, 2026</span>
          </div>

          <div>
            <strong>Data Model</strong>
            <span>November 1, 2026</span>
          </div>

          <div>
            <strong>Process Model</strong>
            <span>November 8, 2026</span>
          </div>

          <div>
            <strong>UI Prototype</strong>
            <span>November 15, 2026</span>
          </div>

          <div>
            <strong>Final Report and Presentation</strong>
            <span>November 23 – December 3, 2026</span>
          </div>
        </div>
      </section>

      <!-- TEAM -->
      <section id="team">
        <h2>Project Team</h2>

        <div class="team">
          <div>
            <strong>Amanda Tu</strong>
            <span>Project Manager</span>
          </div>

          <div>
            <strong>Jonah Kisakye</strong>
            <span>Frontend Developer</span>
          </div>

          <div>
            <strong>Echo Parratt</strong>
            <span>Backend Developer</span>
          </div>

          <div>
            <strong>Jana Hassan</strong>
            <span>UI/UX Designer</span>
          </div>

          <div>
            <strong>Rob Dimmitt</strong>
            <span>Business Analyst</span>
          </div>
        </div>
      </section>
    </main>

    <footer>
      <p>
        ParkSmart · CSC 375 · University of Victoria
      </p>
    </footer>
  </div>
</template>

<style>
:root {
  font-family: Arial, Helvetica, sans-serif;

  --uvic-blue: #005493;
  --uvic-dark-blue: #002754;
  --uvic-green: #008538;
  --uvic-yellow: #f5aa1c;

  color: #222;
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

.site-header {
  background: var(--uvic-dark-blue);
  color: white;
}

.header-inner {
  width: min(1000px, 90%);
  margin: auto;

  display: flex;
  justify-content: space-between;
  align-items: center;

  padding: 22px 0;
}

.site-header h1 {
  margin: 0;
  font-size: 1.6rem;
}

.site-header p {
  margin: 4px 0 0;
  color: #d7e4ef;
  font-size: 0.9rem;
}

nav {
  display: flex;
  gap: 22px;
}

nav a {
  color: white;
  text-decoration: none;
  font-size: 0.9rem;
}

nav a:hover {
  text-decoration: underline;
}

main {
  width: min(900px, 90%);
  margin: auto;
}

section {
  padding: 60px 0;
  border-bottom: 1px solid #e3e3e3;
  scroll-margin-top: 80px;
}

.intro {
  padding-top: 80px;
}

.label {
  color: var(--uvic-green);
  font-weight: bold;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  font-size: 0.8rem;
}

.intro h2 {
  max-width: 760px;
  margin: 10px 0 20px;

  color: var(--uvic-dark-blue);

  font-size: clamp(2.2rem, 5vw, 3.7rem);
  line-height: 1.1;
}

.intro > p:not(.label) {
  max-width: 680px;

  font-size: 1.1rem;
  line-height: 1.7;

  color: #555;
}

.meta {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;

  margin-top: 28px;
}

.meta span {
  padding: 7px 11px;

  border-left: 4px solid var(--uvic-yellow);

  background: #f4f6f8;

  font-size: 0.85rem;
}

section > h2 {
  margin-top: 0;

  color: var(--uvic-dark-blue);

  font-size: 2rem;
}

section > p {
  line-height: 1.8;
  color: #555;
}

.cards {
  display: grid;
  grid-template-columns: repeat(2, 1fr);

  gap: 16px;
}

.cards article {
  padding: 22px;

  border: 1px solid #ddd;
  border-top: 4px solid var(--uvic-blue);
}

.cards h3 {
  margin-top: 0;

  color: var(--uvic-dark-blue);
}

.cards p {
  margin-bottom: 0;

  color: #555;
  line-height: 1.65;
}

.scope-grid {
  display: grid;

  grid-template-columns: 1fr 1fr;

  gap: 40px;

  margin-top: 30px;
}

.scope-grid h3 {
  color: var(--uvic-blue);
}

ul {
  padding-left: 20px;
}

li {
  margin-bottom: 12px;

  line-height: 1.5;
  color: #555;
}

.milestones {
  border-top: 1px solid #ddd;
}

.milestones div {
  display: flex;
  justify-content: space-between;
  gap: 20px;

  padding: 16px 4px;

  border-bottom: 1px solid #ddd;
}

.milestones strong {
  color: var(--uvic-dark-blue);
}

.milestones span {
  color: #666;
}

.team {
  display: grid;

  grid-template-columns: repeat(2, 1fr);

  gap: 12px;
}

.team div {
  display: flex;
  flex-direction: column;

  padding: 16px;

  background: #f4f6f8;

  border-left: 4px solid var(--uvic-green);
}

.team strong {
  color: var(--uvic-dark-blue);
}

.team span {
  margin-top: 4px;

  color: #666;

  font-size: 0.9rem;
}

footer {
  margin-top: 60px;

  padding: 30px;

  text-align: center;

  background: var(--uvic-dark-blue);
  color: white;
}

footer p {
  margin: 0;

  font-size: 0.85rem;
}

@media (max-width: 700px) {
  .header-inner {
    align-items: flex-start;
  }

  nav {
    display: none;
  }

  .cards,
  .scope-grid,
  .team {
    grid-template-columns: 1fr;
  }

  .milestones div {
    flex-direction: column;
    gap: 4px;
  }

  section {
    padding: 45px 0;
  }
}
</style>
