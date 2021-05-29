<template>
  <div class="card">
    <div class="info-card">
      <div class="icon-card">
        <img src="@/assets/asset-4.svg" alt="" />
      </div>
      <div class="title-card">
        <h6>Target Audience Training</h6>
        <span>Follow these easy and simple steps</span>
      </div>
      <div class="calendar">
        <div class="day">
          <span>21</span>
        </div>
        <h6>Full</h6>
      </div>
    </div>
    <div class="progress">
      <div class="progressbar">
        <span></span>
      </div>
      <div class="enroll">
        <span>Enroll</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardPurple'
};
</script>

<style lang="scss" scoped>
.card {
  background-color: #f46367;
  border-radius: 24px;
  box-sizing: border-box;
  padding: 12px;
  height: fit-content;
  .info-card {
    display: flex;
    .icon-card {
      width: 30%;
      img {
        height: 86px;
      }
    }
    .title-card {
      width: 50%;
      color: rgb(255, 255, 255);
      text-align: left;
      h6 {
        margin: 0 0 8px;
        font-weight: 900;
        font-size: 1rem;
      }
      span {
        font-size: 0.9rem;
      }
    }
    .calendar {
      width: 20%;
      display: flex;
      align-items: flex-end;
      flex-direction: column;
      .day {
        background-color: white;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 16px;
        margin-bottom: 6px;
        height: 48px;
        width: 48px;
        span {
          font-size: 1.4rem;
          font-weight: 900;
          color: black;
        }
      }
      h6 {
        margin: 0;
        text-align: center;
        width: 48px;
        color: white;
        font-size: 0.7rem;
        font-weight: 600;
      }
    }
  }
  .progress {
    width: 100%;
    display: flex;
    .progressbar {
      width: 70%;
      position: relative;
      padding: 12px 0 12px 12px;
      span {
        &::before {
          content: "";
          display: block;
          background-color: rgba(255, 255, 255, 0.5);
          border-radius: 2px;
          height: 4px;
          width: 100%;
        }
        &::after {
          content: "";
          display: block;
          position: absolute;
          top: 12px;
          left: 12px;
          background-color: rgb(255, 255, 255);
          border-radius: 2px;
          height: 4px;
          width: 40%;
        }
      }
    }
    .enroll {
      width: 30%;
      position: relative;
      span {
        font-size: 0.8rem;
        font-weight: 600;
        color: white;
        &::before {
          background-color: rgb(255, 255, 255);
          position: absolute;
          content: '';
          display: block;
          top: 10px;
          right: 2px;
          width: 24px;
          height: 2px;
        }
        &::after {
          background-color: rgb(255, 255, 255);
          position: absolute;
          content: '';
          display: block;
          transform: rotate(45deg);
          top: 7px;
          right: 1px;
          width: 8px;
          height: 2px;
        }
      }
    }
  }
}
</style>