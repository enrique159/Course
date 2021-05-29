<template>
  <div class="container">
    <div class="nav">
      <div class="options">
        <div class="icon-option-menu">
          <box-icon name="left-arrow-alt" color="#9097A1"></box-icon>
        </div>
        <div class="notification">
          <span>
            <box-icon name="bell" color="#9097A1"></box-icon>
          </span>
        </div>
      </div>
      <div class="profile">
        <div class="name">
          <h4>Wesley Matthews</h4>
          <h6>Student</h6>
        </div>
        <div class="picture">
          <img src="@/assets/profile.svg" alt="" />
        </div>
      </div>
    </div>

    <!-- My learnings -->
    <div class="mylearning">
      <h4>My Learning</h4>
      <div class="course-1">
        <div class="icon-course">
          <img src="@/assets/target.svg" alt="icon" />
        </div>
        <div class="title-course">
          <h6>Target Audience Training</h6>
          <span
            >Save time and make your business <br />
            more effective by promoting...</span
          >
        </div>
        <div class="progress-course">
          <div class="circle">
            <h5>53<span>%</span></h5>
          </div>
        </div>
      </div>
      <div class="course-2">
        <div class="icon-course">
          <img src="@/assets/code.svg" alt="icon" />
        </div>
        <div class="title-course">
          <h6>The Complete Web...</h6>
          <span
            >Learn Web Development by building <br />
            25 websites...</span
          >
        </div>
        <div class="progress-course">
          <div class="circle">
            <h5>75<span>%</span></h5>
          </div>
        </div>
      </div>
      <div class="course-3">
        <div class="icon-course">
          <img src="@/assets/data.svg" alt="icon" />
        </div>
        <div class="title-course">
          <h6>Grow your Community</h6>
          <span>Follow these easy and simple steps</span>
        </div>
        <div class="progress-course">
          <div class="circle">
            <h5>14<span>%</span></h5>
          </div>
        </div>
      </div>
    </div>
    <calendar/>
  </div>
</template>

<script>
import Calendar from './Calendar.vue';
export default {
  components: { Calendar },
  name: "SideMenu",
};
</script>

<style lang="scss" scoped>
.container {
  box-sizing: border-box;
  padding: 0 48px;
  flex-grow: 100;
  height: 100%;

  .nav {
    height: 12%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .options {
      display: flex;
      .icon-option-menu {
        height: 38px;
        width: 38px;
        margin-right: 16px;
        border-radius: 14px;
        border: 1px solid #e3e3e3;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      .notification {
        height: 38px;
        width: 38px;
        padding-top: 3px;
        margin-right: 16px;
        border-radius: 14px;
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        span {
          &::before {
            content: "";
            display: block;
            position: absolute;
            top: 4px;
            left: 20px;
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background-color: red;
            border: 1px solid white;
          }
        }
      }
    }
    .profile {
      display: flex;
      .name {
        text-align: left;
        h4 {
          margin: 0;
          padding: 6px 0;
          padding-top: 10px;
        }
        h6 {
          margin: 0;
          font-size: 0.8rem;
          color: #0067ff;
        }
      }
      .picture {
        background-color: #f7f7f7;
        justify-content: center;
        align-items: flex-end;
        border-radius: 12px;
        margin-left: 36px;
        display: flex;
        height: 52px;
        width: 52px;
        img {
          width: 46px;
        }
      }
    }
  }

  .mylearning {
    display: inline-block;
    text-align: left;
    width: 100%;
    height: 40%;
    h4 {
      margin: 0;
      margin-bottom: 18px;
      font-size: 1.3rem;
      font-weight: 600;
      color: #9097a1;
    }

    .course-1,
    .course-2,
    .course-3 {
      display: flex;
      align-items: center;
      margin-bottom: 24px;
      .icon-course {
        background-color: rgb(239, 243, 248);
        justify-content: center;
        align-items: center;
        border-radius: 16px;
        margin-right: 12px;
        display: flex;
        height: 52px;
        width: 52px;
        img {
          height: 28px;
        }
      }

      .title-course {
        h6 {
          margin: 0;
          font-size: 1rem;
        }
        span {
          font-size: 0.8rem;
          color: gray;
        }
      }

      .progress-course {
        justify-content: flex-end;
        flex-grow: 100;
        display: flex;
        .circle {
          background-image: url("~@/assets/progress1.svg");
          justify-content: center;
          align-items: center;
          border-radius: 50%;
          display: flex;
          width: 52px;
          height: 52px;
          h5 {
            span {
              font-size: 0.6rem;
            }
          }
        }
      }
    }
    .course-2 {
      .progress-course {
        .circle {
          background-image: url("~@/assets/progress2.svg");
        }
      }
    }
    .course-3 {
      .progress-course {
        .circle {
          background-image: url("~@/assets/progress3.svg");
        }
      }
    }
  }
}
</style>