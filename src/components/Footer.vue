<template>

  <footer class="footer">
     
 <div>
  <!-- Image and text -->
  <h1>{{title}}</h1>
  <b-footer variant="faded" type="light">
    <b-footer-brand href="#">
      <!-- <img src="" class="d-inline-block align-top" alt=""> -->
      Vue
    </b-footer-brand>
  </b-footer>
</div>

 </footer>
     

</template>
 
 <script>
export default {
 name: 'Footer',
 props:{
     title:String
 }
};
</script>

 <style>
.footer {
  background-color: #c580cf;
  border: 1px solid #fa0425;
  padding: 8px;
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100px;
}
</style>