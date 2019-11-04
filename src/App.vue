<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <h1>Built In directives</h1>
        <p v-text="'This is some text'"></p>
        <p v-html="'<i>This is dnyanda Kharade</i>'"></p>
      </div>
    </div>
    <hr>
    <div class="row">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <h1>Custom  directives</h1>
        <p v-highlight:background.delayed="'red'">This is some text</p>
        <p v-local-highlight:background.delayed="'green'">This is some text Local Directive</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  directives:{
    'local-highlight':{
        bind(el, binding, vnode) {

      let delay = 0;
      if(binding.modifiers['delayed']){
        delay = 3000;
      }
      setTimeout(()=>{
        if (binding.arg == 'background') {
          el.style.backgroundColor = binding.value;
        } else {
          el.style.color = binding.value;

        }
      },delay);

    }
    }
  }
}
</script>

<style>

</style>
