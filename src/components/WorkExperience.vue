<template>
  <h1 class="mt-16 mb-8 text-2xl tracking-tighter text-zinc-800 font-bold">
    Work experience
  </h1>

  <div v-for="item in items" :key="item.name" class="relative pb-10 pl-8 border-l-2 border-muted">
    <div class="absolute w-4 h-4 bg-white border-2  rounded-full -left-[9px] top-0"></div>
    <div>
      <div class="flex items-center gap-2 mb-1">
        <h3 class="text-xl font-semibold">{{ item.role }}</h3><span>•</span><a :href="item.link" target="_blank"
          rel="noopener noreferrer" class="flex items-center gap-1 transition-colors">{{ item.name }}
          <Icon icon="ph:arrow-square-up-right-light" />
        </a>
      </div>
      <p class="mb-4 text-sm text-zinc-600">{{ item.period }}</p>
      <p class="mb-2">{{ item.description }}</p>
      <ul class="space-y-2 list-disc list-inside">
        <li v-for="point in item.points" :key="point">{{ point }}</li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { Icon } from '@iconify/vue';
const items = [
  {
    name: "DartsPay Inc",
    link: "https://dartspay.com",
    period: "March 2024 - Present",
    role: "Senior Frontend Developer",
    description: "Building the fastest and most secured cross-border payment platform",
    points: [
      "Proactively leading the frontend engineering effort",
      "Built an internal admin tool for payment monitoring and troubleshooting"
    ]
  },
  {
    name: "Send (YC 2020)",
    link: "https://trysend.com",
    period: "June 2022 - July 2023",
    role: "Senior Frontend Engineer",
    description: "Built a digital freight forwarder and supply chain system",
    points: [
      "Developed easy-to-use customer-facing application for supply chain management from the groundup",
      "Integrated 3rd party freight management APIs for a much better experience",
      "Developed application to manage cargos on behalf of customers"
    ],
  },
  {
    name: "AcademicLabs (GmbH)",
    link: "https://academiclabs.com",
    period: "November 2020 - May 2022",
    role: "Fullstack Software developer (Frontend focused)",
    description: "Built a digital repository and collaboration platform for scientific research",
    points: [
      "Implemented complex pagination and filtering feature for quicker access to relevant content",
      "Enhance overall mobile browsing experience",
      "Reduced data entry time by developing efficient python-based web scrapers to collect publicly available information",
      "Developed mappers to transform scraped data into structured resourceful information using python"
    ]
  },
  {
    name: "Globus bank",
    link: "https://globusbank.com",
    period: "October 2019 - October 2020",
    role: "Lead frontend developer",
    description: "Built the early version of the Corporate banking web application of a major bank",
    points: [
      "Led the frontend team in building the bank's corporate banking application from the groundup using modearn web technologies",
      "Collaborated with backend engineers to architect and integrate API services while adhering to standard OpenAPI specifications"
    ]
  },
  {
    name: "Techpoint Africa",
    link: "https://techpoint.africa",
    period: "December 2018 - September 2019",
    role: "Fullstack web developer",
    description: "Developed internal and customer-facing websites and applications",
    points: [
      "Developed e-commerce website for sales of quarterly sales reports",
      "Integrated paystack payment API into event ticketing website for easy payment collection",
      "implement measures to ensure uninterrupted operations of web applications during high traffic turnovers"
    ]
  }
]
</script>
