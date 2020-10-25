<script lang="ts">
    export let navigateTo: (dapp:string,page:string)=>{};
</script>

<h1 class="pb-2 text-3xl font-bold text-primary">Register</h1>
<div class="col sm:w-1/2">
    <p class="mb-4 text-lg text-primary">Your new GnosisSafe Address: <br>0xai7s6drtf8aubwl3diugasdo8fuga329</p>
    <div class="flex flex-col bg-white border rounded shadow box">
    <div class="px-3 py-2 border-b box__title bg-grey-lighter"><h3 class="text-sm font-medium  text-primary">Please save your Seedphrase*</h3></div>
    <textarea placeholder="word1 word2 word3 word4 .... word23 word24" class="flex-1 p-2 m-1 bg-transparent text-primary"></textarea>
    </div>
<button class="mt-2" on:click={()=>navigateTo("wallet","unlockSafe")}>Yes I have saved my Seedphrase</button>
<p class="mt-2 text-xs text-gray-500">*Your seedphrase is like you password, please write it down and store it somewhere save. When you lose your seedphrase you will never be able to login or recover your Circles Account</p>

</div>


<button on:click="{()=>navigateTo("wallet","index")}">zum index</button>