<script>
  let mode = 0;
</script>

<main>
  <div class="banner">
    <div class="drinkr">Drinkr</div>
    {#if mode == 0}
      <h1 class="title">Envie de sortir ?</h1>
      <button class="btn-signup" on:click={() => (mode = 1)}
        >Je m'inscris</button
      >
      <div class="store-container">
        <img
          src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
          alt="apple-store"
        />
        <img
          src="https://lh3.googleusercontent.com/q1k2l5CwMV31JdDXcpN4Ey7O43PxnjAuZBTmcHEwQxVuv_2wCE2gAAQMWxwNUC2FYEOnYgFPOpw6kmHJWuEGeIBLTj9CuxcOEeU8UXyzWJq4NJM3lg=s0"
          alt="play-store"
        />
      </div>

      <div class="user-satisfaction">
        <div style="margin-right: 10vw;">
          Faites de nouvelles <br />rencontres autrement !
          <div class="sub_text">
            <em>
              "Cette application m'a permis de découvrir <br />de nouvelles
              personnes de manière amusante"</em
            ><br /><b>Nathan B.</b>
          </div>
        </div>
        <img
          style="border-radius: 20px;"
          src="https://imgs.search.brave.com/2dOlZCEsi5ICFWrW9qBCcf23AiOKP6wCB_4z5P9h-wk/rs:fit:860:0:0/g:ce/aHR0cHM6Ly9tZWRp/YS5pc3RvY2twaG90/by5jb20vaWQvNjg0/OTM2NDI4L3Bob3Rv/L2dyb3VwLW9mLXBl/b3BsZS1pbi10aGUt/YmFyLmpwZz9zPTYx/Mng2MTImdz0wJms9/MjAmYz1GWTlDWV9i/bEt3TmJGTkpCd0Vj/ZnVheW16cWFzRG9s/LWk2U25ZNkhoX0xn/PQ"
          alt=""
        />
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
  </div>
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,500;0,700;0,900;1,700&display=swap");
  .banner {
    background: linear-gradient(
      0deg,
      rgba(240, 231, 152, 1) 0%,
      rgba(255, 217, 136, 1) 100%
    );
    width: 100vw;
    height: 100vh;
    border: 1px solid black;
  }
  .title {
    font-family: "Poppins", sans-serif;
    font-weight: 900;
    margin-top: 30vh;
    margin-bottom: 15vh;
  }
  main {
    width: 100vw;
    height: 110vh;
  }

  .btn-signup {
    font-family: "Poppins", sans-serif;
    font-weight: 700;
    color: white;
    font-size: 24px;
    background-color: #e68e12;
    margin-bottom: 10vh;
  }

  .sub_text {
    margin-top: 2vh;
    font-family: "Poppins", sans-serif;
    font-weight: 500;
    font-size: 14px;
  }

  .drinkr {
    position: absolute;
    top: 3vh;
    left: 3vh;
    font-family: "Poppins", sans-serif;
    font-weight: 900;
    font-size: 24px;
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
    margin-bottom: 5vh;
  }

  .store-container > img {
    height: 3.5rem;
    margin: 0.5rem;
  }

  .user-satisfaction {
    font-family: "Poppins", sans-serif;
    font-weight: 700;
    color: black;
    font-size: 24px;
    background-color: white;
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  button {
    font-family: "Poppins", sans-serif;
    font-weight: 700;
    color: white;
    font-size: 24px;
    background-color: #e68e12;
    margin-bottom: 10vh;
  }

  input {
    font-family: "Poppins", sans-serif;
    font-weight: 500;
    font-size: 24px;
    border: 1px solid black;
    border-radius: 5px;
    padding: 0.5rem;
  }

  h2 {
    font-family: "Poppins", sans-serif;
    font-weight: 700;
    color: black;
    font-size: 24px;
    background-color: white;
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
