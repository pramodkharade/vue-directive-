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
        <p v-highlight>This is some text</p>

      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
