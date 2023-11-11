<script>
  let mode = 1;
</script>

<main>
  <div class="drinkr">Drinkr</div>
  {#if mode == 0}
    <div class="beer">
      <button class="btn-login" on:click={() => (mode = 2)}>Connexion</button>
      <img
        src="https://assets.stickpng.com/thumbs/6119457ef8fe340004e0d29e.png"
        alt="Beer"
        width="64px"
      />
    </div>
    <h1 class="title">Envie d'un coup<br /> de <i>boost</i> ?</h1>
    <button class="btn-signup" on:click={() => (mode = 1)}>Je m'inscris</button>
  {:else if mode == 1}
    <div class="container">
      <div class="elt">
        <div class="field">Nom du bar</div>
        <input type="text" />
      </div>

      <div class="elt">
        <div class="field">Numéro de SIRET</div>
        <input type="text" />
      </div>

      <div class="elt">
        <div class="field">Email</div>
        <input type="email" />
      </div>

      <div class="elt">
        <div class="field">Nom du propriétaire</div>
        <input type="text" />
      </div>

      <div class="elt">
        <div class="field">Téléphone</div>
        <input type="phone" />
      </div>

      <div class="elt">
        <div class="field">Mot de passe</div>
        <input type="password" />
      </div>
    </div>
  {:else if mode == 2}
    <h2>Mon espace</h2>
  {/if}
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,500;0,700;0,900;1,700&display=swap");
  .title {
    font-family: "Poppins", sans-serif;
    font-weight: 900;
    margin-top: 30vh;
  }
  main {
    width: 100vw;
    height: 100vh;
    overflow: hidden;
  }

  .btn-signup {
    font-family: "Poppins", sans-serif;
    font-weight: 700;
    color: white;
    font-size: 24px;
    background-color: #e68e12;
  }

  .drinkr {
    position: absolute;
    top: 3vh;
    left: 3vh;
    font-family: "Poppins", sans-serif;
    font-weight: 900;
    font-size: 24px;
  }

  .field {
    font-family: "Poppins", sans-serif;
    font-weight: 500;
    justify-self: start;
  }

  .beer {
    display: flex;
    align-items: center;
    position: absolute;
    right: 2vw;
    top: 2vh;
  }

  .btn-login {
    color: black;
    font-size: 20px;
    font-family: "Poppins", sans-serif;
    font-weight: 700;
    background-color: transparent;
    margin: 1vw;
    border: 4px #e68e12 solid;
  }

  .container {
    margin-top: 7vh;
    display: flex;
    flex-direction: column;
  }

  .elt {
    margin: 1vh;
  }
</style>
