<template>
  <nav>
    <div class="brand"><img width="50" src="../assets/logo.svg" alt="" /></div>
    <div class="list">
      <ul>
        <li><span>00</span> WHY</li>
        <li><span>01</span> WHO</li>
        <li><span>02</span> WHAT</li>
        <li><span>03</span> WHOMST</li>
      </ul>
      <button class="btn">Try For Free</button>
    </div>
  </nav>
</template>
<script>
export default {
  name: "Navbar",
  props: {
    msg: String,
  },
};
</script>
<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  box-shadow: 0 2px 2px 2px rgba(0, 0, 0, 0.5);
}
.list {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
ul {
  list-style: none;
  display: flex;
  gap: 30px;
  font-family: Barlow;
  font-weight: 600;
  font-size: 1.2rem;
  margin-inline-end: 8rem;
  align-items: center;
}
li span {
  font-size: 1.3rem;
  color: red;
}
</style>
