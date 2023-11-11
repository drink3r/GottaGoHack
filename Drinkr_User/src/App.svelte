<script>
  let mode = 0;
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
    <h1 class="title">Envie de sortir ?</h1>
    <button class="btn-signup" on:click={() => (mode = 1)}>Je m'inscris</button>
    <div class="store-container">
        <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" alt="apple-store" />
        <img src="https://lh3.googleusercontent.com/q1k2l5CwMV31JdDXcpN4Ey7O43PxnjAuZBTmcHEwQxVuv_2wCE2gAAQMWxwNUC2FYEOnYgFPOpw6kmHJWuEGeIBLTj9CuxcOEeU8UXyzWJq4NJM3lg=s0" alt="play-store" />
    </div>
  {:else if mode == 1}
    <div class="container">
      <div class="elt">
        <label class="register-label" for="email">Email</label>
        <input type="email" name="email" />
      </div>
      <div class="elt">
        <label class="register-label" for="first_name">Prenom</label>
        <input type="text" name="first_name" />
      </div>
      <div class="elt">
        <label class="register-label" for="name">Nom</label>
        <input type="text" name="name" />
      </div>
      <div class="elt">
        <label class="register-label" for="password">Mot de passe</label>
        <input name="password" type="password" />
      </div>

      <div class="elt">
        <button type="submit" on:click={() => (mode = 2)}>S'inscrire</button>
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

.register-label {
    display: block;
}

.store-container {
    padding: 1rem;
}

.store-container > img {
    height: 3.5rem;
    margin: .5rem;
}
</style>
