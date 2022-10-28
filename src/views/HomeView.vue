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
        {
          id: 5,
          suit: "clubs",
          value: 1,
        },
        {
          id: 6,
          suit: "diamonds",
          value: 1,
        },
        {
          id: 7,
          suit: "hearts",
          value: 1,
        },
        {
          id: 8,
          suit: "spades",
          value: 2,
        },
        {
          id: 9,
          suit: "clubs",
          value: 2,
        },
        {
          id: 10,
          suit: "diamonds",
          value: 2,
        },
        {
          id: 11,
          suit: "hearts",
          value: 2,
        },
        {
          id: 12,
          suit: "spades",
          value: 3,
        },
        {
          id: 13,
          suit: "clubs",
          value: 3,
        },
        {
          id: 14,
          suit: "diamonds",
          value: 3,
        },
        {
          id: 15,
          suit: "hearts",
          value: 3,
        },
      ],
    };
  },
  created: function () {},
  methods: {
    reshuffle: function () {
      let cards = this.cards;
      cards.reverse();
      console.log(cards);
    },
    drawnCards: function () {},
    remainingCards: function () {},
    // Button #2 ("Draw") is where I stopped.
  },
};
</script>

<template>
  <div class="home">
    <!-- BUTTONS -->
    <button v-on:click="reshuffle()">Reshuffle</button>
    ||
    <button v-on="click">Draw</button>
    ||

    <button v-on="click">Draw new hand</button>

    <div class="drawn-cards" style="overflow: auto">
      <!-- DRAWN CARDS TABLE -->
      <h3>DRAWN CARDS</h3>

      <table style="overflow: auto; margin-left: auto; margin-right: auto">
        <thead>
          <tr>
            <th scope="col">Suit</th>
            <th scope="col">Value</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="card in cards" :key="card.id">
            <td>suit</td>
            <td>value</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="remaining-cards">
      <!-- REMAINING CARDS TABLE -->
      <h3>REMAINING CARDS</h3>
      <table style="overflow: auto; margin-left: auto; margin-right: auto">
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
