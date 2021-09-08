<template>
  <div id="widgets-container">
    <div class="wrapper">
      <div class="box">
        <div class="icon-box">
          <img src="./assets/icons/blue-box.svg" alt="" />
        </div>
        <div class="info-box">
          <h3>Ташрифлар сони</h3>
          <p>{{ visits }}</p>
        </div>
      </div>
      <div class="box">
        <div class="icon-box">
          <img src="./assets/icons/clock-around.svg" alt="" />
        </div>
        <div class="info-box">
          <h3>Навбатда</h3>
          <p>
            {{ queue }}
            <span class="inner-span">({{ queuePer }}%)</span>
          </p>
        </div>
      </div>
      <div class="box">
        <div class="icon-box">
          <img src="./assets/icons/waiting-person.svg" alt="" />
          <!-- <img src="./assets/icons/sitting-person.svg" alt="" /> -->
        </div>
        <div class="info-box">
          <h3>Узок кутганлар</h3>
          <p>
            {{ awaited }}
            <span class="inner-span">({{ awaitedPer }}%)</span>
          </p>
        </div>
      </div>
      <div class="box">
        <div class="icon-box">
          <img src="./assets/icons/checked.svg" alt="" />
        </div>
        <div class="info-box">
          <h3>Якунланди</h3>
          <p>
            {{ finished }}
            <span class="inner-span">({{ finishedPer }}%)</span>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: [
    "visits",
    "queue",
    "awaited",
    "finished",
    "queue-per",
    "awaited-per",
    "finished-per",
  ],
};
</script>

<style scoped>
#widgets-container {
  width: 100%;
  height: 150px;
  background: rgba(247, 247, 249, 1);
}
.wrapper {
  width: 90%;
  height: 100%;
  display: flex;
  justify-content: space-around;
  margin: 0 auto;
  padding: 20px 0;
}
.box {
  display: flex;
  padding: 20px;
  border-radius: 16px;
  background: #fff;
}
.box:nth-child(1) p {
  color: #0e87ff;
}
.box:nth-child(2) p {
  color: #5e4be1;
}
.box:nth-child(3) p {
  color: #f32828;
}
.box:nth-child(4) p {
  color: #22c63d;
}
.icon-box {
  position: relative;
}
.icon-box img {
  position: relative;
  top: 10%;
  margin-right: 1rem;
}
.info-box {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-align: end;
}
.info-box h3 {
  font-size: 16px;
  line-height: 24px;
  font-weight: 600;
}
.info-box p {
  font-size: 20px;
  line-height: 32px;
  font-weight: 500;
}
.inner-span {
  font-size: 14px;
  color: rgb(184, 161, 161);
}
</style>
