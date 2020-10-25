<script lang="ts">
    export let navigateTo: (dapp:string,page:string)=>{};

  // import { SessionService } from "../../../kernel/services/sessionService";
  // let user: { name: string; email: string };
  // SessionService.GetInstance().then((session) => {
  //   user = { name: session.getUsername(), email: session.getUserMail() };
  // });
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

<!-- <div
  class="flex flex-col items-center justify-center h-screen bg-white bg-center bg-cover  bg-grey-lighter"
  style="background-image: url(https://source.unsplash.com/7awMZWDS4rg)">
  <div
    class="justify-center w-full h-full max-w-md bg-white border border-gray-300 rounded-lg shadow-2xl wrap md:m-12">
    <div class="grid">
      <header
        class="flex flex-col justify-center border-b border-gray-300 bg-grey-lighter">
        <div class="font-bold text-center uppercase text-primary">Login</div>
      </header>
      <main>
        {#if user}
        <h1 class="text-3xl text-center font-title text-primary">
          Willkommen {user.name},
          <br />{user.email}
        </h1>
        {/if}
        <p class="py-4 text-sm text-center text-gray-700">Yeah!</p>
      </main>

      <footer class="p-6 text-sm border-t border-gray-300">
        <div>
          <form method="POST" onsubmit="return false;">
            <div
              class="w-full p-3 font-bold text-center text-white uppercase rounded-lg bg-primary">
              Oida!
            </div>
          </form>
        </div>
      </footer>
    </div>
  </div>
</div> -->
BLUBB