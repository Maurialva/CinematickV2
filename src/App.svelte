<script>
let ti="CinemaTick - inicio";
let pagenumber="1";
import CustomButton from './CustomButton.svelte';
import Cartelera from './Cartelera.svelte';
import Socialicon from './Socialicon.svelte';
import Searconteiner from './Searchconteiner.svelte';
import Searchconteiner from './Searchconteiner.svelte';
import Grid from './Grid.svelte';
	
	let src = 'logocinematickv2.png';
		let namel = 'logo';
	function handleClick() 
	{
		ti="2";
	}
	function setpagename() {
	location.href='login.html';
}
</script>
<Grid {pagenumber}/>
<main>
<body>
	<div class="grid-container">
		<div class="menuhead">
			<br>
			<br>

			<div align="right">
				<!-- {src} is short for src={src} -->
				
				<img align="left" {src} alt="{namel}" class="logo"  width="16%" vertical-align="top" >
				<br>
			<br>
				<Socialicon nombre={"Instagram"}/> 
				<Socialicon nombre={"Facebook"}/> 
				<Socialicon nombre={"Twitter"}/> 
				<CustomButton class="login" on:click={()=>console.log("Clicked")}>
					LOGIN
				</CustomButton>
			
			</div>
			<br>
			<br>
			<div class="search-container">
					<Searchconteiner/>
			</div>	
		</div>
		{#if pagenumber==7}
		<div class="menuleft"></div> 
		{/if}
		<div class="menucenter">
		{#if pagenumber==1}
		<div id="cartelera">
			<Cartelera/>	
		</div>
		{/if}
		</div>  
		{#if pagenumber==1 }
		<div class="menuright">
			<div id="suscripcion">
				<h1>Suscribirse</h1>
				<input type="text" placeholder="Email..." name="suscrip"  ><br>
				<CustomButton class="suscripcion" on:click={()=>console.log("Clicked")}>
					SUSCRIBIRSE
				</CustomButton>
					</div>
					<div id="destacada">
						<h2>destacada</h2>
						<figure >
						<a href="https://www.instagram.com/"> <img class="destacada" src="p_sample.jpg" alt="Instagram" height="300" width=""></a>
						<figcaption>TITULO</figcaption>
					</figure>
					</div>
		</div>
		{/if}
		<div class="menufoot">
			<br>
			<a class="foot" href="http://localhost:5000/"> INICIO</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<a class="foot"  href="http://localhost:5000/"> SOBRE NOSOTROS</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<a class="foot" href="http://localhost:5000/"> CONTACTO</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<a class="foot" href="http://localhost:5000/"> AYUDA</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<br>
			<br>
		</div>
	  </div>
</body>
</main>
<style>
	main {
		text-align: center;
		padding-left: 10%;
		padding-right: 10%;
		max-width: 240px;
		margin: 0 auto;
		
	}

	:global(h1){
		color: #449fad;
		text-transform: uppercase;
		font-family: 'Tahoma', cursive;
		
		font-size: 330%;
		font-weight: 100;
	}
	

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
	.search-container
	{
		text-align: center;
		width: 100%;
		background-image:  linear-gradient(180deg,rgb(9, 31, 65) 0%, rgb(80, 146, 158) 56%, rgb(56, 213, 224) 100%);
		border-radius: 50px;
		
	}
	.menufoot
	{
		text-align: center;
		width: 98%;
		color: aliceblue;
		background-image:  linear-gradient(0deg,rgb(9, 31, 65) 0%, rgb(80, 146, 158) 56%, rgb(56, 213, 224) 100%);
		border-radius: 50px;
	
	}
</style>