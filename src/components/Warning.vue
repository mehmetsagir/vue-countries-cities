<template>
    <div class="warning">
      <h3>Warning</h3>
      <ul>
        <li>There may be errors in the country and city names listed.</li>
        <li>Sorry, some countries' cities may be missing.</li>
        <li>I plan to resolve these types of problems over time.</li>
      </ul>
    </div>
</template>

<style lang="scss" scoped>
.warning{
  padding: 15px;
  background: #FFCC00 ;
  border-radius: 5px;
  h3{
    font-size: 25px;
  }
  ul{
    margin-left: 20px;
    li:last-child{
      list-style: none;
      color: #EF1716;
      font-weight: bold;
    }
  }
}
</style>