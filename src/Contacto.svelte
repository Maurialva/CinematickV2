<script>
    import Customtextinput from './Customtextinput.svelte';
    import CustomButton from './CustomButton.svelte';
    
    function clickbutton() {
        
    }	
</script>
<center>
<table>
    <tbody>
    <tr>
        <td > 
            <h1>contactarse con nosotros </h1>
            <hr style="color: #449fad; width: 100%;">
        </td>
    </tr>
    <tr rowspan="2">
        <td > 
                <Customtextinput texto="NOMBRE Y APELLIDO" txnom="c_nombre"/>
        </td>
    </tr>
    <tr rowspan="2">
        <td > 
                <Customtextinput texto="EMAIL" txnom="c_email"/>
        </td>
    </tr>
    <tr rowspan="2">
        <td > 
                <Customtextinput texto="ASUNTO DEL MENSAJE" txnom="c_asunto"/>
        </td>
    </tr>
    <tr rowspan="7">
        <td > 
            <h3>
            <textarea  > MENSAJE </textarea>
            </h3>
        </td>
    </tr>
    <tr rowspan="2">
        <td > 
            <CustomButton class="enter" on:click={()=>clickbutton()} >
                ENVIAR MENSAJE
            </CustomButton>
        </td>
    </tr>
    </tbody>
</table>
</center>
<style>
table
{
    text-align: center;
}

textarea 
{ 
    width: 100%; 
   
    color: white;  
    background-color: #449fad; 
    border-radius: 10px; 
}
</style>