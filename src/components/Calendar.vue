<template>
  <div class="calendar">
    <div class="planning">
      <span class="title">Planning</span>
      <div class="arrows">
        <div class="arrow">
          <box-icon name="left-arrow-alt" color="#3f3f3f"></box-icon>
        </div>
        <div class="arrow">
          <box-icon name="right-arrow-alt" color="#3f3f3f"></box-icon>
        </div>
      </div>
    </div>
    <div class="header">
      <span></span>
      <div class="typecalendar active">
        <h4>This week</h4>
      </div>
      <div class="typecalendar">
        <h4>Next week</h4>
      </div>
      <div class="typecalendar">
        <h4>This Month</h4>
      </div>
      <div class="typecalendar">
        <h4>This Year</h4>
      </div>
    </div>
    <div class="columns">
      <div class="hours">
        <span>07:00</span>
        <span>07:00</span>
        <span>07:00</span>
        <span>07:00</span>
        <span>07:00</span>
        <span>07:00</span>
      </div>
      <div class="col">
        <h6>M</h6>
      </div>
      <div class="col">
        <h6>T</h6>
      </div>
      <div class="col">
        <h6>W</h6>
      </div>
      <div class="col">
        <h6>Th</h6>
      </div>
      <div class="col">
        <h6>Fr</h6>
      </div>
      <div class="col">
        <h6>Sa</h6>
      </div>
    </div>
    <div class="bars">
      <div class="bar green">
        <span></span>
      </div>
      <div class="bar yellow">
        <span></span>
      </div>
      <div class="bar purple">
        <span></span>
      </div>
      <div class="bar gray">
        <span></span>
      </div>
      <div class="bar red">
        <span></span>
      </div>
    </div>
    <div class="reminder">
      <div class="icon-reminder">
        <box-icon name="map-pin"></box-icon>
      </div>
      <span>Don't forget to<br />call John..</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Calendar",
};
</script>

<style lang="scss" scoped>
.calendar {
  height: 48%;
  position: relative;
  .planning {
    display: flex;
    margin-bottom: 12px;
    .title {
      font-size: 1.3rem;
      font-weight: 600;
      color: #9097a1;
    }
    .arrows {
      margin-left: 24px;
      display: flex;
      align-items: center;
      .arrow {
        background-color: #f1f1f1;
        margin-right: 12px;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 28px;
        border-radius: 8px;
      }
    }
  }
  .header {
    display: flex;
    justify-content: space-between;
    position: relative;
    span {
      content: "";
      display: block;
      position: absolute;
      bottom: 0;
      left: 0;
      height: 2px;
      width: 100%;
      border-bottom: 2px #f3f3f3 solid;
    }
    .typecalendar {
      display: flex;
      align-items: center;
      text-align: center;
      color: rgb(199, 199, 199);
      height: 48px;
      h4 {
        margin: 0;
      }
    }
    .active {
      color: black;
      font-size: 1.2em;
      border-bottom: 2px #0067ff solid;
      z-index: 3;
    }
  }
  .columns {
    display: flex;
    justify-content: space-between;
    position: absolute;
    top: 86px;
    bottom: 24px;
    width: 100%;
    .hours {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      padding-top: 36px;
      padding-right: 12px;
      border-right: 2px #f3f3f3 solid;
      span {
        font-size: 0.6rem;
        color: darkgrey;
      }
    }
    .col {
      text-align: center;
      border-right: 2px #f3f3f3 solid;
      width: 100%;
      h6 {
        margin: 12px 0 0;
      }
    }
  }
  .bars {
    display: flex;
    flex-direction: column;
    position: absolute;
    justify-content: space-between;
    top: 86px;
    bottom: 24px;
    width: 100%;
    padding-left: 36px;
    padding-top: 36px;
    .bar {
      margin-top: 16px;
      margin-bottom: 16px;
      height: 12px;
      border-radius: 6px;
    }
    .green {
      background-color: rgb(113, 202, 29);
      margin-left: 20%;
      margin-right: 26%;
    }
    .yellow {
      background-color: #fdca3e;
      margin-left: 10%;
      margin-right: 0;
    }
    .purple {
      background-color: #c981f3;
      margin-left: 30%;
      margin-right: 30%;
    }
    .gray {
      background-color: rgb(224, 238, 240);
      margin-left: 50%;
      margin-right: 0;
    }
    .red {
      background-color: #f46367;
      margin-left: 40%;
      margin-right: 30%;
    }
  }
  .reminder {
    clip-path: polygon(0% 0%, 100% 0%, 100% 75%, 83% 75%, 70% 91%, 56% 75%, 0% 75%);
    background: rgba(255, 255, 255, 0.15);
    -webkit-backdrop-filter: blur(6px);
    backdrop-filter: blur(6px);
    padding: 16px 24px;
    height: 98px;
    position: absolute;
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: center;
    top: 118px;
    right: 20%;
    
    .icon-reminder {
      background-color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 50%;
      width: 38px;
      height: 38px;
    }
    span {
      margin-top: 6px;
      font-size: 0.8rem;
    }
  }
}
</style>