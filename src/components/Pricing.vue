<template>
  <section>
    <h2>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Animi corrupti
      nulla
    </h2>
    <p>adipisci eveniet suscipit, modi totam quasi libero</p>

    <div class="cards">
      <div v-for="price in prices" :key="price.id" class="card">
        <h3>{{ price.category }}</h3>
        <h4>{{ price.desc }}</h4>
        <p class="price"><span>$</span>{{ price.price }}<span>/mo</span></p>
        <div class="features">
          <p>
            <span>{{ price.mollitia }}</span
            ><span>mollitia</span>
          </p>
          <p><span>15</span><span>laudantium</span></p>
          <p><span>5</span><span>excepturi</span></p>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Pricing",
  props: {
    prices: Array,
  },
};
</script>
<style scoped>
section {
  margin: 3rem 1rem;
}
.cards {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  width: fit-content;
  margin: 2rem auto;
  justify-content: center;
}
.card {
  width: 280px;
  padding: 2rem 0.5rem;
  display: flex;
  flex-direction: column;
  border: 1px solid rgba(44, 62, 80, 0.1);
  border-radius: 5px;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  text-align: center;
  text-transform: capitalize;
}
.card h4 {
  margin-top: 5px;
  font-weight: 400;
}
.card h3 {
  font-size: 1.4rem;
  font-weight: 600;
}
.card .price {
  margin: 25px auto;
  font-size: 4rem;
  display: flex;
  font-weight: 900;
}
.card .price span {
  font-size: 1.5rem;
  font-weight: 500;
}
.card .price span:first-child {
  align-self: flex-start;
}
.card .price span:last-child {
  align-self: flex-end;
  margin-bottom: 15px;
}
.features {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.features p {
  display: flex;
  flex-direction: column;
  gap: 5px;
}
.features p span:first-child {
  font-weight: 600;
  font-size: 1.2rem;
}
</style>
