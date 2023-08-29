<script>
  /* Basic Contact Form - 
    - fields: name, email, tel, input message, send button

    author: Joeri van Ees 
  */ 

</script>

<h3>Basic Contact Form </h3>



<div class="cf_container">
  <h2>Get In Touch</h2>
  <form>
    <input type="text" id="name" name="name" placeholder="Your name..">
    <input type="email" id="email" name="email" placeholder="info@example.com">
    <input type="number" id="tel-number" name="email" placeholder="Your telephone number..">
    <textarea id="message" name="message" placeholder="Type your message here.."></textarea>
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
    display: block;
    width: 100%;
    // background: purple;
    padding: 0;
    margin: 0;

    display: flex;
    flex-direction: column;

    input {
      padding: 10px 10px;
      margin: 10px 0;
      width: 100%;
      background: rgb(151, 151, 233);
      display: block;
      border: none;
      box-sizing: border-box;

      font-size: 1.0rem;
    }

    input:nth-child(1) {
      margin-top: 0;

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
    }

    input[type=submit] {
      background: rgb(44, 44, 73);
      color: white;
    }

    input[type=submit]:hover {
      background: rgb(85, 85, 139);
    }
  }

}

</style>