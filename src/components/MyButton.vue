<body>
  <html>
  <div id="bind-attribute">
  <span v-bind:title="message">
    鼠标悬停几秒钟查看此处动态绑定的提示信息！ {{msg}}
  </span>
  </div>

  </html>
</body>

<script>


export default {
  name: 'MyButton',
  props: {
    msg: String
  }
}
</script>