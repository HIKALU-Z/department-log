<template>
    <div class="card">
        <ul>
            <li>
                <router-link to="/admin/sick">患者流量</router-link>
            </li>
            <li>
                <router-link to="/admin/sss">手术管理</router-link>
            </li>
            <li>
                <router-link to="/admin/zzz">重点监控</router-link>
            </li>
        </ul>
    </div>
</template>

<script>
export default {};
</script>

<style lang='scss' scoped>
li > a {
  color: #777777;
  display: block;
  padding: 10px 20px;
  transition: all 0.3s ease-in-out;
  &:hover {
    background-color: rgba($color: rgb(10, 94, 221), $alpha: 0.15);
    color: #000000;
  }
  &.router-link-active {
    border-left: 3px solid rgb(178, 9, 245);
    color: #ee681b;
    font-weight: bold;
    // background-color: rgba($color: rgb(214, 21, 63), $alpha: 0.15);
  }
}
</style>
