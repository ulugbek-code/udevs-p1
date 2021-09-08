<template>
  <div id="navbar">
    <div class="btn-groups btn-groups-first">
      <button>
        <img
          id="first-gr-icon-location"
          src="./assets/icons/location.svg"
          alt=""
        />
        Республика
        <img class="inner-icons" src="./assets/icons/next.svg" alt="" />
      </button>
      <button>
        Ташкент г.
        <img class="inner-icons" src="./assets/icons/next.svg" alt="" />
      </button>
      <button>
        Юнусабад т.
        <img id="first-gr-icon-down" src="./assets/icons/down.svg" alt="" />
      </button>
    </div>
    <div class="btn-groups-wrapper">
      <div class="btn-groups btn-groups-second">
        <button>Все</button>
        <button>ДХМ</button>
        <button class="active">ФҲДЁ</button>
      </div>
      <div class="btn-groups" id="btn-groups-third">
        <button>
          <img
            id="last-gr-icon-location"
            src="./assets/icons/calendar.svg"
            alt=""
          />
          Сегодня
          <img id="last-gr-icon-down" src="./assets/icons/down.svg" alt="" />
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
#navbar {
  width: 100%;
  height: 80px;
  padding: 0 5%;
  background: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
#navbar * {
  font-family: "Inter", sans-serif;
}
.btn-groups,
#btn-groups-third button {
  background: rgba(247, 247, 249, 1);
  border-radius: 40px;
  border: none;
}
.btn-groups-first {
  padding: 0 20px;
}
.btn-groups button {
  position: relative;
  background: transparent;
  color: rgba(8, 17, 35, 0.75);
  padding: 12px 16px;
  border: none;
  cursor: pointer;
  border-radius: 40px;
}
.btn-groups .active {
  background: linear-gradient(
    to right,
    rgba(69, 161, 255, 1),
    rgba(1, 118, 238, 1)
  );
}
.btn-groups-wrapper {
  display: flex;
}
.btn-groups-second button,
#btn-groups-third button {
  padding: 8px 36px;
}
.btn-groups-second button:hover {
  background: linear-gradient(
    to right,
    rgba(69, 161, 255, 1),
    rgba(1, 118, 238, 1)
  );
}
#btn-groups-third {
  margin-left: 1rem;
}
/* icons */
.inner-icons {
  position: absolute;
  right: 0;
  bottom: 40%;
}
#first-gr-icon-location {
  position: absolute;
  left: 0;
}
#first-gr-icon-down {
  position: absolute;
  top: 40%;
  right: -5%;
}
#last-gr-icon-location {
  position: relative;
  right: 5%;
  top: 2px;
}
#last-gr-icon-down {
  position: relative;
  left: 5%;
}
</style>
