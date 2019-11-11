<!--
 * @Author: wang cai-hong
 * @Date: 2019-11-11 09:42:56
 -->
<template>
  <div class="time">
    <div class="text-content">
      <h2 class="text-center">Vue时间轴demo</h2>
      <div class="time-line">
        <div v-for="item in testList" class="time-line-div" :key="item.key">
          <p>{{item.time}}</p>
          <p ref="circular"></p>
          <p>
             <span v-for="con in item.texts" :key="con.tag" style="display: flex; flex-column: column; justify-content: flex-start; align-items: center; border-bottom: 1px dashed #fff; margin-bottom: 2   0px; padding: 10px">
                  {{con.content}}
             </span>
          </p>
        </div>
        <div class="img-dotted" ref="dotted"></div>
      </div>
      <div style="margin-top:20px;"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TimeLine",
  data() {
    return {
      testList: [
        {
          key: "1",
          time: "2001-01-01 01:00:00",
          texts: [ 
            {
              tag: 0,
              content: "我是第一个的第一个我是第一个的第一个我是第一个的第一个我是第一个的第一个我是第一个的第一个我是第一个的第一个"
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
  mounted() {
    this.$refs.dotted.style.left =
      this.$refs.circular[0].offsetLeft - 12 + "px";
  },
  components: {}
};
</script>

<style scoped>

.text-center{
	text-align: center;
}
.time h2{
	color:#FF6600;
	margin: 20px auto 30px auto;
}
.time-line{
	position: relative;
	width:300px;
	margin:0 auto;
}
.time-line-div{
	position:relative;
	min-height:85px;
}
.time-line-div>p:nth-child(1){
	position: absolute;
	left:0;
	width:100px;
}
.time-line-div>p:nth-child(2){
	position:absolute;
	left: 100px;
	width:15px;
	height:15px;
	top:10px;
	background:#5CB85C;
	border-radius: 50%;
	z-index: 10
}
.time-line-div>p:nth-child(3){
	position:absolute;
	left: 130px;
    width: 140px;
    height: 60px;   
	padding: 10px;
	background: #317EF3;
	font-size:.8rem;
	color:#fff;
	border-radius: 10px;
    overflow-y: auto;


    scrollbar-arrow-color: #317EF3;
    scrollbar-face-color: #fff; /**//*立体滚动条的颜色*/ 
    /* scrollbar-3dlight-color: #666; 立体滚动条亮边的颜色  */
    scrollbar-highlight-color: #fff; /**//*滚动条空白部分的颜色*/ 
    scrollbar-shadow-color: #fff; /**//*立体滚动条阴影的颜色*/ 
    scrollbar-darkshadow-color: #fff; /**//*立体滚动条强阴影的颜色*/ 
    scrollbar-track-color: #fff; /**//*立体滚动条背景颜色*/ 
    scrollbar-base-color:#fff; /**//*滚动条的基本颜色*/ 
}

.time-line-div>p:nth-child(3)::-webkit-scrollbar {
    width:4px;
    background-color: #fff;
}

.time-line-div>p:nth-child(3)::-webkit-scrollbar-track {
    border-radius:10px;
    margin: 2px 0;
}

.time-line-div>p:nth-child(3)::-webkit-scrollbar-thumb {
    border-radius:10px;
    background: #317EF3;
}

.img-dotted{
	position:absolute;
	width:20px;
	height:100%;
	top:0;
	z-index: 1;
	background:url('/static/dotted.png');
}
</style>
