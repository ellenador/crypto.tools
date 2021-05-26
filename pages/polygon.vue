<template>
  <div>
    <h1 class="mt-4">Polygon Network</h1>

    <v-simple-table dense class="mt-4">
      <template v-slot:default>
        <thead>
          <tr>
            <th class="text-left">Names</th>
            <th class="text-left">Token rewards</th>
            <th class="text-left">Type</th>
            <th class="text-left">Link</th>
          </tr>
        </thead>
        <tbody class="grey--text mb-2">
          <tr v-for="item in desserts" :key="item.name">
            <td>{{ item.name }}</td>
            <td>{{ item.token }}</td>
            <td>{{ item.type }}</td>
            <td>{{ item.link }}</td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>

    <v-btn icon class="ml-n5 mt-9 mb-n6" x-small color="red" style="border: none !important">
      <v-icon style="border: none !important"> mdi-alert </v-icon>
    </v-btn>
    <v-simple-table
      dense
      style="border: 1px dashed #F44336 !important"
    >
      <template v-slot:default>
        <tbody class="grey--text mb-2">
          <tr v-for="item in desserts2" :key="item.name">
            <td>{{ item.name }}</td>
            <td>{{ item.token }}</td>
            <td>{{ item.type }}</td>
            <td>{{ item.link }}</td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>
      <p>I am in no way affiliated with the above projects, nor do I endorse them. Please do your own research before investing.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      desserts: [
        {
          name: "Aave",
          link: "https://aave.com",
          token: "stkAAVE",
          type: "DeFi (colateral & staking)",
        },
        {
          name: "Sushiswap",
          link: "https://app.sushi.com/farms",
          token: "SUSHI",
          type: "DeFi (swap, pools & yieldfarming)",
        },
        {
          name: "Beefy finance",
          link: "https://polygon.beefy.finance/",
          token: "various",
          type: "DeFi (yieldfarming automated)",
        },
        {
          name: "Opensea",
          link: "https://matic.opensea.io/",
          token: "",
          type: "NFT Marketplace",
        },
        {
          name: "Quickswap",
          link: "https://quickswap.exchange/#/swap",
          token: "QUICK",
          type: "DeFi (swap & pools)",
        },
        {
          name: "Etheremon",
          link: "https://ethermon.io/",
          token: "EMON",
          type: "Gamming",
        },
        {
          name: "Cometh",
          link: "https://swap.cometh.io/#/swap",
          token: "MUST",
          type: "DeFi (swap & pools)",
        },
        {
          name: "Alchemy Dao",
          link: "https://polygon.alchemydao.com",
          token: "ALCH",
          type: "DeFi (yieldfarming)",
        },
      ],
      desserts2: [
        {
          name: "Polycat finance",
          link: "https://polycat.finance/",
          token: "FISH",
          type: "DeFi (pools & yieldfarming)",
        },
        {
          name: "Polycake finance",
          link: "https://www.polycake.finance/",
          token: "PCAKE",
          type: "DeFi (pools & yieldfarming)",
        },
        {
          name: "Orcinuslabs",
          link: "https://www.orcinuslabs.ca/pools",
          token: "ORCA",
          type: "DeFi (pools & yieldfarming)",
        },
        {
          name: "Polybear",
          link: "https://polybear.exchange",
          token: "BEAR",
          type: "DeFi (pools & yieldfarming)",
        },
      ],
    };
  },
};
</script>

<style>
.v-data-table > .v-data-table__wrapper > table {
  width: 100%;
  border-spacing: 0;
  border: 1px rgb(230, 180, 230) !important;
  border-style: dashed double !important;
}

.theme--dark.v-data-table
  > .v-data-table__wrapper
  > table
  > thead
  > tr:last-child
  > th {
  border-bottom: 1px dashed rgb(230, 180, 230) !important;
}

.theme--dark.v-data-table
  > .v-data-table__wrapper
  > table
  > tbody
  > tr:hover:not(.v-data-table__expanded__content):not(.v-data-table__empty-wrapper) {
  background: #cacaca13 !important;
}
</style>
<style scoped>
.theme--dark,
.v-btn {
  border: 1px rgb(230, 180, 230) !important;
  border-style: dashed double !important;
}
.v-alert:not(.v-sheet--tile) {
  border: 1px dashed rgb(211, 40, 40) !important;
}
</style>