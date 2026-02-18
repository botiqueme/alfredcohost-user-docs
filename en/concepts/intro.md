<div class="ts-guides-section">

# Understand how Alfred works

Not sure where to start? This page walks you through Alfred’s core concepts and the basics of how the platform works — in simple, practical terms, so everything makes sense even if you’re completely new.

<div class="ts-guides-grid">

  <a class="card ts-guide-card" href="#/en/concepts/what-alfred-can-do_c.md">
    <h3>What Alfred can do</h3>
    <p>Discover Alfred's capabilities and how it helps your guests 24/7 through messaging platforms.</p>
  </a>

  <a class="card ts-guide-card" href="#/en/concepts/properties_c.md">
    <h3>Properties</h3>
    <p>Learn how properties work and how Alfred links guests to the right unit.</p>
  </a>

  <a class="card ts-guide-card" href="#/en/concepts/libraries_c.md">
    <h3>Libraries</h3>
    <p>Build the information Alfred uses to answer guests for each property.</p>
  </a>

  <a class="card ts-guide-card" href="#/en/concepts/plans_billing_cycles_c.md">
    <h3>Plans & billing cycles</h3>
    <p>Learn how plans, subscriptions, and billing cycles work across your properties.</p>
  </a>

  <a class="card ts-guide-card" href="#/en/concepts/property-identifiers_c.md">
    <h3>Property identifiers</h3>
    <p>Understand the identifiers Alfred needs to connect each guest to the right apartment.</p>
  </a>

  <a class="card ts-guide-card" href="#/en/concepts/hands_off_c.md">
    <h3>Hands off</h3>
    <p>Learn how Alfred escalates conversations to your team when guests need human help.</p>
  </a>


</div>

</div>

<style>
/* Contenitore centrale, come Mosaic */
.ts-guides-section {
  max-width: 1040px;
  margin: 0 auto;
  padding: 40px 40px 60px 40px; /* stessa aria SX/DX per titolo, testo e card */
}

/* Titolo + paragrafo allineati a sinistra, come Mosaic */
.ts-guides-section h1 {
  margin-top: 0;
  margin-bottom: 0.5em;
  text-align: left;
}

.ts-guides-section > p {
  margin-top: 0;
  margin-bottom: 1.8em;
  text-align: left;
}

/* Griglia in stile Mosaic: 3 card per riga, allineata a sinistra */
.ts-guides-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  justify-content: flex-start;   /* NON centrata, parte da sinistra */
}

/* Card: usiamo .card globale + aggiustiamo solo layout */
.ts-guide-card {
  border-radius: 8px !important;
  width: calc(33.333% - 16px);
  min-width: 260px;
  max-width: 280px;
  height: 140px;
  padding: 18px 16px !important;

  display: flex !important;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;       /* testo allineato a sinistra come Mosaic */

  text-align: left;
}

/* Testi dentro la card */
.ts-guide-card h3 {
  margin: 0 0 6px 0 !important;
}

.ts-guide-card p {
  margin: 0 !important;
}

/* Responsive */
@media (max-width: 900px) {
  .ts-guides-section {
    padding: 24px 20px 40px 20px;
  }

  .ts-guide-card {
    width: 100%;
    max-width: 100%;
    height: auto;
  }
}
</style>
