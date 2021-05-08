<script>
let ti="CinemaTick - inicio";
let pagenumber="1";
import CustomButton from './CustomButton.svelte';
import Cartelera from './Cartelera.svelte';
import Socialicon from './Socialicon.svelte';
import Searconteiner from './Searchconteiner.svelte';
import Searchconteiner from './Searchconteiner.svelte';
import Grid from './Grid.svelte';
	
	let src = 'logocinematick.png';
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
<body>
	<div class="grid-container">
		<div class="menuhead">
			<br>
			<br>

			<div align="right">
				<!-- {src} is short for src={src} -->
				
				<img align="left" {src} alt="{namel}" class="logo" height="90" width="170" vertical-align="top" >
				
				<Socialicon nombre={"Instagram"}/> 
				<Socialicon nombre={"Facebook"}/> 
				<Socialicon nombre={"Twitter"}/> 
				<CustomButton nombre="LOGIN" on:click={handleClick} /> 
				<br><br>
				<br>
			</div>
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
				<h2>Suscribirse</h2>
				<input type="text" placeholder="Email..." name="suscrip"  ><br>
				<CustomButton nombre="SUSCRIBIRSE" on:click={handleClick} /> 
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

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #11809c;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>