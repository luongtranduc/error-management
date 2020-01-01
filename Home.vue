<template>
  <div>
    <div class="container">
      <div class="notification">
        <!-- Main container -->
        <nav class="level">
          <!-- Left side -->
          <div class="level-left">
            <div class="level-item">
              <div class="field has-addons">
                <p class="control">
                  <input class="input" type="text" placeholder="Find a post" />
                </p>
                <p class="control">
                  <button class="button">Search</button>
                </p>
              </div>
            </div>
          </div>

          <!-- Right side -->
          <div class="level-right">
            <p class="level-item">
              <strong>All</strong>
            </p>
            <p class="level-item">
              <a>Published</a>
            </p>
            <p class="level-item">
              <a>Drafts</a>
            </p>
            <p class="level-item">
              <a>Deleted</a>
            </p>
            <p class="level-item">
              <button class="button is-primary is-outlined" @click="openAdd">
                Register
              </button>
            </p>
          </div>
        </nav>
      </div>
    </div>
    <Add :openmodal='addActive' @closeRequest='close'></Add>
  </div>
</template>
<script>
import Add from "./views/Add";
export default {
  components: {
    Add
  },
  data(){
    return{
      addActive :''
    }
  },
  methods:{
    openAdd(){
      this.addActive ='is-active';
    },
    close(){
      this.addActive='';
    }
  }
};
</script>