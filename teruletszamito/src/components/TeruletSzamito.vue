<template>
  <div>
    <h2>Területszámító</h2>
    <br />

    <label for="inputA">A értéke:</label>
    <input v-model="a" type="number" placeholder="Adja meg az A értékét" />

    <br />
    <br />

    <label for="inputB">B értéke:</label>
    <input v-model="b" type="number" placeholder="Adja meg a B értékét" />

    <br />
    <br />

    <button @click="szamolTerulet">Számol</button>

    <br />
    <br />

    <p>{{ eredmeny }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      a: "",
      b: "",
      eredmeny: "",
    };
  },
  methods: {
    szamolTerulet() {
      if (!this.a || !this.b) {
        alert("Kérem töltse ki mindkét mezőt!");
        return;
      }

      this.eredmeny = "A terület: " + this.a * this.b;
    },
  },
};
</script>

<style scoped>
/* Itt lehet stílusokat megadni, ha szükséges */
</style>
