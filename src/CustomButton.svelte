

<button on:click>
	{nombre}
</button>
<script>
	let sizewidth;
	export let nombre;
	
	switch(nombre)
	{
		case "LOGIN": sizewidth='20%' ;break;
		case "SUSCRIBIRSE": sizewidth='30%';break;
	}
	</script>

<style>
	button {
		height: auto;
		width: 10% ;
		background-color: rgb(90, 29, 29);
		border-color: #693030;
		background-position: 100%;
		background-size: 400%;
		transition: background 900ms ease-in-out;
		text-align: center;
		color: rgb(0, 0, 0); 
		font-size: 150%; 
		padding: 1%; 
		border-radius: 50px; 
		background-image: linear-gradient(45deg,rgb(65, 9, 9) 0%, rgb(158, 80, 80) 56%, rgb(54, 12, 12) 100%); 
		vertical-align:top ;
		border: 10% solid rgb(47, 6, 6); 
		display: inline-block;
		cursor: pointer;
	}
	button:hover {
		background-position: 0;
		color: rgb(87, 12, 12);
		background-image: linear-gradient(43deg,rgb(0, 0, 0) 0%, rgb(37, 26, 26) 56%, rgb(39, 4, 4) 100%); 
		color: rgb(255, 255, 255); 
	}
</style>