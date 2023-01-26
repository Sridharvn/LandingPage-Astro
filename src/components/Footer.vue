<template>
  <div class="bg-[#180300] text-white">
    <div class="py-5 flex justify-around">
      <div v-for="item in contacts" :key="item.name">
        <div class="flex items-center">
          <img :src="item.icon" alt="" />
          <div class="flex flex-col">
            <div class="p-1 pl-3">{{ item.name }}</div>
            <div class="p-1 pl-3">{{ item.details }}</div>
          </div>
        </div>
      </div>
    </div>
    <hr class="h-px my-8 bg-[#ef7216] border-0 mx-20" />
    <div class="flex justify-evenly">
      <div class="flex flex-col p-5 w-1/5">
        <img src="./../../public/Logo.png" alt="" class="w-[250px]" />
        <div class="text-2xl font-bold p-2">NB Equipments and Engineering</div>
        <div class="font-light p-2">
          Lorem ipsum dolor sit amet consectetur adipiscing elit, sed do eiusmod tempor
          incididunt ut labore et dolore magna aliqua.
        </div>
      </div>
      <div class="flex flex-col w-1/5 text-3xl" v-for="item in footers" :key="item.name">
        {{ item.name }}
        <hr class="h-px my-8 bg-[#ef7216] border-0 mr-56" />
        <div v-for="list in item.items" :key="list" class="text-xl">
          {{ list }}
        </div>
      </div>
    </div>
    <hr class="h-px my-8 bg-[#ef7216] border-0 mx-20" />
    <div class="pb-7 text-center flex justify-center text-gray-50">
      &#169; Copyright 2015 - 2019.
      <div class="text-white font-bold pl-1">NB Equipments & Engineering Pvt- Ltd.</div>
      All rights resevered- Designed by
      <div class="text-white font-bold pl-1">Ideamagix.</div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      contacts: [
        {
          name: "Phone",
          icon: "./../../public/Phone.png",
          details: "+91 703-900-0027",
        },
        {
          name: "Address",
          icon: "./../../public//Address.png",
          details: "317 Arcadia, Hiranandani Estate Thane (W), India.",
        },
        {
          name: "E-Mail",
          icon: "./../../public/email.png",
          details: "info@nbee.in",
        },
      ],
      footers: [
        {
          name: "Quick Links",
          items: ["About Us", "Sales", "Careers", "Contact us", "Download Broucher"],
        },
        {
          name: "Products",
          items: [
            "Crawler Cranes",
            "Vibro Hammers",
            "Hydraulic Knuckle Boom Crane",
            "Motor Grader",
          ],
        },
        {
          name: "Rental",
          items: ["Cranes", "Trailers & Axles", "Boom Lift"],
        },
      ],
    };
  },
};
</script>
