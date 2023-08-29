<script>
  /* Bootstrap Footer 01 - 4 columns responsive
  - 4 columns
  - - desktop: 4 col , tablet: 2 col, mobile: 1 col
  - copyright bar

  author: Joeri van Ees 
  */
</script>

<!-- copyable component code goes here -->
<footer class="foot">
  <div class="container">
    <!-- 4 columns,  -->
    <div class="row g-0">
      <div class="col-xs-12 col-md-6 col-lg-3">
        <h3>Heading 1</h3>
        <ul>
          <li><a href="/comp-sandbox">Link #1</a></li>
          <li><a href="/comp-sandbox">Link #2</a></li>
          <li><a href="/comp-sandbox">Link #3</a></li>
          <li><a href="/comp-sandbox">Link #4</a></li>
          <li><a href="/comp-sandbox">Link #5</a></li>
        </ul>
      </div>
      <div class="col-xs-12 col-md-6 col-lg-3">
        <h3>Heading 2</h3>
        <ul>
          <li><a href="/comp-sandbox">Link #1</a></li>
          <li><a href="/comp-sandbox">Link #2</a></li>
          <li><a href="/comp-sandbox">Link #3</a></li>
          <li><a href="/comp-sandbox">Link #4</a></li>
          <li><a href="/comp-sandbox">Link #5</a></li>
        </ul>
      </div>
      <div class="col-xs-12 col-md-6 col-lg-3">
        <h3>Heading 3</h3>
        <ul>
          <li><a href="/comp-sandbox">Link #1</a></li>
          <li><a href="/comp-sandbox">Link #2</a></li>
          <li><a href="/comp-sandbox">Link #3</a></li>
          <li><a href="/comp-sandbox">Link #4</a></li>
          <li><a href="/comp-sandbox">Link #5</a></li>
        </ul>
      </div>
      <div class="col-xs-12 col-md-6 col-lg-3">
        <h3>Heading 4</h3>
        <ul>
          <li><a href="/comp-sandbox">Link #1</a></li>
          <li><a href="/comp-sandbox">Link #2</a></li>
          <li><a href="/comp-sandbox">Link #3</a></li>
          <li><a href="/comp-sandbox">Link #4</a></li>
          <li><a href="/comp-sandbox">Link #5</a></li>
        </ul>
      </div>
    </div>

    <div class="copyright-bar">
      <div class="cb__left">
        <span class="copyright">2022 © company name </span>
        <a href="/comp-sandbox">privacy policy</a>
        <div class="social-icons">
          <a href="/comp-sandbox">
            <i class="social-icon">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="6102 6055 24 24"><path data-name="Path 1192" d="M6102 6055v24h24v-24zm8 19h-3v-11h3zm-1.5-12.3a1.8 1.8 0 1 1 1.8-1.7 1.8 1.8 0 0 1-1.8 1.7zm13.5 12.3h-3v-5.6c0-3.4-4-3.1-4 0v5.6h-3v-11h3v1.8c1.4-2.6 7-2.8 7 2.4z" fill="#fff"></path></svg>
            </i>
          </a>
          <a href="/comp-sandbox">
            <i class="social-icon">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="6134 6055 24 24"><path data-name="Path 1191" d="M6134 6055v24h24v-24zm18.9 9.2a9.3 9.3 0 0 1-14.4 8.3 6.6 6.6 0 0 0 4.9-1.4 3.3 3.3 0 0 1-3-2.2 3.3 3.3 0 0 0 1.4 0 3.3 3.3 0 0 1-2.6-3.3 3.3 3.3 0 0 0 1.5.4 3.3 3.3 0 0 1-1-4.4 9.3 9.3 0 0 0 6.7 3.4 3.3 3.3 0 0 1 5.6-3 6.6 6.6 0 0 0 2-.8 3.3 3.3 0 0 1-1.4 1.8 6.6 6.6 0 0 0 2-.5 6.7 6.7 0 0 1-1.7 1.7z" fill="#fff"></path></svg>
            </i>
          </a>
          <a href="/comp-sandbox">
            <i class="social-icon">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="6166 6055 24 24"><path data-name="Path 1190" d="M6166 6055v24h24v-24zm16 7h-2c-.5 0-1 .2-1 .9v1h3l-.2 3h-2.8v8h-3v-8h-2v-3h2v-1.8c0-2 1-3.1 3.5-3.1h2.5z" fill="#fff"></path></svg>
            </i> 
          </a>
        </div> 
      </div>
      <div class="cb__right">
        <a class="dev-credit" href="https://suprevo.com/">Developed by Suprevo</a>
      </div>
    </div>
  </div>
</footer>


<style lang="scss">

  .foot {
    background-color: aqua;
    padding: 0;
    margin: 0;
    justify-content: center;

    .container {
      padding: 0 20px;
      margin: 0;
      background-color: rgb(94, 94, 210);
      padding-bottom: 20px;
    
      h3 {
        text-transform: uppercase;
        background-color: rgb(152, 152, 210);
      }

      ul {
        background-color: red;
        padding: 0;
        margin: 0 ;
        
        list-style: none;
        
        li {
          text-align: left;
          text-decoration: none;

          a {
            text-decoration: none;
            padding: 6px 0px;
            display: block;
          }
        }
      }

      .copyright-bar {
        margin-top: 30px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        min-height: 100px;
        flex-wrap: wrap;
        
        .cb__left {
          display: flex;
          align-items: center;

          .copyright {
            display: flex;
            padding-right: 40px;
            align-items: center;
            margin-right: 20px;
            flex-wrap: wrap;
            border-right: 1px solid black;
          }

          a {
            // padding-right: 20px;
            text-decoration: none;
          }

          .social-icons{
            padding-left: 20px;
          }

          .social-icon {
            padding: 10px 2px;
            justify-content: center;
            display: inline-block;

            svg {
              display: flex;
              flex-direction: row;
              align-items: center;
              width: 30px;

              path {
                fill: rgb(0, 0, 0);
              }
            }

            &:hover {
              svg path {
                fill: rgb(157, 156, 156);
              }
            }
          }
        }
        

        .cb__right {
          a {
            display: flex;
            justify-content: start;
            text-decoration: none;
          }

          .dev-credit {
            display: flex;
            align-items:flex-end;
          }

          a {
            text-decoration: none;
          }
        }

        
        // start when screen width = < 768px
        @include media-breakpoint-down(md) {
          flex-wrap: wrap;
          display: block;
          justify-content:space-evenly;

          .cb__left{
            flex-wrap: wrap;
            justify-content: center;
          }

          .cb__right {
            display: flex;
            justify-content: center;
          }

          .copyright {
            justify-content: center;
            align-items: center;
          }

          .social-icons {
            padding: 20px 0;
          }
          .dev-credit {
            padding: 0;
          }
        }

        @include media-breakpoint-down(sm)
        {
          .cb__left {
            .copyright {
            padding-right: 30px
            }

            a {
              padding: 0;
            }
          }
          
        }
      }
    }
  }
</style>