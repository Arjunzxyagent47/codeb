<script>
  import Footer from "../components/Footer.svelte";
  import { goto } from '@sapper/app';

  function handlelogin() {
     jQuery('.ui.basic.modal.2').modal('show');
	}
  function handlesignup() {
     jQuery('.ui.basic.modal.1').modal('show');
	}

</script>


<div class="ui fixed hidden menu" style="background-color: #282a36;">
  <div class= "item">
    <a href = "."><h1>
    <i class=" fitted notched circle loading icon"></i>
    BetterReads
    </h1> </a>
  </div>
  <div class="right menu">
    <div class="item">
      <button on:click={handlesignup} class=" fitted ui inverted button">Sign Up</button>
    </div>
    <div class="item">
      <button on:click={handlelogin} class="fitted ui button" style="background-color: #50fa7b;">Log In</button>
    </div>
</div>
</div>

<!-- Modal for Signup-->
<div class="ui basic modal 1">
  <form class="ui form" style = "width: 400px;">
    <div class="field">
      <p >Email address </p>
      <input type="text" name="email" placeholder="email">
    </div>
    <div class="field">
      <p>Password</p>
      <input type="password" name="password" placeholder="password">
    </div>
        <p> By submitting, I agree to the Terms and Conditions</p>
    
    <button class="fitted ui inverted button" type="submit" on:click={() => goto('./home')} >Submit</button>
  </form>
</div>

<!-- Modal for login-->
<div class="ui basic modal 2">
  <form class="ui form" style = "width: 400px;">
    <div class="field">
      <p style="color: #00FF00">Email address</p>
      <input type="text" name="email" placeholder="email">
    </div>
    <div class="field">
      <p style="color: #00FF00">Password</p>
      <input type="password" name="password" placeholder="password">
    </div>
    <button class="fitted ui inverted green button" type="submit" on:click={() => goto('./home')}>Login</button>
  </form>
</div>




<div class="ui grid">
  <div class="four wide row"> A</div>
</div>

<div class="ui text container" style="min-height: 600px ;">
  <h1 class="ui inverted header" style = "margin-top: 0.5em; font-size: 8em;">
    Site under construction
  </h1>
  <h2 class = "ui inverted header " style = "margin-top: 2.5em;">Fetching wood ...</h2>
</div>

<Footer/>


