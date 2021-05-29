<template>
  <div class="container">
    <div class="contenedor">
      <div class="header">
        <div>
          <div class="title">Course Activity</div>
          <div class="subtitle">June 28th, 2020</div>
        </div>
        <div class="btnPlus">
          <box-icon name="plus" color="#FFFFFF"></box-icon>
        </div>
      </div>
      <div class="content">
        <div class="options">
          <span class="course">Courses</span>
          <div class="arrows">
            <div class="arrow">
              <box-icon name="left-arrow-alt" color="#3f3f3f"></box-icon>
            </div>
            <div class="arrow">
              <box-icon name="right-arrow-alt" color="#3f3f3f"></box-icon>
            </div>
          </div>
          <div class="switcher">
            <span class="blocs"></span>
            <div class="bc">
              <span class="list"></span>
            </div>
          </div>
        </div>
        <div class="scrolldiv">
          <card />
          <div style="height: 18px"></div>
          <card-purple />
          <div style="height: 18px"></div>
          <card-yellow />
          <div style="height: 18px"></div>
          <card-red />
          <div style="height: 18px"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Cards/Card.vue";
import CardPurple from "./Cards/CardPurple.vue";
import CardRed from "./Cards/CardRed.vue";
import CardYellow from "./Cards/CardYellow.vue";
export default {
  components: { Card, CardPurple, CardYellow, CardRed },
  name: "MediumMenu",
};
</script>

<style lang="scss" scoped>
.container {
  box-sizing: border-box;
  height: 100%;
  width: 30%;
  max-width: 488px;
  padding: 24px 0;

  .contenedor {
    box-sizing: border-box;
    background-color: rgb(239, 243, 248);
    border-radius: 36px;
    padding: 36px 18px 0;
    height: 100%;
    position: relative;

    .header {
      display: flex;
      justify-content: space-between;
      text-align: left;
      margin-bottom: 48px;
      &:first-child {
        .title {
          font-size: 1.6rem;
          font-weight: 600;
          color: black;
          margin-bottom: 6px;
        }
        .subtitle {
          font-size: 1.1rem;
          font-weight: 400;
          color: #0067ff;
        }
      }
      .btnPlus {
        height: 54px;
        width: 42px;
        border-radius: 14px;
        transition: 0.3s ease-in-out;
        cursor: pointer;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #0067ff;
        box-shadow: 0px 12px 16px 2px rgba(0, 102, 255, 0.295);
        &:hover {
          box-shadow: 0px 8px 16px 4px rgba(0, 102, 255, 0.5);
        }
      }
    }

    .content {
      .options {
        display: flex;
        margin-bottom: 24px;
        .course {
          width: 25%;
          font-size: 1.2rem;
          text-align: left;
          color: rgb(144, 151, 161);
        }
        .arrows {
          display: flex;
          align-items: center;
          width: 65%;
          .arrow {
            background-color: #ffffff;
            margin-right: 12px;
            display: flex;
            justify-content: center;
            align-items: center;
            width: 28px;
            border-radius: 8px;
          }
        }
        .switcher {
          background-color: white;
          border-radius: 12px;
          text-align: right;
          position: relative;
          height: 24px;
          width: 48px;
          .blocs {
            &::before {
              content: "";
              display: block;
              position: absolute;
              background-color: rgb(167, 167, 167);
              box-shadow: 6px 0px 0px 0px rgb(167, 167, 167);
              top: 7px;
              left: 8px;
              height: 4px;
              width: 4px;
            }
            &::after {
              content: "";
              display: block;
              position: absolute;
              background-color: rgb(167, 167, 167);
              box-shadow: 6px 0px 0px 0px rgb(167, 167, 167);
              top: 13px;
              left: 8px;
              height: 4px;
              width: 4px;
            }
          }
          .bc {
            position: absolute;
            top: 2px;
            right: 2px;
            border-radius: 50%;
            background-color: rgb(26, 86, 252);
            height: 20px;
            width: 20px;
            .list {
              &::before {
                content: "";
                display: block;
                position: absolute;
                background-color: rgb(255, 255, 255);
                box-shadow: 0px 3px 0px 0px rgb(255, 255, 255);
                top: 6px;
                left: 6px;
                height: 2px;
                width: 8px;
              }
              &::after {
                content: "";
                display: block;
                position: absolute;
                background-color: rgb(255, 255, 255);
                top: 12px;
                left: 6px;
                height: 2px;
                width: 8px;
              }
            }
          }
        }
      }
      .scrolldiv {
        border-radius: 0 0 10px 10px;
        position: absolute;
        top: 186px;
        bottom: 0px;
        left: 24px;
        right: 24px;
        overflow-x: hidden;
        overflow-y: scroll;
        -ms-overflow-style: none;  /* IE and Edge */
        scrollbar-width: none;
        /* width */
        &::-webkit-scrollbar {
          display: none;
        }
      }
    }
  }
}
</style>