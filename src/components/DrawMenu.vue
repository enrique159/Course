<template>
  <div class="container">
    <div class="logo">
      <img src="@/assets/logo.svg" alt="icon">
      <span>Course</span>
    </div>
    <div class="menu">
      <div class="option-menu" v-for="item in options" v-bind:key="item.index" @click="selectOption(item)">
        <div :class="item.isActive ? 'active-icon icon-option-menu' : 'icon-option-menu'">
          <box-icon :name='item.icon' :color=" item.isActive ? '#FFFFFF' : '#9097A1'"></box-icon>
        </div>
        <div :class="item.isActive ? 'active-title title-option-menu' : 'title-option-menu'">{{ item.title}}</div>
      </div>
    </div>
    <div class="option">
      <div class="infoText">
        <span>Upgrade your plan, <a href="#">Pro plan</a> </span>
      </div>
      <div class="infoIcon">
        <span class="blueboxes"></span>
        <span class="whitearrows"></span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DrawMenu",
  data() {
    return {
      options: [
        {
          icon: "bar-chart",
          title: "Performance",
          isActive: true,
        },
        {
          icon: "book-open",
          title: "Courses",
          isActive: false,
        },
        {
          icon: "comment-dots",
          title: "Comment",
          isActive: false,
        },
        {
          icon: "paint",
          title: "Tools",
          isActive: false,
        },
        {
          icon: "box",
          title: "Resources",
          isActive: false,
        },
      ]
    }
  },
  methods: {
    selectOption(option) {
      if (!option.isActive) {
        this.options.forEach((x) => (x.isActive = false));
        option.isActive = true;
      }
    },
  }
};
</script>

<style lang="scss" scoped>
.container {
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 20%;
  max-width: 286px;
  padding: 24px 48px;

  .logo, .menu, .option {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .logo {
    height: 10%;
    span {
      padding-top: 6px;
      font-size: 1.4rem;
      font-weight: 600;
    }
    img {
      height: 24px;
      margin-right: 6px;
    }
  }

  .menu {
    flex-direction: column;
    margin: auto 0;
    height: auto;
    display: flex;
    text-align: left;

    .option-menu {
      display: flex;
      cursor: pointer;
      width: 100%;
      padding: 12px 8px;
      border-radius: 24px;
      color: rgb(144, 151, 161);
      &:hover {
        background-color: #f7f7f7;
      }

      .icon-option-menu {
        height: 38px;
        width: 38px;
        margin-right: 16px;
        border-radius: 14px;
        transition: 0.3s ease-in-out;
        display: flex;
        justify-content: center;
        align-items: center;
        #icon {
          transition: 0.3s ease-in-out;
        }
      }

      .title-option-menu {
        padding: 12px 0;
        font-weight: 600;
        transition: 0.3s ease-in-out;
      }

      .active-icon {
        background-color: #0067FF;
        box-shadow: 0px 12px 16px 2px rgba(0, 102, 255, 0.295);
      }

      .active-title {
        color: #0067FF;
        font-weight: 600;
      }
    }
  }

  .option {
    background-color: #1E1F38;
    border-radius: 36px;
    height: 184px;
    display: flex;
    flex-direction: column;
    color: white;
    .infoText {
      padding: 0 36px 12px;
      span {
        font-size: 1rem;
      }
      a {
        font-weight: 900;
        color: white;
        text-decoration: underline;
      }
    }
    .infoIcon {
      padding-top: 24px;
      position: relative;
      text-align: left;
      width: 40%;
      height: 12px;
      .blueboxes { 
        &::before {
          content: '';
          display: block;
          position: absolute;
          top: 12px;
          height: 32px;
          width: 32px;
          margin-left: 10px;
          background-color: #162c8d;
          border-radius: 10px;
        }
        &::after {
          content: '';
          display: block;
          position: absolute;
          top: 10px;
          height: 36px;
          width: 36px;
          background-color: #0067FF;
          border-radius: 12px;
        }
      }
      .whitearrows {
        &::before {
          content: '';
          display: block;
          position: absolute;
          top: 27px;
          transform: rotate(45deg);
          left: 4px;
          height: 3px;
          width: 16px;
          border-radius: 2px;
          background-color: white;
        }
        &::after {
          content: '';
          display: block;
          position: absolute;
          top: 32px;
          bottom: 12px;
          left: -20px;
          height: 3px;
          width: 36px;
          border-radius: 3px;
          background-color: white;
        }
      }
    }
  }
}
</style>