

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
		background-color: rgb(29, 81, 90);
		border-color: #305769;
		background-position: 100%;
		background-size: 400%;
		transition: background 900ms ease-in-out;
		text-align: center;
		color: rgb(204, 240, 238); 
		font-size: 150%; 
		padding: 1%; 
		border-radius: 50px; 
		background-image: linear-gradient(45deg,rgb(9, 31, 65) 0%, rgb(80, 146, 158) 56%, rgb(56, 213, 224) 100%); 
		vertical-align:top ;
		border: 10% solid rgb(6, 42, 47); 
		display: inline-block;
		cursor: pointer;
	}
	button:hover {
		background-position: 0;
		color: rgb(13, 12, 87);
		background-image: linear-gradient(83deg,rgb(96, 47, 100) 0%, rgb(28, 166, 221) 25%, rgb(86, 152, 163) 100%); 
		color: rgb(255, 255, 255); 
	}
</style>