<template>
    <div class="card">
        <div class="content">
            <h2>患者流量</h2>
        </div>
        <form @submit.prevent="handleSubmit">
            <div class="field">
                <label class="label" for="inNum">入院人数</label>
                <div class="control">
                    <input class="input" name="in" type="number" placeholder="请输入数字" v-model="current.inNum">
                </div>
                <!-- <p class="help is-danger">人数必须是数字</p> -->
            </div>

            <div class="field">
                <label class="label" for="outNum">出院人数</label>
                <div class="control">
                    <input class="input" name="out" type="number" placeholder="请输入数字" v-model="current.outNum">
                </div>
            </div>

            <div class="field">
                <div class="control">
                    <button type="submit" class="button is-info">提交</button>
                </div>
            </div>
        </form>
        <hr>
        <div class="content" v-cloak>
            <ul>
                <li>入院：{{totalIn}}</li>
                <li>出院：{{totalOut}}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      // 表单对象
      current: {
        inNum: null,
        outNum: null
      },
      // 累加数组
      arr: []
    };
  },
  methods: {
    handleSubmit() {
      // 如何把解构赋值后的值直接赋给一对象
      let obj = Object.assign({}, this.current);
      this.arr.push(obj);
      this.current = {};
      console.log(this.arr);
    }
  },
  computed: {
    totalIn() {
      let sumIn = 0;
      this.arr.forEach(item => {
        sumIn += parseInt(item.inNum);
      });
      return sumIn;
    },
    totalOut() {
      let sumOut = 0;
      this.arr.forEach(item => {
        sumOut += parseInt(item.outNum);
      });
      return sumOut;
    }
  }
};
</script>

<style scoped>
.card {
  padding: 20px;
}
</style>
