<script>
export default {
  data: function () {
    return {
      cards: [
        {
          id: 0,
          suit: "spades",
          value: 0,
        },
        {
          id: 1,
          suit: "clubs",
          value: 0,
        },
        {
          id: 2,
          suit: "diamonds",
          value: 0,
        },
        {
          id: 3,
          suit: "hearts",
          value: 0,
        },
        {
          id: 4,
          suit: "spades",
          value: 1,
        },
      ],
    };
  },
  created: function () {},
  methods: {},
};
</script>

<template>
  <div class="home">
    <div class="remaining-cards">
      <!-- REMAINING CARDS TABLE -->
      <h3>Remaining Cards</h3>
      <table>
        <thead>
          <tr>
            <th scope="col">Suit</th>
            <th scope="col">Value</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="card in cards" :key="card.id">
            <td>{{ card.suit }}</td>
            <td>{{ card.value }}</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="drawn-cards">
      <!-- Drawn CARDS TABLE -->
      <h3>Drawn Cards</h3>
      <table>
        <thead>
          <tr>
            <th scope="col">Suit</th>
            <th scope="col">Value</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="card in cards" :key="card.id">
            <td>{{ card.suit }}</td>
            <td>{{ card.value }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<style>
table,
th,
td {
  border: 1px solid black;
}
</style>
