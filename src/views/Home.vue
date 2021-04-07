<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <calender
      curDateClassName="calenderBg"
      :readOnly="true"
      :disabledDates="disabledDates"
    ></calender>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import calender from "@/components/calender/calender.vue";

export default {
  name: "Home",
  data() {
    let date = new Date();
    return {
      disabledDates: [
        new Date(date.getFullYear(), date.getMonth(), 5),
        new Date(date.getFullYear(), date.getMonth(), 15),
        new Date(date.getFullYear(), date.getMonth(), 20),
      ],
    };
  },
  components: {
    HelloWorld,
    calender,
  },
  methods: {},
};
</script>
<style>
.vue-mobile-calendar
  .dates-list
  .dates-contanier
  .dates-row
  .date-item.calenderBg
  .date {
  background-color: #fff !important;
}
.vue-mobile-calendar
  .dates-list
  .dates-contanier
  .dates-row
  .date-item.calenderBg
  .date {
  color: #323538 !important;
}
.vue-mobile-calendar
  .dates-list
  .dates-contanier
  .dates-row
  .date-item.disabledDate {
  background-color: rgb(66, 113, 240) !important;
  /* background-image: url("./assets/slide_down.png") !important; */
  background-size: cover !important;
  background-repeat: no-repeat !important;
}
</style>
