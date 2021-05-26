<template>
  <div>
    <h1 class="mt-4">Parachains of Kusama</h1>

    <v-simple-table dense class="mt-4">
      <template v-slot:default>
        <thead>
          <tr>
            <th class="text-left">Names</th>
            <th class="text-left">Symbol</th>
            <th class="text-left">Type</th>
            <th class="text-left">Link</th>
            <th class="text-left">Rewards</th>
          </tr>
        </thead>
        <tbody class="grey--text mb-2">
          <tr v-for="item in desserts" :key="item.name">
            <td>{{ item.name }}</td>
            <td>{{ item.symbol }}</td>
            <td>{{ item.type }}</td>
            <td>{{ item.link }}</td>
            <td>{{ item.rewards }}</td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      desserts: [
        {
          name: "Karura",
          link: "https://acala.network/karura",
          symbol: "KAR",
          type: "DeFi",
          rewards: "1 KSM = 12 KAR",
        },
        {
          name: "Moonriver",
          link: "https://moonbeam.network/networks/moonriver/",
          symbol: "RIVER",
          type: "Smart Contract",
          rewards: "",
        },
        {
          name: "Shiden Network",
          link: "https://shiden.plasmnet.io/",
          symbol: "SDN",
          type: "Smart Contract",
          rewards: "1 KSM = 10-20",
        },
        {
          name: "SherpaX",
          link: 'https://chainx.org/en/',
          symbol: "Ksx",
          type: "Interoperability",
          rewards: "",
        },
        {
          name: "Robonomics",
          link: 'https://robonomics.network/',
          symbol: "XRT",
          type: "Marketplace",
          rewards: "",
        },
        {
          name: "Bifrost",
          link: "https://ksm.vtoken.io/ (Code:QN2463)",
          symbol: "BCN",
          type: "Staking Protocol",
          rewards: "1 KSM = 1 svKSM",
        },
        {
          name: "Genshiro",
          link: 'https://genshiro.equilibrium.io/en',
          symbol: "GENS",
          type: "DeFi",
          rewards: "",
        },
        {
          name: "Subsocial",
          link: 'https://subsocial.network/',
          symbol: "SNM",
          type: "Social Network",
          rewards: "",
        },
        {
          name: "Darwinia Crab",
          link: "https://crab.network/",
          symbol: "CRING",
          type: "Interoperability",
          rewards: "",
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
.theme--dark, .v-btn {
  border: 1px rgb(230, 180, 230) !important;
  border-style: dashed double !important;
}
</style>