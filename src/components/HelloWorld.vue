<script setup>
import { ref } from 'vue';
import '@kyndryl-design-system/shidoka-charts/components/chart';

const count = ref(0);
</script>

<template>
  <div class="kd-grid">
    <div class="kd-grid__col--sm-4 kd-grid__col--md-8 kd-grid__col--lg-12">
      <h1 class="kd-type--headline-03">Shidoka Vue Sample App</h1>
    </div>

    <div class="kd-grid__col--sm-4 kd-grid__col--md-4 kd-grid__col--lg-8">
      <kd-chart
        type="bar"
        height="400"
        chartTitle="Bar Chart"
        description="Description"
        :labels="['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange']"
        :datasets="[
          { label: 'Dataset 1', data: [12, 19, 3, 5, 2, 3] },
          { label: 'Dataset 2', data: [8, 15, 7, 9, 6, 12] },
        ]"
        :options="{
          scales: {
            x: {
              title: {
                text: 'Color',
              },
            },
            y: {
              title: {
                text: 'Votes',
              },
            },
          },
        }"
      />
    </div>

    <div class="kd-grid__col--sm-4 kd-grid__col--md-4 kd-grid__col--lg-4">
      <kd-chart
        type="doughnut"
        chartTitle="Doughnut Chart"
        description="Description"
        height="400"
        :labels="['Blue', 'Red', 'Orange', 'Yellow', 'Green', 'Purple']"
        :datasets="[
          {
            label: 'Dataset 1',
            data: [12, 19, 3, 5, 2, 3],
          },
        ]"
        :options="{
          scales: {
            x: {
              title: {
                text: 'Color',
              },
            },
            y: {
              title: {
                text: 'Votes',
              },
            },
          },
        }"
      />
    </div>
  </div>
</template>
