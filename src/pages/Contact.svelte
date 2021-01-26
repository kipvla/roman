<script>
  import {t} from '../i18n'
</script>

<div class="container-fluid" id="contact">
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
            <textarea class="form-control" name="message" />
          </label>
        </div>
        <input type="submit" class="btn btn-info" value={$t('contact.form')[3]} />
      </form>
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
    color: black;
    text-shadow: 1px 1px 1px white;
    font-weight: 500;
  }
</style>
