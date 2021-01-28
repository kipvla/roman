<script>
  import {fly} from 'svelte/transition'
  import {t} from '../i18n'
</script>

<div class="container-fluid d-flex justify-content-center align-items-start" id="contact">
  <div in:fly={{duration: 2000, x: 200}} id="form" class="px-2 py-3 rounded">
    <div class="m-auto mb-3" id="blurb">
      {$t('contact.message')}
    </div>
    <div class="content mt-5">
      <div class="container contact-form" style="text-align: center;">
        <form action="https://formspree.io/f/xpzolpwz" method="POST">
          <div class="form-group">
            <label>
              {$t('contact.form')[0]}:
              <input class="form-control" type="text" name="name" />
            </label>
          </div>
          <div class="form-group">
            <label>
              {$t('contact.form')[1]}:
              <input class="form-control" type="text" name="_replyto" />
            </label>
          </div>
          <div class="form-group">
            <label>
              {$t('contact.form')[2]}:
              <textarea class="form-control" name="message" rows="10" col="10"/>
            </label>
          </div>
          <input type="submit" class="btn btn-info" value={$t('contact.form')[3]} />
        </form>
      </div>
    </div>
  </div>
  
</div>

<style>
  /* #blurb {

  } */
  #contact {
    padding-top: 5rem;
    background-image: url("/images/bigbend2.jpeg");
    background-size: cover;
    /* background-position: 48% center; */
    height: 800px;
    text-align: center;
    font-weight: 500;
    color: white;
  }
  #form {
    background-color: rgba(100,100,100, 0.8);
    max-width: fit-content;
    max-height: fit-content;
  }
</style>
