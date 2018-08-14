<template>
    <nav class="navbar is-link">
        <div class="navbar-brand">
            <router-link to="/" class="navbar-item">
                <img src="./../assets/image/logo.png" alt="Bulma: a modern CSS framework based on Flexbox" width="112" height="28">
            </router-link>
            <div class="navbar-burger burger" data-target="navbarExampleTransparentExample">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>

        <div id="navbarExampleTransparentExample" class="navbar-menu">
            <div class="navbar-start">
                <router-link class="navbar-item" to="/">
                    首页
                </router-link>
                <div class="navbar-item has-dropdown is-hoverable">
                    <a class="navbar-link">
                        日志录入
                    </a>
                    <div class="navbar-dropdown is-boxed">
                        <router-link to='/admin/sick' class="navbar-item" href="#">
                            患者流量
                        </router-link>

                        <hr class="navbar-divider">

                        <a class="navbar-item is-active" href="#">
                            统计
                        </a>
                    </div>
                </div>
            </div>

            <!--  <div class="navbar-end">
                <div class="navbar-item">
                    <div class="field is-grouped">
                        <p class="control">
                            <a class="bd-tw-button button" data-social-network="Twitter" data-social-action="tweet" data-social-target="http://localhost:4000" target="_blank" href="https://twitter.com/intent/tweet?text=Bulma: a modern CSS framework based on Flexbox&amp;hashtags=bulmaio&amp;url=http://localhost:4000&amp;via=jgthms">
                                <span class="icon">
                                    <i class="fab fa-twitter"></i>
                                </span>
                                <span>
                                    Tweet
                                </span>
                            </a>
                        </p>
                        <p class="control">
                            <a class="button is-primary" href="https://github.com/jgthms/bulma/releases/download/0.7.1/bulma-0.7.1.zip">
                                <span class="icon">
                                    <i class="fas fa-download"></i>
                                </span>
                                <span>Download</span>
                            </a>
                        </p>
                    </div>
                </div>
            </div> -->
        </div>
    </nav>
</template>

<script>
export default {
  data() {
    return {
      theme: "dark"
    };
  }
};
</script>

<style scoped>
</style>
