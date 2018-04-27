<template>
   <div>
                                <ul class="share-list">
                                        <li>
                                            <i class="fa fa-star" style="color:#eebf13"></i>
                                            分享到QQ空间
                                        </li>
                                        <li>
                                            <i class="fa fa-twitter" style="color:#00aaec"></i>
                                            分享到Twitter
                                        </li>
                                        <li>
                                            <i class="fa fa-facebook-official" style="color:#4460a0"></i>
                                            分享到Facebook
                                        </li>
                                        <li>
                                            <i class="fa fa-google-plus" style="color:#f9402e"></i>
                                            分享到Google+
                                        </li>
                                        <li>
                                            <i class="fa fa-github" style="color:#3f902d"></i>
                                            分享到豆瓣
                                        </li>
                                    </ul>
                                </div>
</template>
<script>
export default {
  name: "moreShare",
  data() {
    return {};
  }
};
</script>
<style scoped>
 .share-list li{
    line-height: 32px;
    height: 32px;
    font-size: 16px;
    padding: 0 7px;
    background-color: white;
    
}
.share-list li:hover{
    background: #ddd;
}
.share-list:after{
    content: '';
    width: 10px;
    height: 10px;
    border-left: 2px solid #ddd;
    border-bottom: 2px solid #ddd;
    transform: rotate(-45deg);
    background-color: white;
    position: absolute;
    top: 156.5px;
    left: 65px;

}


</style>

