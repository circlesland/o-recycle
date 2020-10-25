<script lang="ts">
    export let navigateTo: (dapp:string,page:string)=>{};

    let notifications = [{
        title: "trusted",
        type: "trust 1",
        address: "0x765asfhopasjnfodguzagsfoiuasdfkjbaskdbfj"
    },
    {
        title: "waiting for trust 2",
        type: "trust 2",
        address: "0x765asfhopasjnfodguzagsfoiuasdfkjbaskdbfj"
    },
    {
        title: "waiting for trust 2",
        type: "trust 2",
        address: "0x765asfhopasjnfodguzagsfoiuasdfkjbaskdbfj"
    }];
</script>
<style>
    .card {
        @apply mb-2 border border-gray-200 rounded p-4
    }
</style>

<h1 class="pb-2 text-3xl font-bold border-b border-gray-400 text-primary">Unlock Your Safe</h1>

<p class="mb-4 text-xl text-primary">Your new GnosisSafe Address: 0xai7s6drtf8aubwl3diugasdo8fuga329</p>

<div class="mt-4 mb-2 text-xl text-primary">Waiting For Trust</div>
<p class="mb-5">Share your link to get trusted: <br> <span class="text-red-500">https://yourtrustlink.eth.link/#!/0x986dft7a8sodbfao8sdfga8sdofhbiasbdfiladsf</span></p>

{#each notifications as n}
    <div class="card">{n.title} --- {n.type} --- {n.address}</div>
{/each}

<button class="text-gray-400 bg-gray-200" on:click={()=>navigateTo("Wallet","safe")}>create account</button>
<br>

