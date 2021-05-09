<script>

let pagenumber="2";
let ti="CinemaTick - inicio";
import CustomButton from './CustomButton.svelte';
import Cartelera from './Cartelera.svelte';
import Socialicon from './Socialicon.svelte';
import Customtextinput from './Customtextinput.svelte';
import Searchconteiner from './Searchconteiner.svelte';
import Grid from './Grid.svelte';
import Customfigure from './Customfigure.svelte';
import Login from './Login.svelte';
import Customhead from './Customhead.svelte';


	
function clickbutton() {
	pagenumber="2";
}		

</script>
<Grid {pagenumber} {ti}/>

<main>
<body>
	<div class="grid-container">
		<div class="menuhead">
	
			<Customhead/>
			<!-- 
			<div align="right">
				 
				
				<img align="left" src='logocinematickv2.png' alt="logo" class="logo"  width="16%" vertical-align="top" >
				
				
		
			
				<Socialicon nombre={"Instagram"}/> 
				<Socialicon nombre={"Facebook"}/> 
				<Socialicon nombre={"Twitter"}/> 
				<CustomButton class="login" on:click={()=>clickbutton()} >
					LOGIN
				</CustomButton>
				
			</div>
			
				<h2>Todas las peliculas en un lugar, cinematick&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</h2>
			
			
			<div class="search-container">
					<Searchconteiner/>
			</div>	-->
		</div>
		{#if pagenumber==7}
		<div class="menuleft"></div> 
		{/if}
		<div class="menucenter">
		{#if pagenumber==1}
		<div id="cartelera">
			<Cartelera/>	
		</div>
		{:else if pagenumber==2}
		<Login/>
		{/if}

		</div>  
		{#if pagenumber==1 }
		<div class="menuright">
			<div id="suscripcion">
				<h1>Suscribirse</h1>
			<Customtextinput texto="EMAIL..." txnom="suscripcion"/>
				<CustomButton class="suscripcion" on:click={()=>console.log("Clicked")}>
					SUSCRIBIRSE
				</CustomButton>
					</div>
					<div id="destacada">
						<h2>destacada</h2>
					<Customfigure figname="TITULO"/>
					</div>
		</div>
		{/if}
		<div class="menufoot">
			
			<h3>
			<a class="foot" href="#?ti=1" style="text-shadow:0px 4px 6px rgba(0,0,0,0.76) ;"> INICIO</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<a class="foot"  href="http://localhost:5000/"  style="text-shadow:0px 4px 6px rgba(0,0,0,0.76) ;"> SOBRE NOSOTROS</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<a class="foot" href="http://localhost:5000/" style="text-shadow:0px 4px 6px rgba(0,0,0,0.76) ;"> CONTACTO</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<a class="foot" href="http://localhost:5000/" style="text-shadow:0px 4px 6px rgba(0,0,0,0.76) ;"> AYUDA</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			
			<br></h3>
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
		color: #ffffff;
		text-transform: uppercase;
		font-family: 'Tahoma', cursive;
		text-align: center;
		font-size: 230%;
		font-weight: 1;
		text-shadow:0px 5px 10px rgba(41, 39, 39, 0.76) ;
	}
	:global(h2){
		color: #ffffff;
		text-transform: uppercase;
		font-family: 'Tahoma', cursive;
		text-align: center;
		font-size: 200%;	
		text-shadow:0px 5px 10px rgba(41, 39, 39, 0.76) ;
		font-weight: 1;

	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
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