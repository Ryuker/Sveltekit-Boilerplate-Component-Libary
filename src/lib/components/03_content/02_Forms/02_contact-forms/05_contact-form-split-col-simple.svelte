<script>
	/* Contact Form Split Col Simple
    - fields: name, email, tel, subject,input message, send button (with icon)
    - contact info with socials

    - using bootstrap 5.0

    author: Joeri van Ees - created: 10-02-2022
  */
</script>

<section class="container contact-form">
  <div class="container__header">
    <h1>Contact</h1>
  </div>
  <div class="row">

    <!-- Contact Form -->
    <div class="col-12 col-lg-8">
      <form>
        <div class="input-fields">
          <input type="text" id="name" name="name" placeholder="Uw naam">
          <input type="email" id="email" name="email" placeholder="Uw e-mailadres">
          <input type="tel" id="tel-number" name="tel-number" placeholder="Uw telefoonnummer"/>
          <input type="text" id="subject" name="subject" placeholder="Onderwerp">
          <textarea type="text" id="message" name="message" placeholder="Uw bericht"></textarea>
        </div>
        <button type="submit" class="button button--icon">Verzenden <i class="fas fa-paper-plane"></i></button>
      </form>
    </div>

    <!-- Contact Info -->
    <div class="col-12 col-lg-4">
      <h3>Contactgegevens</h3>
      <ul>
        <li>
          <strong>E</strong>
          <a href="mailto:info@vanstooten.nl">info@vanstooten.nl</a>
        </li>
        <li>
          <strong>T</strong>
          <a href="tel:+31(0)10 123 456 89">+31(0)10 123 456 89</a>
        </li>
        <li class="social-icons">
          <a href="/comp-builder"><i class="fa-brands fa-instagram"></i></a>
          <a href="/comp-builder"><i class="fa-brands fa-facebook"></i>
          <a href="/comp-builder"><i class="fa-brands fa-youtube"></i></a>
        </li>
      </ul>
    </div>
  </div>
</section>



<style lang="scss" global>
	.contact-form {
		padding-bottom: 50px;
		ul {
			li {
				font-size: 0.95rem;
				margin-bottom: 5px;
				strong {
					color: $black;
					display: inline-block;
					width: 24px;
				}
				a {
					color: $black;
				}
				&.social-icons {
					display: flex;
					margin-top: 10px;
					margin-left: -10px;
					a {
						display: flex;
						height: 48px;
						width: 48px;
						justify-content: center;
						align-items: center;
						font-size: 1.7rem;
						color: $blue;
					}
				}
			}
		}
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

  input[type=checkbox] {
    height: 50px;
    width: 50px;
    padding: 0;
  }
}
</style>
