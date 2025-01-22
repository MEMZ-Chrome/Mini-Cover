<template>
  <footer>
      <button class="logo-btn" @click="toggleTips">小提示</button>
    </div>
  </footer>
  <div class="tips-popup" :class="{ 'show': showTipsPopup }">
    <div class="popup-content">
      <span>为避免性能问题，建议不要连续做图</span>
      <span>建议经常<a href="/">刷新页面</a>优化性能</span>
      <span class="highlight"><strong>重要提示：请确保您的浏览器和设备性能良好</strong></span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showTipsPopup: false,
      icpNumber: import.meta.env.VITE_APP_ICP_NUMBER
    };
  },
  methods: {
    toggleTips() {
      this.showTipsPopup = !this.showTipsPopup;

      if (this.showTipsPopup) {
        setTimeout(() => {
          this.showTipsPopup = false;
        }, 3000);
      }
    }
  }
};
</script>
