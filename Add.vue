<template>
  <div class="modal" :class="openmodal">
    <div class="modal-background"></div>
    <div class="modal-card">
      <header class="modal-card-head">
        <p class="modal-card-title">Register System</p>
        <button class="delete" aria-label="close" @click="close"></button>
      </header>
      <section class="modal-card-body">
        <div class="field">
          <label class="label">Name</label>
          <div class="control">
            <input class="input" type="text" placeholder="Text input" />
          </div>
        </div>

        <div class="field">
          <label class="label">HTTP Code</label>
          <div class="control is-expanded">
            <div class="select is-fullwidth">
              <select name='httpcode'>
                <option>500</option>
                <option>400</option>
                <option>200</option>
              </select>
            </div>
          </div>
        </div>
      </section>
      <footer class="modal-card-foot">
        <button class="button is-success">Register</button>
        <button class="button" @click="close">Cancel</button>
      </footer>
    </div>
  </div>
</template>


<script>
export default {
  props: ["openmodal"],
  methods: {
    close() {
      this.$emit("closeRequest");
    }
  }
};
</script>