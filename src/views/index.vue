<template>
  <div id="index">
    <dv-full-screen-container class="bg">
      <dv-loading v-if="loading">Loading...</dv-loading>
      <div v-else class="host-body">
       <div>
         <v-header ></v-header>
       </div>

        <!-- 第二行 -->
        <!-- <div class="d-flex jc-between px-2">
          <div class="d-flex" style="width: 40%">
            <div
              class="react-right ml-4"
              style="width: 6.25rem; text-align: left;background-color: #0f1325;"
            >
              <span class="react-before"></span>
              <span class="text">数据分析1</span>
            </div>
            <div class="react-right ml-3" style="background-color: #0f1325;">
              <span class="text colorBlue">数据分析2</span>
            </div>
          </div>
          <div style="width: 40%" class="d-flex">
            <div class="react-left bg-color-blue mr-3">
              <span class="text fw-b">vue-big-screen</span>
            </div>
            <div
              class="react-left mr-4"
              style="width: 6.25rem; background-color: #0f1325; text-align: right;"
            >
              <span class="react-after"></span>
              <span class="text">2020年03月16日 周一 12:00</span>
            </div>
          </div>
        </div> -->

        <div class="body-box">
          <!-- 第三行数据 -->
          <div class="content-box">
            <div>
              <dv-border-box-12>
                <centerLeft1 />
                
              </dv-border-box-12>
            </div>
            <div>
              <dv-border-box-12>
                <centerLeft2 />
              </dv-border-box-12>
            </div>
            <!-- 中间 -->
            <div>
              <center />
            </div>
            <!-- 中间 -->
            <div>
              <centerRight2 />
            </div>
            <div>
              <dv-border-box-13>
                <centerRight1 />
              </dv-border-box-13>
            </div>
          </div>

          <!-- 第四行数据 -->
          <div class="bototm-box">
            <dv-border-box-13>
              <bottomLeft />
            </dv-border-box-13>
            <dv-border-box-12>
              <bottomRight />
            </dv-border-box-12>
          </div>
        </div>
      </div>
    </dv-full-screen-container>
  </div>
</template>

<script>
import vHeader from "../components/layout/header"
import centerLeft1 from "./centerLeft1";
import centerLeft2 from "./centerLeft2";
import centerRight1 from "./centerRight1";
import centerRight2 from "./centerRight2";
import center from "./center";
import bottomLeft from "./bottomLeft";
import bottomRight from "./bottomRight";
export default {
  data() {
    return {
      loading: true
    };
  },
  components: {
    vHeader,
    centerLeft1,
    centerLeft2,
    centerRight1,
    centerRight2,
    center,
    bottomLeft,
    bottomRight
  },
  mounted() {
    this.cancelLoading();
  },
  methods: {
    cancelLoading() {
      setTimeout(() => {
        this.loading = false;
      }, 500);
    }
  }
};
</script>

<style lang="scss">
#index {
  color: #d3d6dd;
  background-color: #000000;
  width: 100%;
  height: 100vh;

  .bg {
    // padding: 0.2rem 0.2rem 0 0.2rem;
    background-image: url("../assets/background.png");
    background-size: cover;
    background-position: center center;
  }

  .host-body {
    .title {
      position: relative;
      width: 6.25rem;
      text-align: center;
      background-size: cover;
      background-repeat: no-repeat;

      .title-text {
        font-size: 0.3rem;
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translate(-50%);
      }

      .title-bototm {
        position: absolute;
        bottom: -0.375rem;
        left: 50%;
        transform: translate(-50%);
      }
    }

    // 平行四边形
    .react-left {
      cursor: pointer;
      font-size: 0.225rem;
      width: 3.75rem;
      height: 0.625rem;
      line-height: 0.625rem;
      text-align: center;
      transform: skewX(-45deg);

      .react-after {
        position: absolute;
        right: -0.3125rem;
        top: 0;
        height: 0.625rem;
        width: 0.625rem;
        background-color: #0f1325;
        transform: skewX(45deg);
      }

      .text {
        display: inline-block;
        transform: skewX(45deg);
      }
    }

    .react-right {
      cursor: pointer;
      font-size: 0.225rem;
      width: 3.75rem;
      height: 0.625rem;
      line-height: 0.625rem;
      text-align: center;
      transform: skewX(45deg);

      .react-before {
        position: absolute;
        left: -0.3125rem;
        top: 0;
        height: 0.625rem;
        width: 0.625rem;
        background-color: #0f1325;
        transform: skewX(-45deg);
      }

      .text {
        display: inline-block;
        transform: skewX(-45deg);
      }
    }

    .body-box {
      margin-top: 0.2rem;
      display: flex;
      flex-direction: column;

      //下方区域的布局
      .content-box {
        display: grid;
        grid-template-columns: 2fr 3fr 5fr 3fr 2fr;
      }

      // 底部数据
      .bototm-box {
        margin-top: 0.125rem;
        display: grid;
        grid-template-columns: repeat(2, 50%);
      }
    }
  }
}

</style>