<script>
    //Version 1
    export let number_1 = 0;
    
    function numbers_1() {
        number_1 = Math.floor(Math.random() * (50 - 0 + 1)); 
        number_1 = number_1;
    }


    //Version 2
    let num_array = [];
    let duplicates = false;
    
    function addToArray() {
        const x = 0;
        num_array = [];
        while (num_array.length < 3) {
            const x = Math.floor(Math.random() * 50) + 1;
            if (num_array.includes(x)) {
                num_array.push(x + 1);
            }
            else {
                num_array.push(x);
            };
            num_array = num_array;
        }

    }

</script>



<div class="container mt-5 p-4" id="main">



<!--Version 1-->
    <h1>Lottery Number Generator V1</h1>
    <p>Version 1 of this tool generates a random number between 1 and 50.</p>

    <button on:click={numbers_1}>Generate</button>

    <p>Your number is: {number_1}</p>
    <hr>
<!--END-->

<!--Version 2-->
<h1>Euromillions Number Generator V2</h1>
<p>Version 2 of this tool generates 3 numbers and pushes them to an array. The results of which are then diplayed.</p>

<button type="button" class="btn btn-primary" on:click={addToArray}>Generate numbers</button>


<div class="container pt-4"> 
    <div class="row">
        {#if (num_array[0] == undefined)}
        <div class="col"><div class="num-box"><span id="num">0</span></div></div> 
        <div class="col"><div class="num-box"><span id="num">0</span></div></div> 
        <div class="col"><div class="num-box"><span id="num">0</span></div></div> 

        {:else}
        <div class="col"><div class="num-box"><span id="num">{num_array[0]}</span></div></div> 
        <div class="col"><div class="num-box"><span id="num">{num_array[1]}</span></div></div> 
        <div class="col"><div class="num-box"><span id="num">{num_array[2]}</span></div></div> 
        {/if}
       
    </div>



 </div>

<!--END-->






</div>

<style>
    #main {
        max-width: 1000px;
    }
    .num-box {
        margin:auto;
        border-style: solid;
        border-radius: 60px;
        width: 100px;
        height:100px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    #num {
        font-family: Arial, Helvetica, sans-serif;
        font-size: xx-large;
    }
</style>