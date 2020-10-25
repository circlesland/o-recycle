<script lang="ts">
    export let navigateTo: (dapp:string,page:string)=>{};
</script>

<main class="h-full p-8 overflow-y-scroll bg-gray-100">
    <h1 class="pb-2 text-3xl font-bold text-primary">
        Welcome to the Circles Lite Wallet
    </h1>
    <p class="">The Circles Lite Wallet is build on ipfs</p>
</main>

<footer class="flex p-4">
    <button
        class="w-full"
        on:click={() => navigateTo('wallet', 'login')}>login</button>
    <button
        class="w-full"
        on:click={() => navigateTo('wallet', 'register')}>register</button>
</footer>
