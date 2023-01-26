<template>
  <div class="text-center flex flex-col items-center">
    <div class="text-[#ef7216] p-3 text-2xl">OUR SERVICES</div>
    <div class="text-4xl w-1/2 p-2">
      We are a India based top Equipments & Engineering company
    </div>
    <div class="flex justify-evenly items-center">
      <div
        v-for="item in services"
        :key="item.name"
        class="flex flex-col justify-center items-center"
      >
        <img v-bind:src="item.image" alt="" class="p-2" />
        <div class="border text-start p-3 w-1/2">
          <img v-bind:src="item.mdi" alt="" class="h-8 w-8 m-3" />
          <div class="p-4 text-2xl">{{ item.name }}</div>
          <div class="p-4 text-xl">{{ item.description }}</div>
          <div class="p-4 text-xl">Read More &#8594;</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      services: [
        {
          name: "Manufacturing",
          image: "./../../public/manufacturing.png",
          mdi: "./../../public/manufacturing-mdi.png",
          description:
            "Corem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt",
        },
        {
          name: "Sales",
          image: "./../../public/sales.png",
          mdi: "./../../public/sales-mdi.png",
          description:
            "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque",
        },
        {
          name: "Rental",
          image: "./../../public/rental.png",
          mdi: "./../../public/rental-mdi.png",
          description:
            "Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores",
        },
      ],
    };
  },
};
</script>
