<template>
  <form method="post" class="new-comment">
      <slot></slot>
      <textarea name="comment-content" placeholder="写下你的评论" v-model="value">
        
      </textarea>
      <div class="write-function-block">
        <div class="emoji-modal-wrap">
         <a class="emoji" @click="emojiShow($event)">
          <i class="fa fa-smile-o"></i>
         </a>
         <transition name="emoji">
        <div class="emoji-modal" v-show="isShow">
          <vue-emoji @select="selectEmoji"></vue-emoji>
        </div>
        </transition>
      </div>
      <div class="hint">Ctrl+Enter发表</div>
      <a href="#" class="btn-send">发送</a>
      <a href="#" class="btn-cancel">取消</a>
      </div>
    </form>
</template>
<script>
import vueEmoji from '~/components/emoji.vue'
export default {
  name:'myForm',
  data(){
      return{
        isShow:false,
        value:'',
        data:[]
      }
  },
  methods:{
    selectEmoji (code) {
      this.value += code
    },
    submit () {
      this.data.push(this.value)
      this.value = ''
    },
    emojiShow(e){
      this.isShow=!this.isShow;
      e.stopPropagation();
    }
  },
  components:{
    vueEmoji
  },
  mounted(){
    document.addEventListener('click', (e) => {
      this.isShow= false;
    })
  }
}
</script>
<style scoped>
.comment-list .new-comment {
  position: relative;
  margin: 0 0 20px 56px;
}
.comment-list .new-comment .avatar {
  width: 38px;
  height: 38px;
  position: absolute;
  left: -48px;
  display: inline-block;
  margin-right: 10px;
}
.comment-list .new-comment textarea {
  padding: 10px 15px;
  width: 100%;
  height: 80px;
  outline: none;
  resize: none;
  display: inline-block;
  font-size: 13px;
  border: 1px solid #dcdcdc;
  background: #f7f7f7;
  border-radius: 4px;
  vertical-align: top;
}
.comment-list .new-comment .write-function-block {
  height: 50px;

}
.comment-list .new-comment .write-function-block .emoji-modal-wrap{
  position: relative;
}
.comment-list .new-comment .write-function-block .emoji {
  float: left;
  margin-top: 14px;
}
.comment-list .new-comment .write-function-block .emoji i {
  font-size: 20px;
  color: #969696;
}
.comment-list .new-comment .write-function-block .emoji i:hover {
  color: #2f2f2f;
}
.comment-list .new-comment .write-function-block .hint {
  float: left;
  margin: 18px 0 0 20px;
  font-size: 13px;
  color: #969696;
}
.comment-list .new-comment .write-function-block .btn-send {
  float: right;
  width: 78px;
  padding: 8px 18px;
  margin: 10px 0;
  background: #42c02e;
  display: block;
  outline: none;
  color: #fff;
  font-size: 16px;
  text-align: center;
  border-radius: 100px;
}
.comment-list .new-comment .write-function-block .btn-send:hover {
  background: #3db922;
}
.comment-list .new-comment .write-function-block .btn-cancel {
  float: right;
  margin: 18px 30px 0 0;
  color: #969696;
  font-size: 16px;
}
.comment-list .new-comment .write-function-block .emoji-modal{
  position: absolute;
  border: 1px solid #ddd;
  top: 50px;
  left: -56px;
  /* overflow: hidden; */
  height: 241px;
  width:382px;
  border-radius: 4px;
  z-index: 1000;
}
.comment-list .new-comment .write-function-block .emoji-modal:before{
  content: '';
  width: 15px;
  height: 15px;
  border-top: 1px solid #ddd;
  border-left: 1px solid #ddd;
  background: #eee;
  position: absolute;
  top: -8px;
  left: 57px;
  transform: rotate(45deg);
}
.comment-list .new-comment .write-function-block .emoji-modal .emoji{
  margin: 0;
  padding: 0;
}
.emoji-enter-active, .emoji-leave-active {
  transition: all .3s;
  transform: translateY()(0);
}
.emoji-enter, .emoji-leave-to  {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
