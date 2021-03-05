<script>
  import { fade } from "svelte/transition";
  import { t } from "../i18n";
</script>

<div
  class="container-fluid d-flex justify-content-center align-items-start"
  id="contact"
>
  <div in:fade={{ duration: 1500}} id="form" class="px-2 py-3 rounded">
    <div class="m-auto mb-3" id="blurb">
      {$t("contact.message")}
    </div>
    <div class="content mt-5">
      <div class="container contact-form" style="text-align: center;">
        <form action="https://formspree.io/f/xwkwyddo" method="POST">
          <div class="form-group">
            <label for="name">
              {$t("contact.form")[0]}:
            </label>
            <input class="form-control" type="text" name="name" />
          </div>
          <div class="form-group">
            <label for="_replyto"> {$t("contact.form")[1]}: </label>

            <input class="form-control" type="text" name="_replyto" />
          </div>
          <div class="form-group">
            <label for="message">
              {$t("contact.form")[2]}:
            </label>

              <textarea
                class="form-control"
                name="message"
                rows="10"
              />
          </div>
          <input
            type="submit"
            class="btn btn-info"
            value={$t("contact.form")[3]}
          />
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
    color: white;
  }
  #form {
    background-color: rgba(5, 127, 195, 0.5);
    max-width: fit-content;
    max-height: fit-content;
  }
</style>
