<script>
	export let search;
	let product = 0;
	$: if(product<0)
	{
		alert("Can't < 0")
		product = 0
	} 
	else if(product > 20){
		alert("Can't >20")
		product =20
	}
	
</script>
<div class="container">
	<div class="search">
	<input placeholder="Search">
	<button  on:click={() => search}>Search</button>
	</div>
    <div class="card">
        <div class="card-title">
            <img src="https://th.bing.com/th/id/R.88a8464261f2ce6709d8f614256dcad5?rik=WVu8GN3e%2fEjyQw&riu=http%3a%2f%2fwww.hdwallpaper.nu%2fwp-content%2fuploads%2f2015%2f12%2fNaruto_Shippuden_15.jpg&ehk=l6ncRD4saee3iB9pTdQ1Qs7RIEBg2iPBgyQPyLrpQE4%3d&risl=&pid=ImgRaw&r=0" alt="">
        </div>
        <div class="card-body">
            <span>NARUTO</span> <br>
            <span>Naruto Shipudden</span>
        </div>
        <div class="card-end">
					<button on:click={()=> product-=1}>-</button>
					<span>{product}</span>
					<button on:click={()=> product+=1}>+</button>
        </div>
    </div>
</div>
<style>
	img{
		width: 200px;
		margin: 10px;
		border-radius:10px;
	}
	.card{
		/* background: blue; */
		border-radius: 10px;
		width:220px;
		box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
	}
	.card-body{
	text-align: center;
	}
	.card-end{
	text-align: center;
		padding: 7px
	}
</style>