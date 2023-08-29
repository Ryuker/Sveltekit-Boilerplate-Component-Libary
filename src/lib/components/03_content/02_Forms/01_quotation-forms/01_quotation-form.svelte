<script>
  /* Quotation Form 
    - fields: firstname, surname, email, country (select), tel, radio select, submit button
    - icon inside submit button

    author: Joeri van Ees - created: 10/08/2022
  */ 
</script>


<div class="container-fluid quotation-form">
  <form>
    <div class="input-fields">
      <input type="text" id="fname" name="fname" placeholder="Your first name..">
      <input type="text" id="fname" name="sname" placeholder="Your surname..">
      <input type="email" id="email" name="email" placeholder="info@example.com">
      <select id="country" name="country">
        <option value="" disabled selected>Select your country..</option>
        <option value="netherlands">Netherlands</option>
        <option value="belgium">Belgium</option>
        <option value="germany">Germany</option>
      </select>
      <input type="number" id="tel-number" name="tel-number" placeholder="Your telephone number..">
    </div>
    <div class="color-radio-select">
      <span>spray color:</span>
      <input type="radio" id= "radioRed" name="radioColor" value="red" checked>
      <label class="rover-col--red" for="radioRed"></label>
      <input type="radio" id= "radioPink" name="radioColor" value="pink">
      <label class="rover-col--pink" for="radioPink"></label>
      <input type="radio" id= "radioBlack" name="radioColor" value="black">
      <label class="rover-col--black" for="radioBlack"></label>
      <input type="radio" id= "radioBlue" name="radioColor" value="blue">
      <label class="rover-col--blue" for="radioBlue"></label>
      <input type="radio" id= "radioGreen" name="radioColor" value="green">
      <label class="rover-col--green" for="radioGreen"></label>
      <input type="radio" id= "radioYellow" name="radioColor" value="yellow">
      <label class="rover-col--yellow" for="radioYellow"></label>
    </div>
    <input type="submit" value="Submit" />
  </form>
</div>


<style lang="scss" global>

.quotation-form {
  padding: 200px 40px;
  width: 100%;
  display: flex;
  justify-content: center;
}

form {
  padding: 0 50px 0 0;
  margin: 0;

  .input-fields {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;

    input, select {
      display: block;
      padding: 0 12px;
      margin: 10px 0px;
      width: calc(50% - 10px);
      height: 48px;
      box-sizing: border-box;
      font-size: 1rem;
      border: 1px solid $white;
      outline: 1px solid $white;
      @include media-breakpoint-down(md) {
        width: 100%;
      }
      &:focus {
        border: 1px solid $primary;
        outline: 1px solid $primary;
      }
    }
  }

  button.button {
    float:right;
    margin: 20px 0;
  }

  textarea {
    padding: 10px 10px;
    margin: 10px 0;
    width: 100%;
    min-height: 200px;
    box-sizing: border-box;
    font-size: 1rem;
    border: 0;
    outline: 0;
    resize: vertical; /* Allow the user to vertically resize the textarea (not horizontally) */
   
    &:focus {
      border: 1px solid $primary;
      outline: 1px solid $primary;
    }
  }

  // input[type="text"], input[type="tel"], input[type="tel"] {
  //   padding: 10px 10px;
  //   margin: 10px 10px;
  //   width: 70%;
  //   display: block;
  //   border: none;
  //   box-sizing: border-box;

  //   font-size: 1.0rem;

  //   &:focus {
  //     border: 1px solid $primary;
  //     outline: 1px solid $primary;
  //   }
  // }

  input[type=checkbox] {
    height: 50px;
    width: 50px;
    padding: 0;
  }

  .color-radio-select {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    margin: 10px 0;
    h3 {
      display: block;
    }
    .color {
      display: flex;
      flex-direction: column;
      text-align: center;
      span {
        display: block;
        margin: 10px 0;
        font-weight: 700;
        font-size: 0.9rem;
        line-height: 1;
        text-transform: uppercase;
      }
    }

    // span {
    //   font-size: 1.2rem;

    //   @include media-breakpoint-down(md) {
    //     width: 100%;
    //     display: block;
    //   }
    // }

    input[type=radio] {
      opacity: 0;
      position: fixed;
      width: 0;
      display: inline-block;

      &:nth-child(0) {
        margin-left: 0;
      }
    }

    label {
      display: inline-block;
      width: 100px;
      height: 100px;
      background-color: #ddd;
      margin: 0;
      margin: 0 10px; 
      font-family: sans-serif, Arial;
      font-size: 16px;

      &:hover {
        outline-offset: 3px;
      }
    }

    input[type=radio]:focus + label {
      outline-offset: 3px;
    }

    input[type=radio]:checked + label {
      outline-offset: 3px;
    }

    .rover-col {
      $outline-props: 4px solid;

      &--red {
        $red: rgb(255, 0, 0);
        background: $red;
        outline: $outline-props $red;

        &:hover {
          outline: $outline-props $red;
        }
      }

      &--blue {
        $blue-col: rgb(24, 106, 247);
        background: $blue-col;
        outline: $outline-props $blue-col;

        &:hover {
          outline: $outline-props $blue-col;
        }
      }

      &--pink {
        $pink: rgb(255, 0, 170);
        background: $pink;
        outline: $outline-props $pink;

        &:hover {
          outline: $outline-props $pink;
        }
      }

      &--black {
        $black-col: rgb(0, 0, 0);
        background: $black-col;
        outline: $outline-props $black-col;

        &:hover {
          outline: $outline-props $black-col;
        }
      }

      &--green {
        $green: rgb(57, 157, 0);
        background: $green;
        outline: $outline-props $green;

        &:hover {
          outline: $outline-props $green;
        }
      }

      &--yellow {
        $yellow: rgb(255, 247, 0);
        background: $yellow;
        outline: $outline-props rgb(205, 205, 205);
        outline-offset: 0;
        border: 1px solid rgb(205, 205, 205);

        &:hover {
          outline: $outline-props rgb(195, 195, 195);
          outline-offset: 3px;
        }
      }
    }
  }
}



</style>