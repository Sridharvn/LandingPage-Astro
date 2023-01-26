<template>
  <div class="flex justify-evenly">
    <div
      v-for="item in team"
      :key="item.name"
      class="p-3 flex flex-col items-center justify-center"
    >
      <img v-bind:src="item.profile" alt="" />
      <div>
        {{ item.name }}
      </div>
      <div class="text-[#ef7216]">
        {{ item.position }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      team: [
        {
          name: "Micheal Wagou",
          profile: "./../../public/Micheal-Wagou.png",
          position: "Director",
        },
        {
          name: "Alex Mitchell",
          profile: "./../../public/Alex-Mitchell.png",
          position: "Founder",
        },
        {
          name: "Margaret Anderson",
          profile: "./../../public/Margaret-Anderson.png",
          position: "Manager",
        },
        {
          name: "John Harris",
          profile: "./../../public/John-Harris.png",
          position: "Manager",
        },
      ],
    };
  },
  methods: {
    getImgUrl(pic) {
      //   return require(pic);
    },
  },
};
</script>
