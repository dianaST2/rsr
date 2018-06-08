<template>
  <f7-page>
    <f7-block-title>Left Panel</f7-block-title>
    <f7-block>
      <p>Это левая боковая панель. Вы можете закрыть её кликнув: <f7-link panel-close>close me</f7-link></p>
    </f7-block>
    <f7-block-title>Меню</f7-block-title>
    <f7-list>
      <f7-list-item link="/about/" title="About" panel-close></f7-list-item>
      <f7-list-item link="/form/" title="Form" panel-close></f7-list-item>
      <f7-list-item link="/events/" title="Events" panel-close></f7-list-item>
    </f7-list>
    <f7-block>
      <p></p>
    </f7-block>
  </f7-page>
</template>
<script>
  export default {
  };
</script>
