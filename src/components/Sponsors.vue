<template>
  <section>
    <h2>Special Sponsors</h2>
    <p>adipisci eveniet suscipit, modi totam quasi libero</p>

    <div class="cards">
      <div v-for="sponsor in sponsors" :key="sponsor.id" class="card">
        <img
          :src="require(`@/assets/${sponsor.img}`)"
          alt=""
          width="150"
          height="150"
        />
        <p class="name">{{ sponsor.name }}</p>
        <p class="pos">{{ sponsor.pos }}</p>
        <p class="org">@{{ sponsor.org }}</p>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Sponsors",
  props: {
    sponsors: Array,
  },
};
</script>
<style scoped>
section {
  margin: 3rem 1rem;
}
h2 {
  font-family: Barlow;
  font-size: 2rem;
  font-weight: 800;
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
  align-items: center;
  gap: 1rem;
}
img {
  border-radius: 100%;
}
.name {
  font-size: 1.1rem;
  font-weight: 500;
}
.pos {
  font-size: 1.3rem;
  font-weight: 700;
}
.org {
  font-weight: 500;
}
</style>
