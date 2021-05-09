<script>

import CustomButton from './CustomButton.svelte';
import Socialicon from './Socialicon.svelte';
import Searchconteiner from './Searchconteiner.svelte';

function clickbutton() {
	
}	
</script>



<table>
    <tbody>
    <tr>
    <td> <img  src='logocinematickv2.png' alt="logo" class="logo"  width="70%"  ></td>
    
    <td> <div align="right"><Socialicon nombre={"Instagram"}/> 
        <Socialicon nombre={"Facebook"}/> 
        <Socialicon nombre={"Twitter"}/> 
        <CustomButton class="login" on:click={()=>clickbutton()} >
            LOGIN
        </CustomButton>
         </div>
         <h1>el mejor cine a un click de distancia &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            &nbsp;&nbsp;&nbsp;
            &nbsp;&nbsp;&nbsp;&nbsp;
            &nbsp;&nbsp;
         </h1> </td>
    </tr>
    <tr>
        <td colspan="2">
            <div class="search-container">
        
            <Searchconteiner/>
        </div>
        </td>
    </tr>
    </tbody>
    </table>

<style>
.search-container
	{
		text-align: center;
		width: 100%;
		background-image:  linear-gradient(180deg,rgb(9, 31, 65) 0%, rgb(80, 146, 158) 56%, rgb(56, 213, 224) 100%);
		border-radius: 50px;
		
	}
</style>