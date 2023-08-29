<script>
  /* Contact Form with Icon and Captcha  
    - fields: name, email, tel, input message, send button
    - icon next to input fields

    author: Joeri van Ees 
  */ 

</script>

<h3>Contact Form with Icon and Captcha  </h3>



<div class="cf_container">
  <h2>Get In Touch</h2>
  <form>
    <div class="input-fields">
      <input type="text" id="name" name="name" placeholder="Your name..">
      <input type="email" id="email" name="email" placeholder="info@example.com">
      <input type="number" id="tel-number" name="email" placeholder="Your telephone number..">
    </div>
    <div class="icon"><i class="fa-solid fa-atom"></i></div>


    <textarea id="message" name="message" placeholder="Type your message here.."></textarea>

    <input type="checkbox" id="captcha-checkbox">
    <input type="text" id="captcha" name="captcha" placeholder="I'm not a robot..">
    <input type="submit" value="Submit">
  </form>

</div>


<style lang="scss">
.cf_container {
  display: block;
  width: 100%;
  background: rgb(222, 46, 46);
  max-width: 800px;
  min-height: 400px;

  margin-bottom: 30px;

  padding: 10px;
  box-sizing: border-box;

  h2 {
    font-size: 1.2rem;
    text-align: center;
  }

  form {
    width: 100%;
    // background: purple;
    padding: 0;
    margin: 0;

    display: flex;
    flex-direction: row;
    flex-wrap: wrap;

    .input-fields {
      background: rgb(128, 128, 192);
      flex-grow: 4;
      width: 50%;
      display: flex;
      flex-direction: column;
      order: 1;

      input {
        padding: 10px 10px;
        margin: 10px 0;
        width: 100%;
        background: rgb(151, 151, 233);
        display: block;
        border: none;
        box-sizing: border-box;

        font-size: 1.0rem;

        order: 1;
      }

      input:nth-child(1) {
        margin-top: 0;
      }
    }
    

    .icon {
      background: blue;
      width: 50%;
      height: 100%;
      text-align: center;
      order: 2;
      align-self:center;
      flex-grow: 4;
      i {
        font-size: 8.0rem;
      }

      @include media-breakpoint-down(sm) {
        display: none;
      }

    }

    textarea {
      background: rgb(151, 151, 233);
      padding: 10px 10px;
      margin: 10px 0;
      width: 100%;
      min-height: 200px;
      border: none;
      box-sizing: border-box;
      font-size: 1.0rem;
      resize: vertical; /* Allow the user to vertically resize the textarea (not horizontally) */

      font-family: "Arial", Times, serif;
      order: 3;
      flex-shrink: 0;
    }

    input {
      padding: 10px 10px;
      margin: 10px 10px;
      width: 70%;
      background: rgb(151, 151, 233);
      display: block;
      border: none;
      box-sizing: border-box;

      font-size: 1.0rem;

      order: 4;
    }

    input[type=checkbox] {
      background: rgb(151, 151, 233);
      height: 50px;
      width: 50px;
      padding: 0;

      order:4;

    }

    input[type=submit] {
      background: rgb(44, 44, 73);
      height: 50px;
      width: 100px;
      border: none;
      color: white;
      justify-self: flex-end;
      align-self: flex-end;
      order: 4;

      @include media-breakpoint-down(sm) {
        width: 100%;
        
      }
    }

    input[type=submit]:hover {
      background: rgb(85, 85, 139);
      flex-shrink: 0;
      align-self: flex-end;
      order: 4;
    }
  }

}

</style>