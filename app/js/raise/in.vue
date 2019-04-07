<template>
    <panel title="In货推荐">
        <section :class="$style.content">
            <div :class="$style.item" v-for="(item,index) in items" :key="item.img">
                <img :src="item.catory" alt="">
                <div :class="$style.list">
                    <div :class="$style.product" v-for="pro in item.list" :key="pro.img">
                        <img :src="pro.img" alt="">
                        <p :class="$style.title">{{pro.title}}</p>
                        <p :class="$style.price"><em>{{pro.price}}</em>起</p>
                        <div :class="$style.bar">
                            <div :class="$style.barWrapper">
                                <div :class="$style.inner" :style="{width:pro.progress+'%'}"></div>
                            </div>
                            <p>{{pro.progress}}%</p>
                        </div>
                        <label v-if="index==0">精选</label>
                    </div>
                </div>
            </div>
        </section>
    </panel>
</template>

<script type="text/ecmascript-6">
import Panel from "../common/Panel";

export default {
  data() {
    return {
      items: [
        {
          catory:
            "//img12.360buyimg.com/jrpmobile/jfs/t3406/210/2247820735/50952/86016eea/5846d8e7N20446dbd.png?width=750&height=200",
          list: [
            {
              img:
                "https://img30.360buyimg.com/cf/s250x250_jfs/t14881/283/656508232/143980/9b606acf/5a33a171N18c9c80a.jpg",
              title: "双响炮蓝牙音箱",
              price: "29.00",
              progress: 72
            },
            {
              img:
                "https://img30.360buyimg.com/cf/s250x250_jfs/t15529/308/632300625/135123/adb9c6d0/5a37676dNc31da9ea.jpg",
              title: "脑波相机",
              price: "998.00",
              progress: 259
            }
          ]
        },
        {
          catory:
            "//img12.360buyimg.com/jrpmobile/jfs/t3739/82/2244582797/54399/746c7d79/5846a953N66b67d05.png?width=750&height=200",
          list: [
            {
              img:
                "https://img30.360buyimg.com/cf/s250x250_jfs/t11257/287/2281727659/55759/e00b90a/5a138f21N32dca834.jpg",
              title: "智能电动牙刷",
              price: "19.00",
              progress: 481
            },
            {
              img:
                "https://img30.360buyimg.com/cf/s250x250_jfs/t14209/293/662014092/61635/bba5c330/5a33a983N077cac56.jpg",
              title: "烟草加热电子烟",
              price: "258.00",
              progress: 105
            }
          ]
        },
        {
          catory:
            "//img12.360buyimg.com/jrpmobile/jfs/t3214/113/4408032436/61548/ce316eef/5846d310Ne93f00c9.png?width=750&height=200",
          list: [
            {
              img:
                "https://img30.360buyimg.com/cf/s250x250_jfs/t15007/47/884045069/149879/17987250/5a3cb182N15868ea1.jpg",
              title: "赖公高淮封藏老酒",
              price: "99.00",
              progress: 199
            },
            {
              img:
                "https://img30.360buyimg.com/cf/s250x250_jfs/t14197/160/546457496/134173/4e1baccd/5a30ccc5Na44f7492.jpg",
              title: "泗洪花雕醉蟹",
              price: "58.00",
              progress: 222
            }
          ]
        }
      ]
    };
  },
  components: {
    Panel
  }
};
</script>

<style lang="scss" module>
@import "../../css/element";

.content {
  .item {
    text-align: center;
    padding-bottom: 20px;
    .list {
      @include list(row);
      justify-content: space-around;
      .product {
        width: 45%;
        height: 198px;
        background: rgba(0, 0, 0, 0.02);
        position: relative;
        img {
          margin: 22px auto 10px;
          width: 90px;
          height: 90px;
        }
        .title {
          font-family: PingFangSC-Medium;
          font-size: 14px;
          color: #444;
        }
        .price {
          font-family: PingFangSC-Semibold;
          font-size: 10px;
          color: #999;
          line-height: 24px;
          em {
            margin-right: 2px;
            font-size: 18px;
            color: #ff3232;
            &:before {
              content: "￥";
              font-size: 14px;
            }
          }
        }
        .bar {
          @include list(row);
          align-items: center;
          justify-content: space-between;
          padding: 0 10px;
          line-height: 15px;
          .barWrapper {
            width: 72px;
            height: 5px;
            background: #f6e6e6;
            border-radius: 11px;
            .inner {
              width: 40%;
              max-width: 100%;
              height: 5px;
              background-image: linear-gradient(270deg, #f55 1%, #ff9c31 100%);
              border-radius: 11px;
            }
          }
          p {
            font-size: 12px;
            color: #999;
          }
        }
        label {
          position: absolute;
          left: 0;
          top: 0;
          font-family: PingFangSC-Medium;
          font-size: 10px;
          color: #ff0000;
          text-align: center;
          padding: 2px 4px;
          background-image: linear-gradient(-35deg, #c1c1c1 0, #acacac 100%);
        }
      }
    }
  }
}
</style>