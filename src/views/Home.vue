<template>
  <div class="container">
    <section class="vote">
      <h3 class="give-your-vote">
        Silahkan Berikan Penilaian Anda Terhadap Pelayanan Kami
      </h3>

      <div class="emoticon">
        <!-- Ini akan menjadi component vote -->
      </div>
    </section>

    <section class="finish">
      <h4>Terima Kasih Telah Memberikan Penilaian Anda</h4>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: { }
};
</script>

<style type="text/css">
  .container{
    display: flex;
    flex-wrap: wrap;
    height: 100vh;
    align-items: center;
  }

  section{
    width: 100%;
  }
</style>
