<script>
	import { slide } from 'svelte/transition';
    import CustomButton from './CustomButton.svelte';
	let visible = true;
	let sections = [
		{
			id: 1,
			title: "¿COMO SE COMPRA EN ESTA PAGINA?",
			content:  "Si el titular de datos personales utiliza los servicios de CinemaTick, en consecuencia presta su consentimiento, conforme a lo establecido en la ley 25.326 de Protección de Datos Personales, a tenor de lo cual declara conocer y aceptar, para que sus datos personales integren la base de datos de CinemaTick, otorgando por la presente autorización expresa para: (i) el tratamiento automatizado de dichos datos e información y (ii) su utilización para servicios actuales o futuros, que desarrolle SA.El titular de los datos personales tiene la facultad de ejercer el derecho de acceso a los mismos en forma gratuitaWelcome to section 2 test content",
			active: false,
		},
		{
			id: 2,
			title: "¿ES SEGURO INGRESAR UNA TARJETA DE CREDITO?",
			content: "Si el titular de datos personales utiliza los servicios de CinemaTick, en consecuencia presta su consentimiento, conforme a lo establecido en la ley 25.326 de Protección de Datos Personales, a tenor de lo cual declara conocer y aceptar, para que sus datos personales integren la base de datos de CinemaTick, otorgando por la presente autorización expresa para: (i) el tratamiento automatizado de dichos datos e información y (ii) su utilización para servicios actuales o futuros, que desarrolle SA.El titular de los datos personales tiene la facultad de ejercer el derecho de acceso a los mismos en forma gratuitaWelcome to section 2 test content",
			active: false,
		},
		{
			id: 3,
			title: "¿COMO CREO UNA CUENTA DE CINEMATICK?",
			content:  "Si el titular de datos personales utiliza los servicios de CinemaTick, en consecuencia presta su consentimiento, conforme a lo establecido en la ley 25.326 de Protección de Datos Personales, a tenor de lo cual declara conocer y aceptar, para que sus datos personales integren la base de datos de CinemaTick, otorgando por la presente autorización expresa para: (i) el tratamiento automatizado de dichos datos e información y (ii) su utilización para servicios actuales o futuros, que desarrolle SA.El titular de los datos personales tiene la facultad de ejercer el derecho de acceso a los mismos en forma gratuitaWelcome to section 2 test content",
			active: false,
		},
        {
			id: 4,
			title: "¿QUE PASA SI NO PUEDO IR AL CINE Y YA PAGUE LA ENTRADA?",
			content:  "Si el titular de datos personales utiliza los servicios de CinemaTick, en consecuencia presta su consentimiento, conforme a lo establecido en la ley 25.326 de Protección de Datos Personales, a tenor de lo cual declara conocer y aceptar, para que sus datos personales integren la base de datos de CinemaTick, otorgando por la presente autorización expresa para: (i) el tratamiento automatizado de dichos datos e información y (ii) su utilización para servicios actuales o futuros, que desarrolle SA.El titular de los datos personales tiene la facultad de ejercer el derecho de acceso a los mismos en forma gratuitaWelcome to section 2 test content",
			active: false,
		}
	]
	
	const expand = (section) => {
		sections = sections.map(s => {
			s.active = false
			if (s.id === section.id) {
				s.active = true
			}
			return s
		})
	}
</script>
<h1>preguntas frecuentes </h1>
<hr style="color: #449fad; width: 100%;">
{#each sections as section}
<div class="accordion">
        <CustomButton class="ayuda" on:click={() => expand(section)} >
            {section.title}
        </CustomButton>
	{#if section.active}
		<div class="slider" transition:slide>
			<h2>
				Respuesta:
			</h2>
            <h3>
			<p><br>{section.content}<br><br><br></p></h3>
		</div>
	{/if}
</div>
{/each}

<style>
	.accordion {
		margin-bottom: 1%;
       
	}
	.slider {
		/* Comment out the border and padding and let the wonkyness begin!
		border: 1px solid #eee;
		padding: 4px 20px;
		*/
		
		/* Added some color to illustrate the issue */
		background-color: #449fad;
		color: white;
        border-radius: 50px;
	}

    h3
    {
        color: white;
    }
</style>

