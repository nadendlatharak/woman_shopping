<template>
  <div class="header_bar">
    <div class="header_pages">
      <div class="navigation_pages">
        <div>New Launch</div>
        <div>Top Wear</div>
        <div>Bottom Wear</div>
        <div>Cosmetics</div>
        <div>Foot Wear</div>
        <div>Wish Ful</div>
        <div>Plus Members</div>
        <div>Sale</div>
     </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .header_bar{
    margin:0px;
    width: auto;
    height: 80px;
    background-color: rgb(232, 232, 252);
    display: flex;
    position:relative;
  }

  .header_pages{
    flex: 2;
    display: flex;
    align-items: center;
    /* justify-content: center; */
    /* align-items: center; */
    /* justify-content: space-between; */
  }

  .navigation_pages{
    display: flex;
    /* align-items: center; */
    /* justify-content: space-between; */
    align-items: space-between;
  }

  .navigation_pages div {
    margin-left: 24px ;
  }


</style>
