<script lang="ts">
    export let navigateTo: (dapp:string,page:string)=>{};
    // import { CirclesWrapper } from "../../kernel/circles-protocol/circlesActions";
    import moment from "moment"
    // import { theGraphClient } from "../../kernel/circles-protocol/theGraph/theGraphClient";
    // import type { ActivitiesQuery } from "../../kernel/circles-protocol/theGraph/generated";

    // let balance = "";
    // let safeaddress = "";
    // let activitiesquery: ActivitiesQuery;
    // async function f() {
    //     let account = CirclesWrapper.restoreAccount();
    //     safeaddress = await CirclesWrapper.getSafeAddress(account);
    //     balance = await CirclesWrapper.getBalance(account, safeaddress);
    //     activitiesquery = (
    //         await theGraphClient.activities({
    //             safeAddress: safeaddress.toLowerCase(),
    //         })
    //     ).data;
    // }

    // f();

</script>

<style>
    .card {
        @apply mb-2 border border-gray-200 rounded p-4;
    }
</style>
<!-- 
<main class="overflow-y-scroll">
<div class="h-32 pt-6 text-4xl font-bold text-center text-white bg-primary">
    <p>{balance} CRC</p>
    <p class="text-xs text-gray-400">Safe: {safeaddress.toLowerCase()}</p>
</div>
<div class="p-4 bg-gray-200">
    <div class="p-2 text-lg text-primary">Your Transactions</div>
        {#if activitiesquery}
            {#each activitiesquery.notifications as n}
            <div class="flex w-full bg-white border-b border-gray-200 h-14 text-primary">
                <div class="flex flex-col justify-center w-12 h-12 text-center">
                <i class="text-2xl fas fa-arrow-down" />
                </div>
                <div class="flex-1 px-2 py-2 text-base">
                    {n.type}
                <p class="-mt-2 text-xs text-gray-500">
                    {moment.unix(n.time).locale('en').fromNow()} from {n.transfer.from} to {n.transfer.to}
                </p>
                </div>
                <div class="h-12 px-3 py-2 text-2xl font-bold font-title text-secondary">
                </div>
            </div>
            {/each}
        {/if}
    </div>
</main>

<footer>
    <button on:click={() => navigateTo('trustSomeone')}>trustSomeone</button>
<button on:click={() => navigateTo('getTrust')}>shareProfile</button>
  
</footer> -->
