<script lang="ts">
  import { navigateTo, o } from "o-types";

  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  // import { navigateTo } from "../../kernel/viewRegistry";
  // import { CirclesWrapper } from "../../kernel/circles-protocol/circlesActions";
  let seedPhrase = "";
  function login() {
    // if (seedPhrase == "") return;
    // let account = CirclesWrapper.safeOwnerFromKeyphrase(seedPhrase);
    // //@todo catch some errors
    // CirclesWrapper.storeAccount(account);
    // navigateTo("safe");
    alert("loginaction");
  }
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

<div class="grid">
  <header
    class="flex flex-col justify-center border-b border-gray-300 bg-grey-lighter">
    <div class="font-bold text-center uppercase text-primary">Login</div>
  </header>

  <main class="overflow-y-scroll h-full bg-gray-100 p-8;">
    <p class="py-4 text-sm text-center text-gray-700">Yeah!</p>
  </main>

  <footer class="p-6 text-sm border-t border-gray-300">
    <div>
      <!-- <form method="POST" onsubmit="return false;">
        <div
          class="w-full p-3 font-bold text-center text-white uppercase rounded-lg bg-primary">
          Oida!
        </div>
      </form> -->
    </div>
  </footer>
</div>

<!-- 

<div class="p-8 bg-gray-100 ">
  <h1 class="pb-2 text-3xl font-bold text-primary">Login</h1>
</div>
<div class="h-full overflow-y-scroll">
  <div class="p-4 ">
    <h3 class="text-sm font-medium text-primary">
      Please enter your Seedphrase
    </h3>
    <div class="flex flex-col bg-white border rounded box ">
      <textarea
        placeholder="word1 word2 ... word24"
        bind:value={seedPhrase}
        class="flex-1 p-2 m-1 bg-transparent text-grey-darkest" />
    </div>
    <button
      class="w-full mt-2"
      on:click={() => navigateTo({ dapp: o.WALLET, route: 'wallet' }, dispatch)}>login</button>
  </div>
</div> -->
