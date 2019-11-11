<!--
 * @Author: wang cai-hong
 * @Date: 2019-11-11 10:56:19
 -->
<template>
  <div class="time-line-con">
      <h2>border</h2>
      <div class="time-content">
          <div class="content-detail" v-for="item in testList" :key="item.key">
              <p><font-awesome-icon :icon="['fas','plane']" size="lg"  class="font-icon" />{{item.time}}</p>
              <p>
                <span v-for="con in item.texts" :key="con.tag">{{con.content}}</span>
              </p>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: "TimeLineTwo",
  data() {
    return {
      testList: [
        {
          key: "1",
          time: "2001-01-01 01:00:00",
          texts: [
            {
              tag: 0,
              content:
                "我是第一个的第一个我是第一个的第一个我是第一个的第一个我是第一个的第一个我是第一个的第一个我是第一个的第一个"
            },
            {
              tag: 1,
              content: "我是第一个的第二个"
            },
            {
              tag: 2,
              content: "我是第一个的第三个"
            },
            {
              tag: 3,
              content: "我是第一个的第一个"
            },
            {
              tag: 4,
              content: "我是第一个的第二个"
            },
            {
              tag: 5,
              content: "我是第一个的第三个"
            }
          ]
        },
        {
          key: "2",
          time: "2002-02-02 02:00:00",
          texts: [
            {
              tag: 0,
              content: "我是第二个的第一个"
            },
            {
              tag: 1,
              content: "我是第二个的第二个"
            },
            {
              tag: 2,
              content: "我是第二个的第三个"
            }
          ]
        },
        {
          key: "3",
          time: "2003-03-03 03:00:00",
          texts: [
            {
              tag: 0,
              content: "我是第三个的第一个"
            },
            {
              tag: 1,
              content: "我是第三个的第二个"
            },
            {
              tag: 2,
              content: "我是第三个的第三个"
            }
          ]
        },
        {
          key: "4",
          time: "2004-04-04 04:00:00",
          texts: [
            {
              tag: 0,
              content: "我是第四个的第一个"
            },
            {
              tag: 1,
              content: "我是第四个的第二个"
            },
            {
              tag: 2,
              content: "我是第四个的第三个"
            }
          ]
        },
        {
          key: "5",
          time: "2005-05-05 05:00:00",
          texts: [
            {
              tag: 0,
              content: "我是第五个的第一个"
            },
            {
              tag: 1,
              content: "我是第五个的第二个"
            },
            {
              tag: 2,
              content: "我是第五个的第三个"
            }
          ]
        }
      ]
    };
  },
  components: {}
};
</script>

<style scoped>
html {
    position: relative;
    text-align: center;
}
.time-content {
    position: absolute;
    left: 50%; 
    width: 300px;
    border-left: 1px dashed #000;
}
.content-detail {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
}

.content-detail p {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    width: 180px;
}

.content-detail p:first-child {
    color: aqua;
}

.font-icon {
    position: absolute;
    left: -10px;
}

/* .content-detail p:first-child::before {
    position: absolute;
    left: -12px;
    top: 12px;
    display: block;
    content: '';
    width: 20px;
    height: 20px;
    background-color: #fff;
    border: 2px solid #333;
    border-radius: 30px;
} */

.content-detail p span {
    padding: 20px 0;
    border-bottom: 1px dashed #000;
}

.content-detail p span:first-child {
    padding-top: 0;
}
</style>
