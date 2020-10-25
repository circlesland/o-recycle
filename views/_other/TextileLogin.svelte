<script lang="ts">
  // import { SessionService } from "../../../kernel/services/sessionService";
  // // import { DagService } from "../../../kernel/services/dagService";
  // import type { User } from "../../../kernel/interfaces/user";
  // import { LoginState } from "../../../kernel/enums/loginState";
  // import type { ServiceError } from "@textile/hub-grpc/hub_pb_service";
  // import { DagService } from "../../../kernel/services/dagService";
  // import page from "page";
  // export let login: string = "";
  // export let loginProcess = LoginState.None;
  // export let user: User;
  // export let error: ServiceError;
  // import {navigateTo} from "../../../kernel/main";

  // let addrGatewayUrl = "";
  // SessionService.GetInstance().then((instance: SessionService) => {
  //   if (instance.hasSession) {
  //     navigateTo("odentity","blubb");
  //   }
  //   addrGatewayUrl = instance.addrGatewayUrl;
  // });

  // async function signInOrSignUpAsync() {
  //   if (login == null || login == "") return;
  //   loginProcess = LoginState.LoggingIn;
  //   let sessionService = await SessionService.GetInstance();
  //   let resp = await sessionService.signInOrSignUp(login);

  //   if (resp.error) {
  //     error = resp.error;
  //     loginProcess = LoginState.Error;
  //     return;
  //   }
  //   user = { email: sessionService.getUserMail(), name: sessionService.getUsername() };

  //   loginProcess = LoginState.LoggedIn;

  //   //     console.log(await TextileSession.Instance.listBuckets(key.getKey(), key.getSecret()));
  //   //     key = keys.getListList()[3];
  //   //     console.log(await TextileSession.Instance.listBuckets(key.getKey(), key.getSecret()));
  //   //     key = keys.getListList()[4];
  //   //
  //   //  console.log(await SessionService.GetInstance.listBuckets(key.getKey(), key.getSecret()));
  // }
  // async function dostuff() {
  //   let instance = await SessionService.GetInstance();
  //   let keys = await instance.listKeys();
  //   var key = keys.getListList()[2];
  //   await instance.listBuckets(key.getKey(), key.getSecret());
  //   let dag = new DagService();
  //   await dag.testhash();
  // }
</script>

<style>
  @media screen and (min-width: 600px) {
    .wrap {
      height: 95%;
    }
  }
  @media screen and (min-width: 1024px) {
    .wrap {
      height: 85%;
    }
  }
  @media screen and (min-width: 1600px) {
    .wrap {
      height: 75%;
    }
  }
  .grid {
    @apply h-full w-full;
    grid-template-areas:
      "header"
      "main"
      "footer";
    grid-template-rows: 40px 1fr auto;
    grid-template-columns: 1fr;
  }
  header {
    grid-area: header;
  }
  main {
    grid-area: main;
    @apply overflow-y-scroll h-full bg-gray-100 p-8;
  }
  footer {
    grid-area: footer;
  }
</style>
<!-- 
<div
  class="flex flex-col items-center justify-center h-screen bg-white bg-center bg-cover  bg-grey-lighter"
  style="background-image: url(https://source.unsplash.com/7awMZWDS4rg)">
  <div
    class="justify-center w-full h-full max-w-md bg-white border border-gray-300 rounded-lg shadow-2xl wrap md:m-12">
    <div class="grid">
      <header
        class="flex flex-col justify-center border-b border-gray-300 bg-grey-lighter">
        <div class="font-bold text-center uppercase text-primary">Login</div>
      </header>
      {#if loginProcess != LoginState.LoggedIn}
        <main>
          <h1 class="text-3xl font-black text-center font-title text-primary">
            Willkommen,
            <br />auf Omo Earth
          </h1>
          <p class="py-4 text-sm text-center text-gray-700">
            Die Menschen auf Omo Earth nennen sich Omo Sapiens. Jeder Omo
            entwickelt und kontrolliert 100% seiner eigenen Daten und Apps und
            speichert diese in seinem privaten Omo Haus. Um als Omo Sapien dein
            Haus zu öffnen oder ein neues Omo Sapien Haus zu bauen, melde dich
            unten über unseren Hosting Partner textile.io an.
          </p>
          <div class="flex p-2 mx-auto">
            <img
              src="https://github.com/omoearth/omo-marketplace/workflows/dev.omo.earth/badge.svg"
              alt="deployBadge" />
            <img
              src="https://github.com/omoearth/textile/workflows/hub.dev.omo.earth/badge.svg"
              alt="deployBadge" />
          </div>
        </main>
      {/if}
      {#if loginProcess == LoginState.LoggedIn}
        <main>
          <p class="text-2xl text-center  font-title text-primary">
            Herzlich Willkommen,<br />{user.name}
          </p>{user.email}
        </main>
      {/if}

      <footer class="p-6 text-sm border-t border-gray-300">
        {#if loginProcess == LoginState.None}
          <div>
            <form method="POST" onsubmit="return false;">
              <p class="p-1 text-gray-700">Wähle deinen Haus Anbieter</p>
              <div class="flex">
                <div
                  class="w-20 h-20 p-4 mr-1 bg-gray-100 bg-gray-200 border border-gray-300 rounded-lg">
                  <img src="images/textile.png" />
                </div>
                <div
                  class="w-20 h-20 p-3 mr-1 text-xs text-center text-gray-500 bg-gray-100 rounded-lg">
                  more coming soon
                </div>
              </div>
              <p
                class="p-2 mt-2 text-gray-600 bg-gray-100 border border-gray-300 rounded-lg">
                {addrGatewayUrl}
              </p>

              <p class="p-1 text-gray-700">Anmelden</p>
              <div
                class="w-full px-2 pt-1 mb-2 bg-gray-200 border border-gray-300 rounded-lg focus:outline-none">
                <label
                  for="email"
                  class="block text-xs font-medium text-gray-600">Email</label>

                <input
                  type="text"
                  name="email"
                  class="w-full text-xl text-gray-700 bg-gray-200 border border-transparent rounded-lg  focus:outline-none"
                  bind:value={login} />
              </div>
              <div
                class="w-full p-3 font-bold text-center text-white uppercase rounded-lg bg-primary"
                on:click={() => signInOrSignUpAsync()}>
                Omo Haus öffne dich
              </div>
            </form>
          </div>
        {/if}
        {#if loginProcess == LoginState.LoggingIn}
          <div class="p-12 text-lg bg-gray-200 rounded-lg">
            Dein Türschlüssel wurde an deine Email geschickt. Bitte öffne den
            Link in deiner Email, um dein Haus aufzuschließen.
          </div>
        {/if}
        {#if loginProcess == LoginState.Error}
          <div class="p-12 text-lg text-white bg-red-400 rounded-lg">
            <p>{error.message}</p>
          </div>
        {/if}
        {#if loginProcess == LoginState.LoggedIn}
          <div class="p-8">App-Navbar</div>
        {/if}
        <button on:click={() => navigateTo("wallet","index")}>klick mich</button>
      </footer>
    </div>
  </div>
</div> -->
