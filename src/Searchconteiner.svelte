<script>
import Searchicon from './Searchicon.svelte';
</script>

<br><br>
					<form action="http://localhost:5000/">
						
					<input type="text" placeholder="BUSCAR..." name="searchbar"  >
					<Searchicon/>
					
					<br>
					<br>
					</form>

    <style>
    
	input[type=text] 
	{
		vertical-align:middle;
		text-align: center;
		transition: background 900ms ease-in-out;
		background-color: rgb(255, 255, 255);
		background-position: 100%;
		background-size: 200%;
		border: rgb(255, 255, 255);
		background-image: linear-gradient(90deg,rgb(255, 255, 255) 0%, rgb(21, 70, 75) 56%, rgb(17, 28, 70) 100%);		
		color: rgb(255, 255, 255); 
		border-radius: 50px; 
		width:80%;
        font-size: 120%;
		}
	
	input:focus {  border-image: #000000; 
	outline: none;
	background-position: 0;
	transition: background 900ms ease-in-out;
	background-image: linear-gradient(43deg,rgb(27, 32, 83) 0%, rgb(33, 214, 199) 56%, rgb(4, 25, 39) 100%); 
	}
	input:hover{
		background-position: 0;
		transition: background 900ms ease-in-out;
		background-image:  linear-gradient(43deg,rgb(27, 32, 83) 0%, rgb(33, 214, 199) 56%, rgb(4, 25, 39) 100%); 
	}
</style>