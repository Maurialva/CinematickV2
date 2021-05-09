
<script>
export let pagenumber;
let ti;
switch(pagenumber)
	{
	case "1": ti="CinemaTick - inicio";break;
	case "2": ti="CinemaTick - Login";break;
	case "3": ti="CinemaTick - Registro";break;
	case "4": ti="CinemaTick - Sobre nosotros";break;
	case "5": ti="CinemaTick - Contactarse";break;
	case "6": ti="CinemaTick - Ayuda";break;
	case "7": ti="CinemaTick - Busqueda";break;
	case "8": ti="CinemaTick - Pelicula";break;
	case "9": ti="CinemaTick - Seleccion de Butacas";break;
	case "10": ti="CinemaTick - Datos de compra";break;
	case "11": ti="CinemaTick - Error";break;
	}

</script>



{#if pagenumber=="1"}
    
    <style>
    
    .menuhead { grid-area: header; }
    .menuleft { grid-area: menu; }
    .menucenter { grid-area: main; }
    .menuright { grid-area: right; }
    .menufoot { grid-area: footer; }
    
    .grid-container {
      display: grid;
      grid-template-areas:
        'header header header header header header'
        'main main main main right right'
        'footer footer footer footer footer footer';
      grid-gap: 1%;
      background-color:#449fad;
      padding: 1%;
      border-radius: 50px; 
    }
    
    .grid-container > div {
      background-color:lightgray;
      text-align: center;
      padding: 1%;
      border-radius: 50px; 
      border-color: aqua;
      
      
    }
    </style>

{:else if pagenumber=="7"}

<style>
    
    .menuhead { grid-area: header; }
    .menuleft { grid-area: menu; }
    .menucenter { grid-area: main; }
    .menuright { grid-area: right; }
    .menufoot { grid-area: footer; }
    
    .grid-container {
      display: grid;
      grid-template-areas:
        'header header header header header header'
        'menu menu main main main main'
        'footer footer footer footer footer footer';
        grid-gap: 1%;
      background-color:linear-gradient(45deg,rgb(9, 31, 65) 0%, rgb(80, 146, 158) 56%, rgb(56, 213, 224) 100%);
      padding: 1%;
      border-radius: 50px; 
    }
    
    .grid-container > div {
      background-color:lightgray;
      text-align: center;
      padding: 1%;
      border-radius: 50px; 
      border-color: aqua;
      
      
    }
    </style>
{:else }

<style>
    
    .menuhead { grid-area: header; }
    .menuleft { grid-area: menu; }
    .menucenter { grid-area: main; }
    .menuright { grid-area: right; }
    .menufoot { grid-area: footer; }
    
    .grid-container {
      display: grid;
      grid-template-areas:
        'header header header header header header'
        'main main main main main main'
        'footer footer footer footer footer footer';
        grid-gap: 1%;
      background-color:linear-gradient(45deg,rgb(9, 31, 65) 0%, rgb(80, 146, 158) 56%, rgb(56, 213, 224) 100%);
      padding: 1%;
      border-radius: 50px; 
    }
    
    .grid-container > div {
      background-color:lightgray;
      text-align: center;
      padding: 1%;
      border-radius: 50px; 
      border-color: aqua;
      
      
    
    }
    </style>
{/if}

<svelte:head>
	<title>{ti}</title>
</svelte:head>
