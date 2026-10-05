<template>
  <div class="page">
    <!-- NAVIGATION -->
    <header class="navbar">
      <a href="#" class="brand">
        <span class="brand-icon">P</span>
        <span>ParkSmart</span>
      </a>

      <nav>
        <a href="#overview">Overview</a>
        <a href="#goals">Goals</a>
        <a href="#scope">Scope</a>
        <a href="#stakeholders">Stakeholders</a>
        <a href="#milestones">Milestones</a>
        <a href="#risks">Risks</a>
        <a href="#team">Team</a>
      </nav>
    </header>

    <!-- HERO -->
    <section class="hero">
      <div class="hero-inner">
        <div class="hero-content">
          <p class="eyebrow">CSC 375 · Project Charter</p>

          <h1>ParkSmart</h1>

          <h2>
            Automated Parking Capacity Monitoring and Historical Data Analytics
            Solution
          </h2>

          <p class="hero-description">
            ParkSmart is a proposed parking availability and data analytics
            solution for the University of Victoria (UVic).
          </p>

          <div class="hero-actions">
            <a href="#overview" class="primary-btn">
              Explore Project
            </a>

            <a href="#milestones" class="secondary-btn">
              View Milestones
            </a>
          </div>

          <div class="hero-meta">
            <div>
              <span>Course</span>
              <strong>CSC 375</strong>
            </div>

            <div>
              <span>University</span>
              <strong>University of Victoria</strong>
            </div>

            <div>
              <span>Version</span>
              <strong>1.2</strong>
            </div>

            <div>
              <span>Date</span>
              <strong>October 5, 2026</strong>
            </div>
          </div>
        </div>
      </div>
    </section>

    <main class="content">
      <!-- PROJECT OVERVIEW -->
      <section id="overview" class="section">
        <div class="section-heading">
          <p class="section-number">01</p>

          <div>
            <p class="section-kicker">Project Overview</p>
            <h2>Project Summary</h2>
          </div>
        </div>

        <div class="large-card">
          <p>
            ParkSmart is a proposed parking availability and data analytics
            solution for the University of Victoria (UVic). The project
            addresses limitations in UVic’s current parking information system,
            which mainly provides static information and does not allow drivers
            to easily view current parking availability before or while
            travelling through campus. This can result in drivers spending
            additional time searching for parking, contributing to traffic
            congestion, delays, unnecessary vehicle idling, and frustration for
            campus users.
          </p>

          <p>
            The proposed solution will provide a centralized interface that
            displays current parking availability and historical parking trends,
            while also supporting administrative analysis of parking usage. The
            key stakeholders who are expected to benefit from ParkSmart include
            UVic students, faculty, staff, and campus visitors who require
            parking, as well as UVic Campus Security and Parking Services and
            University Systems staff who may use the system to monitor parking
            activity, support operational decisions, and assist with future
            parking planning.
          </p>
        </div>
      </section>

      <!-- NEED -->
      <section class="section">
        <div class="section-heading">
          <p class="section-number">02</p>

          <div>
            <p class="section-kicker">Why ParkSmart?</p>
            <h2>Need</h2>
          </div>
        </div>

        <div class="large-card emphasis-card">
          <p>
            The current UVic parking website provides only static, high-level
            information, making it ineffective for helping drivers easily find
            available parking or navigate to the correct lot. The system's lack
            of real-time navigation results in drivers on Ring Road slowing down
            to manually search for lots, creating congestion and increasing
            delays for everyone.
          </p>

          <p>
            Our proposed solution addresses these issues by offering real-time
            parking availability and automated visual and audio navigation. This
            will reduce time spent searching for parking and reduce congestion
            on the roads and, consequently, carbon emissions from idling cars.
            Additionally, the system will collect data on congestion patterns
            and usage trends, giving the university insights for future planning
            and expansion.
          </p>
        </div>
      </section>

      <!-- GOALS -->
      <section id="goals" class="section">
        <div class="section-heading">
          <p class="section-number">03</p>

          <div>
            <p class="section-kicker">Project Goals</p>
            <h2>Goals, Objectives & Outcomes</h2>
          </div>
        </div>

        <div class="goal-grid">
          <article class="goal-card">
            <span class="goal-index">01</span>
            <h3>System Design and Prototyping</h3>

            <div class="goal-content">
              <h4>Objective</h4>
              <p>
                Develop a working prototype to display our most important
                features. Things like real-time parking availability, available
                spaces, and historical parking trends through a simple
                interface.
              </p>

              <h4>Business Outcome</h4>
              <p>
                This will allow UVic to assess ParkSmart as a prototype first to
                gauge feasibility and effectiveness before committing to a
                full-scale implementation of it.
              </p>
            </div>
          </article>

          <article class="goal-card">
            <span class="goal-index">02</span>
            <h3>Efficiency and Emission Reduction</h3>

            <div class="goal-content">
              <h4>Objective</h4>
              <p>
                The objective for the new system is to reduce the amount of time
                spent looking for parking by at least 30%, subsequently reducing
                emissions released by this amount as well. This can be tracked
                using historical data.
              </p>

              <h4>Business Outcome</h4>
              <p>
                This would heavily contribute to / fall in line with UVic's
                “Climate & Sustainability Action Plan 2030”. It pledges
                commitments to the environment and includes several goals which
                involve reducing emissions.
              </p>
            </div>
          </article>

          <article class="goal-card">
            <span class="goal-index">03</span>
            <h3>User Experience</h3>

            <div class="goal-content">
              <h4>Objective</h4>
              <p>
                Users will be able to provide feedback through the software.
                They can report on satisfaction as well as the success of the
                application to help them find a suitable lot with available
                spots.
              </p>

              <h4>Business Outcome</h4>
              <p>
                More parking not only benefits those driving but also will
                increase use of UVic parking services as well as usage of the
                HONK mobile app. As a result, this should drive profit upwards
                for all parties involved with overseeing UVic parking.
              </p>
            </div>
          </article>

          <article class="goal-card">
            <span class="goal-index">04</span>
            <h3>Data Driven Administration</h3>

            <div class="goal-content">
              <h4>Objective</h4>
              <p>
                Collect and analyze real-time and historical parking data to
                identify things like peak hours, most popular lots, as well as
                common parking usage patterns.
              </p>

              <h4>Business Outcome</h4>
              <p>
                This will allow UVic to make better-informed decisions about
                parking capacity and lot management, as well as pricing and
                future infrastructure investments.
              </p>
            </div>
          </article>

          <article class="goal-card">
            <span class="goal-index">05</span>
            <h3>Regulatory Compliance</h3>

            <div class="goal-content">
              <h4>Objective</h4>
              <p>
                Ensure that the system follows appropriate privacy and data
                management guidelines.
              </p>

              <h4>Business Outcome</h4>
              <p>
                This will reduce legal and privacy risks while ensuring the
                system can be safely implemented by UVic.
              </p>
            </div>
          </article>
        </div>
      </section>

      <!-- SCOPE -->
      <section id="scope" class="section">
        <div class="section-heading">
          <p class="section-number">04</p>

          <div>
            <p class="section-kicker">Project Scope</p>
            <h2>Scope Definition</h2>
          </div>
        </div>

        <div class="large-card">
          <p>
            The ParkSmart project encompasses the analysis, design, prototyping,
            integration planning, and evaluation of a centralized parking
            information solution for UVic. The prototype will provide users with
            current parking availability information, parking lot navigation,
            historical parking trends, and an administrative interface for
            monitoring parking utilization. The project will also define system
            requirements, develop supporting models and interface designs, and
            evaluate the feasibility of the proposed solution. The project does
            not include full production deployment of parking-detection hardware
            or operation of UVic's parking enforcement and payment systems.
          </p>
        </div>

        <div class="scope-grid">
          <article class="scope-card in-scope">
            <div class="scope-title">
              <span>✓</span>
              <h3>Activities In Scope</h3>
            </div>

            <ul>
              <li>
                Requirements gathering and analysis for the ParkSmart system by
                researching and surveying stakeholders.
              </li>

              <li>
                Design and development of a mobile friendly ParkSmart prototype
                for commuters.
              </li>

              <li>
                Development of a user-facing dashboard displaying current
                parking availability for the selected lots in scope, Parking
                Lots 1, E, and the Carsa Parkade.
              </li>

              <li>
                Development of an administrative portal for monitoring parking
                availability and usage patterns, where access is restricted to
                authorized users.
              </li>

              <li>
                Simple and intuitive interface design, including
                mobile-responsive user and web-based administrative interfaces.
              </li>
            </ul>
          </article>

          <article class="scope-card out-scope">
            <div class="scope-title">
              <span>×</span>
              <h3>Activities Out of Scope</h3>
            </div>

            <ul>
              <li>
                Physical deployment of parking-detection hardware, such as
                cameras or ground sensors.
              </li>

              <li>
                Full production deployment of ParkSmart across UVic, only
                including Parking Lots 1, E, and the Carsa Parkade.
              </li>

              <li>
                Direct processing of parking payments or other financial
                transactions, such as hourly rates on physical meters or monthly
                virtual permits.
              </li>

              <li>
                Enforcing UVic parking regulations, including conducting
                patrols, issuing citations for violations, and arranging the
                towing of non-compliant vehicles.
              </li>

              <li>
                Construction or expansion of physical parking facilities, such
                as paving roads and installing physical signage.
              </li>
            </ul>
          </article>
        </div>
      </section>

      <!-- STAKEHOLDERS -->
      <section id="stakeholders" class="section">
        <div class="section-heading">
          <p class="section-number">05</p>

          <div>
            <p class="section-kicker">Stakeholders</p>
            <h2>Who ParkSmart Serves</h2>
          </div>
        </div>

        <div class="stakeholder-grid">
          <article class="stakeholder-card">
            <div class="stakeholder-tag">Primary End User</div>

            <h3>UVic Commuters</h3>

            <p class="stakeholder-subtitle">
              Students, staff, and faculty
            </p>

            <p>
              Primary ParkSmart users who will use the system to view parking
              availability, identify suitable parking areas, and review parking
              condition information. Their feedback can help assess the
              system's usability and effectiveness.
            </p>
          </article>

          <article class="stakeholder-card">
            <div class="stakeholder-tag">End User</div>

            <h3>Campus Visitors</h3>

            <p class="stakeholder-subtitle">
              Guests, families, and other visitors to UVic
            </p>

            <p>
              Occasional users who may benefit from ParkSmart when navigating
              unfamiliar parking areas on campus. The system can provide clearer
              parking information and help visitors identify available parking
              more efficiently.
            </p>
          </article>

          <article class="stakeholder-card">
            <div class="stakeholder-tag">
              Business Stakeholder / Administrative User
            </div>

            <h3>UVic Campus Security and Parking Services</h3>

            <p class="stakeholder-subtitle">
              Parking services staff and administrators
            </p>

            <p>
              Responsible for parking-related operations and administration at
              UVic. These stakeholders may use ParkSmart data to monitor parking
              availability and usage patterns and to support parking management
              and planning decisions.
            </p>
          </article>

          <article class="stakeholder-card">
            <div class="stakeholder-tag">
              Technical Support / System Administration
            </div>

            <h3>University Systems (IT)</h3>

            <p class="stakeholder-subtitle">
              IT Staff and administration
            </p>

            <p>
              Supports the technical infrastructure required for ParkSmart.
              Responsibilities may include system integration, security,
              reliability, maintenance, and technical support for the parking
              information system.
            </p>
          </article>
        </div>
      </section>

      <!-- MILESTONES -->
      <section id="milestones" class="section">
        <div class="section-heading">
          <p class="section-number">06</p>

          <div>
            <p class="section-kicker">Schedule</p>
            <h2>Project Milestones</h2>
          </div>
        </div>

        <div class="timeline">
          <article class="timeline-item">
            <div class="timeline-marker"></div>

            <div class="timeline-date">
              October 5, 2026
            </div>

            <div class="timeline-content">
              <h3>Project Charter</h3>

              <p>
                Defines the project scope, objectives, stakeholders, roles,
                schedule, deliverables, and risks.
              </p>
            </div>
          </article>

          <article class="timeline-item">
            <div class="timeline-marker"></div>

            <div class="timeline-date">
              October 11, 2026
            </div>

            <div class="timeline-content">
              <h3>Requirements</h3>

              <p>
                Documents the system requirements for the proposed ParkSmart
                solution.
              </p>
            </div>
          </article>

          <article class="timeline-item">
            <div class="timeline-marker"></div>

            <div class="timeline-date">
              October 25, 2026
            </div>

            <div class="timeline-content">
              <h3>Use Cases</h3>

              <p>
                Documents the major interactions between users and the proposed
                system.
              </p>
            </div>
          </article>

          <article class="timeline-item">
            <div class="timeline-marker"></div>

            <div class="timeline-date">
              November 1, 2026
            </div>

            <div class="timeline-content">
              <h3>Data Model</h3>

              <p>
                Defines the main data entities and relationships required by the
                system.
              </p>
            </div>
          </article>

          <article class="timeline-item">
            <div class="timeline-marker"></div>

            <div class="timeline-date">
              November 8, 2026
            </div>

            <div class="timeline-content">
              <h3>Process Model</h3>

              <p>
                Represents the major system processes and information flows.
              </p>
            </div>
          </article>

          <article class="timeline-item">
            <div class="timeline-marker"></div>

            <div class="timeline-date">
              November 15, 2026
            </div>

            <div class="timeline-content">
              <h3>UI Prototype</h3>

              <p>
                Demonstrates the proposed user interface and key workflows.
              </p>
            </div>
          </article>

          <article class="timeline-item">
            <div class="timeline-marker"></div>

            <div class="timeline-date">
              Nov 23rd, 26th, 30th, and Dec 3rd
            </div>

            <div class="timeline-content">
              <h3>Final Report and Presentation</h3>

              <p>
                Presents the final project and proposed solution.
              </p>
            </div>
          </article>
        </div>
      </section>

      <!-- RISKS -->
      <section id="risks" class="section">
        <div class="section-heading">
          <p class="section-number">07</p>

          <div>
            <p class="section-kicker">
              Risk Management
            </p>

            <h2>Project Risks</h2>
          </div>
        </div>

        <div class="risk-grid">
          <article class="risk-card">
            <div class="risk-header">
              <h3>Data Accuracy</h3>

              <div class="risk-levels">
                <span>Probability: M</span>
                <span class="high">Impact: H</span>
              </div>
            </div>

            <p>
              The system reports incorrect or skewed data from technical errors,
              duplicate entries, or physical cases where drivers park outside
              designated zones, leading to imprecise metrics.
            </p>

            <div class="mitigation">
              <strong>Risk Management Plan</strong>

              <p>
                Deploy machine learning models to predict spot availability
                based on historical usage and automatically flag irregular data
                points. Calibrate these models regularly using physical lot
                sweeps and user-reported discrepancies.
              </p>
            </div>
          </article>

          <article class="risk-card">
            <div class="risk-header">
              <h3>Privacy and Regulatory Compliance</h3>

              <div class="risk-levels">
                <span>Probability: L</span>
                <span class="high">Impact: H</span>
              </div>
            </div>

            <p>
              Failure to adhere to local data protection laws resulting in
              unauthorized exposure of sensitive information that may cause
              financial penalties and reputational damage.
            </p>

            <div class="mitigation">
              <strong>Risk Management Plan</strong>

              <p>
                Ensure FIPPA compliance, where data is stripped of all personal
                identifiers, before data transmission or storage. Enforce
                role-based access control, multi-factor authentication, and
                end-to-end encryption.
              </p>
            </div>
          </article>

          <article class="risk-card">
            <div class="risk-header">
              <h3>Integration with Current System</h3>

              <div class="risk-levels">
                <span>Probability: M</span>
                <span class="high">Impact: H</span>
              </div>
            </div>

            <p>
              ParkSmart encounters compatibility issues with legacy
              infrastructure or third-party APIs, which may cause data
              synchronization errors and deployment delays.
            </p>

            <div class="mitigation">
              <strong>Risk Management Plan</strong>

              <p>
                Thoroughly test all API connections in isolation in a staging
                environment before deployment. Establish a clear strategy to
                immediately revert to the previous, stable version if critical
                failure occurs.
              </p>
            </div>
          </article>

          <article class="risk-card">
            <div class="risk-header">
              <h3>System Downtime or Latency</h3>

              <div class="risk-levels">
                <span>Probability: M</span>
                <span class="high">Impact: H</span>
              </div>
            </div>

            <p>
              Blocked workflows and end-user frustration from unexpected server
              outages or slow application response time during peak usage.
            </p>

            <div class="mitigation">
              <strong>Risk Management Plan</strong>

              <p>
                Run early beta tests with a limited user group to evaluate the
                application’s performance under lower load. Implement
                around-the-clock monitoring, load balancing, and clear disaster
                planning.
              </p>
            </div>
          </article>

          <article class="risk-card">
            <div class="risk-header">
              <h3>Low User Adoption</h3>

              <div class="risk-levels">
                <span>Probability: M</span>
                <span class="high">Impact: H</span>
              </div>
            </div>

            <p>
              The campus community hesitates to adopt the ParkSmart dashboard
              because of a poor user experience, unclear benefits, or entrenched
              parking habits.
            </p>

            <div class="mitigation">
              <strong>Risk Management Plan</strong>

              <p>
                Refine the interface through early pilot testing, highlight
                time-saving benefits in a campuswide launch campaign, and offer
                early-adopter incentives to help users break their established
                parking routines.
              </p>
            </div>
          </article>
        </div>
      </section>

      <!-- ASSUMPTIONS / CONSTRAINTS -->
      <section class="section">
        <div class="section-heading">
          <p class="section-number">08</p>

          <div>
            <p class="section-kicker">Planning</p>
            <h2>Assumptions & Constraints</h2>
          </div>
        </div>

        <div class="scope-grid">
          <article class="info-card">
            <h3>Assumptions</h3>

            <ul>
              <li>
                <strong>User Accessibility:</strong>
                The target campus demographic (students, faculty, and staff)
                possesses the necessary mobile devices and digital literacy to
                access and navigate the ParkSmart dashboard.
              </li>

              <li>
                <strong>Network Stability:</strong>
                The campus maintains sufficient Wi-Fi and cellular network
                coverage and uptime across all parking zones to support
                real-time data synchronization.
              </li>

              <li>
                <strong>Stakeholder Support:</strong>
                University administration, IT departments, and campus security
                are fully aligned with the project goals and will allocate the
                necessary resources for testing and rollout.
              </li>

              <li>
                <strong>Data Availability and Machine Learning:</strong>
                Suppose relevant data pipelines are established from the HONK
                mobile application and UVic Systems. Moreover, sufficient
                historical parking baseline is available to accurately train
                and calibrate the machine learning predictive models before the
                official launch.
              </li>
            </ul>
          </article>

          <article class="info-card">
            <h3>Constraints</h3>

            <ul>
              <li>
                <strong>Regulatory & Privacy Boundaries:</strong>
                All data collection, processing, and storage must strictly
                adhere to FIPPA regulations, requiring absolute anonymization
                of user data.
              </li>

              <li>
                <strong>Software-Only Architecture:</strong>
                The project is strictly prohibited from purchasing, installing,
                or maintaining any physical hardware (e.g., ground sensors,
                cameras). All occupancy data must be derived entirely through
                software, user mobile devices, and predictive algorithms
                through presumed data pipelines from UVic Systems and the HONK
                mobile application.
              </li>

              <li>
                <strong>Technical Integration Limits:</strong>
                The system architecture is constrained by the capabilities, API
                rate limits, and potential technical debt of the university’s
                existing legacy parking infrastructure.
              </li>

              <li>
                <strong>Schedule and Academic Calendar:</strong>
                The academic calendar heavily restricts deployment and testing
                phases.
              </li>
            </ul>
          </article>
        </div>
      </section>

      <!-- TEAM -->
      <section id="team" class="section">
        <div class="section-heading">
          <p class="section-number">09</p>

          <div>
            <p class="section-kicker">Project Organization</p>
            <h2>Meet the Team</h2>
          </div>
        </div>

        <div class="team-grid">
          <article class="team-member">
            <div class="avatar">AT</div>
            <h3>Amanda Tu</h3>
            <p>Project Manager</p>
          </article>

          <article class="team-member">
            <div class="avatar">JK</div>
            <h3>Jonah Kisakye</h3>
            <p>Frontend Developer</p>
          </article>

          <article class="team-member">
            <div class="avatar">EP</div>
            <h3>Echo Parratt</h3>
            <p>Backend Developer</p>
          </article>

          <article class="team-member">
            <div class="avatar">JH</div>
            <h3>Jana Hassan</h3>
            <p>UI/UX Designer</p>
          </article>

          <article class="team-member">
            <div class="avatar">RD</div>
            <h3>Rob Dimmitt</h3>
            <p>Business Analyst</p>
          </article>
        </div>
      </section>

      <!-- GOVERNANCE -->
      <section class="section">
        <div class="section-heading">
          <p class="section-number">10</p>

          <div>
            <p class="section-kicker">Organization</p>
            <h2>Project Governance</h2>
          </div>
        </div>

        <div class="large-card">
          <p>
            ParkSmart will use a collaborative project governance structure.
            This will be led by the Project Manager. The Project Manager will
            have the responsibility of coordinating project activities,
            tracking deadlines, assigning work and helping other team members
            resolve blockers. Major design choices and decisions involving
            changes to project scope, schedule or deliverables will be discussed
            and reviewed with the entire team.
          </p>

          <p>
            Each team member will be responsible for completing work within
            their assigned role while keeping the Project Manager up to date
            with progress, issues, dependencies and deliverables. Decisions that
            affect multiple areas, such as API integration, authentication, data
            structure, or interface design, will be coordinated between the
            relevant team members. This governance structure is intended to
            maintain accountability while still allowing the team to make
            decisions collaboratively.
          </p>
        </div>
      </section>
    </main>

    <!-- FOOTER -->
    <footer>
      <div class="footer-content">
        <div>
          <strong>ParkSmart</strong>
          <p>
            Automated Parking Capacity Monitoring and Historical Data Analytics
            Solution
          </p>
        </div>

        <div class="footer-right">
          <p>CSC 375 — Introduction to System Analysis</p>
          <p>University of Victoria</p>
          <p>October 5, 2026</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<style>
:root {
  font-family:
    Inter,
    ui-sans-serif,
    system-ui,
    -apple-system,
    BlinkMacSystemFont,
    "Segoe UI",
    sans-serif;

  color: #17211d;
  background: #f5f7f6;

  font-synthesis: none;
  text-rendering: optimizeLegibility;
}

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  min-width: 320px;
  background: #f5f7f6;
}

a {
  color: inherit;
  text-decoration: none;
}

.page {
  min-height: 100vh;
}

/* NAVBAR */

.navbar {
  position: sticky;
  top: 0;
  z-index: 100;

  display: flex;
  justify-content: space-between;
  align-items: center;

  padding: 16px 6%;

  background: rgba(255, 255, 255, 0.94);
  backdrop-filter: blur(14px);

  border-bottom: 1px solid #dde4e1;
}

.brand {
  display: flex;
  align-items: center;
  gap: 10px;

  color: #134e42;

  font-size: 1.15rem;
  font-weight: 800;
}

.brand-icon {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 32px;
  height: 32px;

  border-radius: 8px;

  background: #176b5b;
  color: white;
}

nav {
  display: flex;
  align-items: center;
  gap: 25px;
}

nav a {
  color: #53635d;

  font-size: 0.88rem;
  font-weight: 600;

  transition: 0.2s ease;
}

nav a:hover {
  color: #176b5b;
}

/* HERO */

.hero {
  position: relative;

  overflow: hidden;

  background:
    radial-gradient(
      circle at 80% 20%,
      rgba(87, 183, 147, 0.18),
      transparent 35%
    ),
    linear-gradient(135deg, #102f29 0%, #155d50 55%, #176b5b 100%);

  color: white;
}

.hero::after {
  content: "";

  position: absolute;

  right: -100px;
  bottom: -220px;

  width: 620px;
  height: 620px;

  border-radius: 50%;

  border: 100px solid rgba(255, 255, 255, 0.025);
}

.hero-inner {
  position: relative;
  z-index: 1;

  display: flex;
  align-items: center;

  min-height: 78vh;

  width: min(1180px, 88%);
  margin: auto;

  padding: 90px 0;
}

.hero-content {
  max-width: 850px;
}

.eyebrow {
  margin: 0 0 18px;

  color: #94d8c1;

  font-size: 0.82rem;
  font-weight: 800;

  letter-spacing: 0.18em;
  text-transform: uppercase;
}

.hero h1 {
  margin: 0;

  font-size: clamp(4.8rem, 11vw, 9rem);
  line-height: 0.9;

  letter-spacing: -0.055em;
}

.hero h2 {
  max-width: 800px;

  margin: 24px 0 0;

  color: #cde3db;

  font-size: clamp(1.2rem, 2.5vw, 1.75rem);
  font-weight: 500;

  line-height: 1.4;
}

.hero-description {
  max-width: 700px;

  margin-top: 25px;

  color: rgba(255, 255, 255, 0.76);

  font-size: 1.08rem;
  line-height: 1.8;
}

.hero-actions {
  display: flex;
  gap: 12px;

  margin-top: 34px;
}

.primary-btn,
.secondary-btn {
  padding: 13px 21px;

  border-radius: 9px;

  font-weight: 700;

  transition:
    transform 0.2s ease,
    background 0.2s ease;
}

.primary-btn {
  background: white;
  color: #155d50;
}

.secondary-btn {
  border: 1px solid rgba(255, 255, 255, 0.32);

  color: white;
}

.primary-btn:hover,
.secondary-btn:hover {
  transform: translateY(-2px);
}

.hero-meta {
  display: flex;
  flex-wrap: wrap;
  gap: 45px;

  margin-top: 60px;
  padding-top: 28px;

  border-top: 1px solid rgba(255, 255, 255, 0.16);
}

.hero-meta div {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.hero-meta span {
  color: rgba(255, 255, 255, 0.5);

  font-size: 0.72rem;

  text-transform: uppercase;
  letter-spacing: 0.12em;
}

.hero-meta strong {
  font-size: 0.92rem;
}

/* GENERAL CONTENT */

.content {
  width: min(1180px, 88%);
  margin: auto;
}

.section {
  padding: 100px 0 5px;

  scroll-margin-top: 75px;
}

.section-heading {
  display: flex;
  align-items: flex-start;
  gap: 18px;

  margin-bottom: 35px;
}

.section-number {
  margin: 10px 0 0;

  color: #1b806d;

  font-size: 0.82rem;
  font-weight: 800;
}

.section-kicker {
  margin: 0 0 5px;

  color: #1b806d;

  font-size: 0.79rem;
  font-weight: 800;

  letter-spacing: 0.13em;
  text-transform: uppercase;
}

.section-heading h2 {
  margin: 0;

  color: #17231f;

  font-size: clamp(2rem, 4vw, 3.3rem);

  letter-spacing: -0.04em;
}

.large-card,
.info-card {
  padding: 35px;

  background: white;

  border: 1px solid #dfe6e3;
  border-radius: 16px;

  box-shadow: 0 10px 35px rgba(31, 57, 48, 0.045);
}

.large-card p {
  margin-top: 0;

  color: #5c6b65;

  font-size: 1.03rem;
  line-height: 1.85;
}

.large-card p:last-child {
  margin-bottom: 0;
}

.emphasis-card {
  border-left: 5px solid #1b806d;
}

/* GOALS */

.goal-grid {
  display: grid;

  grid-template-columns: repeat(2, 1fr);

  gap: 20px;
}

.goal-card {
  position: relative;

  padding: 30px;

  overflow: hidden;

  background: white;

  border: 1px solid #dfe6e3;
  border-radius: 16px;

  box-shadow: 0 8px 25px rgba(31, 57, 48, 0.04);
}

.goal-card:last-child {
  grid-column: 1 / -1;
}

.goal-index {
  color: #1b806d;

  font-size: 0.78rem;
  font-weight: 800;
}

.goal-card h3 {
  margin: 8px 0 22px;

  color: #21342d;

  font-size: 1.35rem;
}

.goal-content h4 {
  margin: 20px 0 5px;

  color: #176b5b;

  font-size: 0.75rem;

  letter-spacing: 0.12em;
  text-transform: uppercase;
}

.goal-content p {
  margin: 0;

  color: #68756f;

  line-height: 1.7;
}

/* SCOPE */

.scope-grid {
  display: grid;

  grid-template-columns: repeat(2, 1fr);

  gap: 20px;

  margin-top: 20px;
}

.scope-card {
  padding: 30px;

  background: white;

  border: 1px solid #dfe6e3;
  border-radius: 16px;
}

.scope-title {
  display: flex;
  align-items: center;
  gap: 12px;
}

.scope-title span {
  display: flex;
  justify-content: center;
  align-items: center;

  width: 32px;
  height: 32px;

  border-radius: 50%;

  font-size: 1.25rem;
  font-weight: 800;
}

.in-scope .scope-title span {
  background: #e5f5ef;
  color: #176b5b;
}

.out-scope .scope-title span {
  background: #f7ecea;
  color: #9d483e;
}

.scope-card h3 {
  margin: 0;

  font-size: 1.2rem;
}

.scope-card ul,
.info-card ul {
  padding-left: 20px;
  margin-bottom: 0;
}

.scope-card li,
.info-card li {
  margin-bottom: 15px;

  color: #63716c;

  line-height: 1.65;
}

/* STAKEHOLDERS */

.stakeholder-grid {
  display: grid;

  grid-template-columns: repeat(2, 1fr);

  gap: 20px;
}

.stakeholder-card {
  padding: 30px;

  background: white;

  border: 1px solid #dfe6e3;
  border-radius: 16px;

  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease;
}

.stakeholder-card:hover {
  transform: translateY(-3px);

  box-shadow: 0 12px 30px rgba(31, 57, 48, 0.07);
}

.stakeholder-tag {
  display: inline-block;

  margin-bottom: 18px;

  padding: 6px 10px;

  border-radius: 6px;

  background: #e8f5f1;

  color: #176b5b;

  font-size: 0.7rem;
  font-weight: 800;

  text-transform: uppercase;
  letter-spacing: 0.06em;
}

.stakeholder-card h3 {
  margin: 0;

  color: #22342e;

  font-size: 1.3rem;
}

.stakeholder-subtitle {
  margin: 7px 0 20px !important;

  color: #176b5b !important;

  font-weight: 600;
}

.stakeholder-card p {
  margin: 0;

  color: #68766f;

  line-height: 1.7;
}

/* TIMELINE */

.timeline {
  position: relative;

  margin-left: 8px;
}

.timeline::before {
  content: "";

  position: absolute;

  top: 10px;
  bottom: 10px;
  left: 7px;

  width: 2px;

  background: #cee2db;
}

.timeline-item {
  position: relative;

  display: grid;

  grid-template-columns: 20px 200px 1fr;

  gap: 25px;

  padding: 0 0 37px;
}

.timeline-marker {
  position: relative;
  z-index: 2;

  width: 16px;
  height: 16px;

  margin-top: 4px;

  border-radius: 50%;

  background: #176b5b;

  border: 4px solid #e5f4ef;
}

.timeline-date {
  color: #176b5b;

  font-size: 0.85rem;
  font-weight: 800;
}

.timeline-content h3 {
  margin: 0 0 6px;

  color: #263a33;
}

.timeline-content p {
  margin: 0;

  color: #68766f;

  line-height: 1.6;
}

/* RISKS */

.risk-grid {
  display: grid;
  gap: 20px;
}

.risk-card {
  padding: 30px;

  background: white;

  border: 1px solid #dfe6e3;
  border-radius: 16px;
}

.risk-header {
  display: flex;
  justify-content: space-between;
  gap: 20px;

  margin-bottom: 15px;
}

.risk-header h3 {
  margin: 0;

  color: #263a33;
}

.risk-levels {
  display: flex;
  gap: 8px;
}

.risk-levels span {
  padding: 5px 9px;

  border-radius: 6px;

  background: #f0f3f2;

  color: #63716c;

  font-size: 0.72rem;
  font-weight: 700;
}

.risk-levels .high {
  background: #f7e8e6;
  color: #a24c42;
}

.risk-card > p {
  color: #68766f;

  line-height: 1.7;
}

.mitigation {
  margin-top: 20px;
  padding: 18px;

  border-radius: 10px;

  background: #f4f8f6;
}

.mitigation strong {
  color: #176b5b;

  font-size: 0.78rem;

  text-transform: uppercase;
  letter-spacing: 0.08em;
}

.mitigation p {
  margin: 8px 0 0;

  color: #63716c;

  line-height: 1.6;
}

/* ASSUMPTIONS */

.info-card h3 {
  margin-top: 0;

  color: #21342d;

  font-size: 1.35rem;
}

.info-card strong {
  color: #176b5b;
}

/* TEAM */

.team-grid {
  display: grid;

  grid-template-columns: repeat(5, 1fr);

  gap: 16px;
}

.team-member {
  padding: 25px 15px;

  text-align: center;

  background: white;

  border: 1px solid #dfe6e3;
  border-radius: 14px;
}

.avatar {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 58px;
  height: 58px;

  margin: 0 auto 17px;

  border-radius: 50%;

  background: #e5f3ee;

  color: #176b5b;

  font-weight: 800;
}

.team-member h3 {
  margin: 0 0 6px;

  color: #263a33;

  font-size: 1rem;
}

.team-member p {
  margin: 0;

  color: #176b5b;

  font-size: 0.83rem;
  font-weight: 600;
}

/* FOOTER */

footer {
  margin-top: 110px;

  padding: 55px 6%;

  background: #102f29;

  color: white;
}

.footer-content {
  display: flex;

  justify-content: space-between;
  gap: 40px;

  width: min(1180px, 100%);
  margin: auto;
}

.footer-content strong {
  font-size: 1.4rem;
}

.footer-content p {
  max-width: 500px;

  color: rgba(255, 255, 255, 0.6);

  line-height: 1.6;
}

.footer-right {
  text-align: right;
}

/* RESPONSIVE */

@media (max-width: 900px) {
  nav {
    display: none;
  }

  .goal-grid,
  .scope-grid,
  .stakeholder-grid {
    grid-template-columns: 1fr;
  }

  .goal-card:last-child {
    grid-column: auto;
  }

  .team-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .timeline-item {
    grid-template-columns: 20px 1fr;
  }

  .timeline-date {
    grid-column: 2;
  }

  .timeline-content {
    grid-column: 2;
  }

  .risk-header {
    flex-direction: column;
  }

  .hero-meta {
    gap: 25px;
  }
}

@media (max-width: 600px) {
  .hero-inner {
    min-height: 72vh;

    padding: 65px 0;
  }

  .hero h1 {
    font-size: 4.2rem;
  }

  .hero-actions {
    flex-direction: column;

    align-items: flex-start;
  }

  .hero-meta {
    display: grid;

    grid-template-columns: repeat(2, 1fr);
  }

  .section {
    padding-top: 75px;
  }

  .large-card,
  .scope-card,
  .stakeholder-card,
  .risk-card,
  .info-card {
    padding: 23px;
  }

  .team-grid {
    grid-template-columns: 1fr;
  }

  .footer-content {
    flex-direction: column;
  }

  .footer-right {
    text-align: left;
  }
}
</style>
