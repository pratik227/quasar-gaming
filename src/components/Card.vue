<template>
  <span>
    <q-intersection
      once
      transition="scale"
    >
    <q-card
      :class="$q.screen.lt.sm?'rounded-borders full-height text-white col-lg-6 col-md-6 col-xs-12 col-sm-12':'rounded-borders text-white col-lg-12 col-md-12 col-xs-12 col-sm-12'"
      style="background-color: #181728">
      <q-card-section class="text-center">
        <q-avatar size="100px" class="shadow-10">
          <img src="https://cdn.quasar.dev/img/boy-avatar.png">
        </q-avatar>
      </q-card-section>

      <q-card-section class="q-pt-none  ">
        <div class="text-h6 text-center ">
          Pratik Patel
        </div>
        <div :class="!$q.screen.lt.sm?'text-caption q-mt-md text-justify q-px-xl':'text-caption q-mt-md text-justify'">
          {{text}}
        </div>
      </q-card-section>
    </q-card>
    </q-intersection>
  </span>
</template>

<script>
    export default {
        name: "Card",
        data() {
            return {
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
            }
        }
    }
</script>

<style scoped>

</style>
