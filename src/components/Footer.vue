<template>
  <footer class='footer has-text-centered'>
    <nav class='level'>
      <div class='level-left'>
        <div class='level-item' style="display: flex; flex-direction: column; align-items: flex-start;">
          <span>from lolo to coco</span>
          <span>to wish her the happiest birthday</span>
          
        </div>
      </div>
    </nav>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
.footer {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  padding: 0.3rem 0;
  font-size: 0.9rem;
  background: #fafafa;
  border-top: 1px solid #eaeaea;
  z-index: 100;
}
.footer .level {
  margin-bottom: 0;
}
</style>
