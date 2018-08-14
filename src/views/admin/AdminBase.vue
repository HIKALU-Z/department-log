<template>
    <div>
        <Nav></Nav>
        <main class="container">
            <div class="columns">
                <div class="column is-2">
                    <AdminNav></AdminNav>
                </div>
                <div class="column is-10">
                    <router-view></router-view>
                </div>
            </div>
        </main>
        <Footer></Footer>
    </div>
</template>

<script>
const Nav = () => import("@/components/Nav.vue");
const Footer = () => import("@/components/Footer.vue");
const AdminNav = () => import("@/components/admin/AdminNav.vue");
export default {
  components: {
    Nav,
    AdminNav,
    Footer
  }
};
</script>

<style scoped>
main {
  padding: 30px 0;
}
</style>
