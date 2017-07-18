<template>
  <div class=page>
    <header>
      <Topbar/>
    </header>
    <main>
      <ResumeEditor/>
      <ResumePreview/>
    </main>
  </div>
</template>

<script>
//css
import './assets/reset.css'
import 'normalize.css/normalize.css'

//
import Topbar from './components/Topbar'
import ResumeEditor from './components/ResumeEditor'
import ResumePreview from './components/ResumePreview'


export default {
  name: 'app',
  data: function () {
    return {
      text: '你好'
    }
  },
  components: {
    Topbar,
    ResumeEditor,
    ResumePreview
  }
}
</script>

<style>
.page {
  height: 100vh;/*相对于视窗的高度：视窗高度是100vh*/
  display: flex;
  flex-direction: column;/*导航栏和内容按列上下排*/
  background: #EAEBEC;
  
}

.page>main {
  flex-grow: 1; /*占据所有剩余空间*/
}

.page>main {
  min-width: 1024px;
  max-width: 1440px;
  margin-top: 16px;
  margin-bottom: 16px;
  display: flex;/*内容按默认左右排列*/
  justify-content: space-around;/*元素位于各行之前、之间、之后都留有空白的容器内*/
   width: 100%;/*不写100%,内容会往中间缩小.*/  
   align-self: center; /*align-self 属性定义flex子项单独在侧轴（纵轴）方向上的对齐方式,元素位于容器的中心*/
}

#resumeEditor {
  width: 35%;
  background: #444;
}

#resumePreview {
  width: 61.66667%;/**/
  background: #777;
}
</style>