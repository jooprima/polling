<template>
  <div class="container">
    <section class="vote">
      <h3 class="give-your-vote">
        Silahkan Berikan Penilaian Anda Terhadap Pelayanan Kami
      </h3>

      <div class="emoticons"><vote :voteProp="vote" /></div>
    </section>

    <section class="finish">
      <transition name="fade"  @after-enter="resetVote">
        <h4 v-if="show">Terima Kasih Telah Memberikan Penilaian Anda</h4>
      </transition>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
// import Vote from "@/components/Vote.vue";
import Vote from "../components/Vote.vue";

export default {
  name: "Home",
  data: function() {
    return {
      show: false,
    };
  },
  components: { Vote },
  methods: {
    vote() {
      this.show = true;
    },
    resetVote(){
      this.show = false;
    }
  },
};
</script>

<style type="text/css">
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.container {
  display: flex;
  flex-wrap: wrap;
  height: 100vh;
  align-items: center;
}

section {
  width: 100%;
}

.give-your-vote {
  font-size: 21px;
}

.emoticons {
  display: flex;
  justify-content: center;
}

.finish {
  position: absolute;
  bottom: 20px;
}
</style>
