<template>
  <div class="footer-wrapper">
    <div class="footer-content">
      <div class="footer-left left">
        <ul class="footer-info left">
          <h2>会员体系</h2>
          <li>
            <router-link :to="{ path: '/homeVip' }">会员体系</router-link>
          </li>
          <li>
            <router-link :to="{ path: '/rightVip' }">会员权益</router-link>
          </li>
        </ul>
        <ul class="footer-info right">
          <h2>仓豆商城</h2>
          <li>
            <router-link :to="{ path: '/homeMall' }">商品首页</router-link>
          </li>
        </ul>
      </div>
      <div class="footer-middle left">
        <div class="item left">
          <img src="./app-download.png" alt="下载" width="80" height="80"/>
          <h2>下载钱满仓APP</h2>
        </div>
        <div class="item right">
          <img src="./qmc-wx-2wm.png" alt="二维码" width="80" height="80">
          <h2>关注我们</h2>
        </div>
      </div>
      <div class="footer-right left">
        <h1>400-135-1766</h1>
        <p class="zhiCustomBtn">在线客服</p>
        <h3>客服热线（工作时间：09:00-21:00）</h3>
      </div>
      <div class="footer-bottom">
        京ICP备14053053号−1 / @2017 北京佛尔斯特金融信息服务有限公司 / 京公网安备 11010102002289号

      </div>
    </div>
  </div>
</template>
<script>
  export default{
    methods: {
      enter(){
        this.$refs.encryption.style.cssText = 'opacity:1;z-index:1;';
      },
      leave(){
        setTimeout(() => {
          this.$refs.encryption.style.cssText = 'opacity:0;z-index:-1;';
        }, 3000);
      }
    },
    mounted() {
      const s = document.createElement('script');
      s.type = 'text/javascript';
      s.src = 'https://www.sobot.com/chat/frame/js/entrance.js?sysNum=621c96e39127438091fdaa6f75741e9b';
      s.className = "zhiCustomBtn";
      s.id = "zhichiScript";
      s.setAttribute('data-args', 'customBtn=true')
      document.body.appendChild(s);
    },
  };
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "footer.styl";
</style>

