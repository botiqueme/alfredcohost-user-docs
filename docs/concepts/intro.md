# Step-by-step guides

Use these workflows when you want to perform a concrete task in Alfred Co.Host.

<div class="grid">

  <a class="card" href="#/get-started.md">
    <h3>Quickstart</h3>
    <p>Set up Alfred for the first time and connect your properties.</p>
  </a>

  <a class="card" href="#/procedures/properties_p.md">
    <h3>Manage properties</h3>
    <p>Add, edit, or deactivate properties and units in your account.</p>
  </a>

  <a class="card" href="#/procedures/libraries_p.md">
    <h3>Manage property information</h3>
    <p>Update the content Alfred uses to reply to guests.</p>
  </a>

  <a class="card" href="#/procedures/subscriptions_p.md">
    <h3>Manage subscriptions</h3>
    <p>View, update, or cancel your current subscription.</p>
  </a>

  <a class="card" href="#/procedures/plans_billing_cycles_p.md">
    <h3>Plans &amp; billing cycles</h3>
    <p>Change plans and control how and when you are billed.</p>
  </a>

  <a class="card" href="#/procedures/change_payment_card_p.md">
    <h3>Change payment card</h3>
    <p>Update the card used to charge your subscription.</p>
  </a>

</div>

<style>

/* Grid more compact */
.grid {
  gap: 20px !important;         /* meno spazio tra le card */
  padding: 0 16px !important;   /* un po' meno padding laterale */
}

/* Card sizing uniform + radius 5 */
.card {
  border-radius: 5px !important;                   /* raggio più piccolo */
  padding: 24px 20px !important;
  width: calc(33.333% - 20px) !important;          /* 3 per riga */
  max-width: 260px !important;
  min-width: 220px !important;

  /* Equal height magic */
  height: 180px !important;                        /* ALTEZZA STANDARD */
  display: flex !important;
  flex-direction: column !important;
  justify-content: center !important;              /* centra titolo + testo */
  align-items: center !important;
  text-align: center !important;
}

/* Card text spacing più compatto */
.card h3 {
  margin: 0 0 6px 0 !important;
}

.card p {
  margin: 0 !important;
}

/* Mobile: card a larghezza piena */
@media (max-width: 600px) {
  .card {
    width: 100% !important;
    height: auto !important;     /* Lascia che crescano su mobile */
  }
}
</style>
