<div class="ts-guides-section">

# Step-by-step guides

Clear, practical workflows that show you exactly how to complete tasks in Alfred Co.Host — from setup to daily operations.

## Setup & Library

<div class="ts-guides-grid">

  <a class="card ts-guide-card" href="#/procedures/properties_p.md">
    <h3>Manage properties</h3>
    <p>Create, edit, or delete properties in your host dashboard.</p>
  </a>

  <a class="card ts-guide-card" href="#/procedures/setup_library_p.md">
    <h3>Set up your library</h3>
    <p>Get started with your library setup — from quick launch to full control.</p>
  </a>

  <a class="card ts-guide-card" href="#/procedures/libraries_p.md">
    <h3>Add library content</h3>
    <p>Add text, media, or custom items to your property library so Alfred can use them in replies.</p>
  </a>

  <a class="card ts-guide-card" href="#/procedures/test_assistant.md">
    <h3>Test assistant</h3>
    <p>Test how Alfred responds before going live. Make sure everything works perfectly for your guests.</p>
  </a>

</div>

## Writing & Content

<div class="ts-guides-grid">

  <a class="card ts-guide-card" href="#/procedures/writing_tips.md">
    <h3>How to write great library items</h3>
    <p>Learn best practices for writing clear, effective library content that helps Alfred communicate with guests.</p>
  </a>

  <a class="card ts-guide-card" href="#/procedures/writing_custom_items.md">
    <h3>Writing custom items</h3>
    <p>Add custom items to your library to cover property-specific details beyond standard categories.</p>
  </a>

  <a class="card ts-guide-card" href="#/procedures/writing_policies.md">
    <h3>Writing internal policies</h3>
    <p>Create custom policies to control Alfred's behavior in specific situations.</p>
  </a>

</div>

## Subscriptions & Billing

<div class="ts-guides-grid">

  <a class="card ts-guide-card" href="#/procedures/subscriptions_p.md">
    <h3>Manage subscriptions</h3>
    <p>Manage property subscriptions and control when your assistant is live.</p>
  </a>

  <a class="card ts-guide-card" href="#/procedures/change_payment_card_p.md">
    <h3>Change payment card</h3>
    <p>Update the payment card used for all your Alfred Co.Host subscriptions.</p>
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

/* Titoli delle sezioni */
.ts-guides-section h2 {
  margin-top: 2.5em;
  margin-bottom: 1.2em;
  text-align: left;
  font-size: 1.5em;
  font-weight: 600;
}

.ts-guides-section h2:first-of-type {
  margin-top: 0;
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
