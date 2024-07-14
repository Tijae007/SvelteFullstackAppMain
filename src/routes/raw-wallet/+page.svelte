<script lang="ts">
    import { PrivateKey } from '@bsv/sdk'
    
    let WIF:string
    let address:string
    
    function createKeys () {
    
        const privKey = PrivateKey.fromRandom()
        WIF = privKey.toWif()
        console.log("Private Key WIF format is ", WIF)
        address = privKey.toAddress()
        console.log("Your bitcoin address is ", address)
    }
    
    </script>
    
    <section class="mt-10 pt-10 w-full max-w-xl p-12 mx-auto rounded-lg shadow-xl dark:bg-white/10 bg-white/30 ring-1 ring-gray-900/5 backdrop-blur-lg">
        <br>
        <button class=" bg-yellow-500 text-white p-2 rounded mx-auto" on:click={createKeys}> Generate New Wallet Keys </button>
        <br>
        <br>
        <p>Private Key WIF format is {WIF}</p>
        <br>
        <p>Your BitCoin Address is {address}</p>
    </section>
    
    