<template>
  <div class="mt-5">
    <h2 class="text-center"><b>Наши клиенты</b></h2>
    <div class="row w-100">
        <div class="col-sm text-center my-auto mt-md-0 mt-3">
             <img src="../assets/client1.png" />
        </div>
        <div class="col-sm text-center my-auto mt-md-0 mt-3">
             <img src="../assets/client2.jpg" />
        </div>
        <div class="col-sm text-center my-auto mt-md-0 mt-3">
             <img src="../assets/client3.jpg" />
        </div>
        <div class="col-sm text-center my-auto mt-md-0 mt-3">
             <img src="../assets/client5.jpg" />
        </div>
        <div class="col-sm text-center my-auto mt-md-0 mt-3">
             <img src="../assets/client5.png" />
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "OurClients"
};
</script>
<style scoped>
img{
     text-align: center;
     width: 80%;
    pointer-events: none;
}
 .row{
          margin: 0;
     }
@media screen and (max-width: 576px) {
     img{
          width: 50%;
     }
     .col-sm{
          width: 100vw;
          padding: 0;
          text-align: center;
     }
    
}
</style>
