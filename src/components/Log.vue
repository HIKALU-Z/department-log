<template>
    <div>
        <!-- <table>
            <caption>
                <h1>阿水的阿里blog</h1>
            </caption>
            <tr>
                <th>name</th>
                <th>password</th>
                <th>goal</th>
            </tr>
            <tr>
                <th>xlj</th>
                <th colspan="2">001</th>
            </tr>
            <tr>
                <th>asa</th>
                <th rowspan="2">
                    <table border="1" width="800" bordercolor="blue">
                        <caption>
                            <h1>阿水的阿里blog</h1>
                        </caption>
                        <tr>
                            <th>name</th>
                            <th>password</th>
                            <th>goal</th>
                        </tr>
                        <tr>
                            <th>xlj</th>
                            <th colspan="2">001</th>
                        </tr>
                        <tr>
                            <th>asa</th>
                            <th rowspan="2">002</th>
                            <th>88</th>
                        </tr>
                        <tr>
                            <th>add</th>
                            <th>76</th>
                        </tr>
                    </table>
                </th>
                <th>88</th>
            </tr>
            <tr>
                <th>add</th>
                <th>76</th>
            </tr>
        </table> -->
        <div class="card">
            <h1 class="title">科室工作日志</h1>
            <form>
                <table class="table is-hoverable is-fullwidth is-bordered">
                    <tbody>
                        <!-- 患者流量开始 -->
                        <tr>
                            <th rowspan="3">患者流量</th>
                            <th rowspan="2" colspan="2">入院</th>
                            <th colspan="6">出院</th>
                            <th rowspan="2">留院</th>
                            <th rowspan="2">门诊</th>
                            <th rowspan="2">C型病例</th>
                            <th rowspan="2">D型病例</th>
                        </tr>
                        <tr>
                            <th>A型</th>
                            <th>B型</th>
                            <th>C型</th>
                            <th>D型</th>
                            <th>总数</th>
                            <th>住院总天数</th>
                        </tr>
                        <tr>
                            <td colspan="2">
                                <input type="date">
                            </td>
                            <td>
                                <input class="input-number" type="number" name="A" id="">
                            </td>
                            <td>
                                <input class="input-number" type="number" name="A" id="">
                            </td>
                            <td>
                                <input class="input-number" type="number" name="A" id="">
                            </td>
                            <td>
                                <input class="input-number" type="number" name="A" id="">
                            </td>
                            <td>
                                <input class="input-number" type="number" name="A" id="">
                            </td>
                            <td>
                                <input class="input-number" type="number" name="A" id="">
                            </td>
                            <td>
                                <input type="number" name="" id="">
                            </td>
                            <td>
                                <input type="number" name="" id="">
                            </td>
                            <td>
                                <input type="text">
                            </td>
                            <td>
                                <input type="text">
                            </td>
                        </tr>
                        <!-- 患者流量结束 -->
                        <!-- 临床路径开始 -->
                        <tr>
                            <th rowspan="2">临床路径</th>
                            <th colspan="3">应入病例</th>
                            <th colspan="3">实入病例</th>
                            <th colspan="3">退出病例</th>
                            <th colspan="3">完成病例</th>
                        </tr>
                        <tr>
                            <td colspan="3">
                                <input class="input-number" type="number">
                            </td>
                            <td colspan="3">
                                <input class="input-number" type="number">
                            </td>
                            <td colspan="3">
                                <input class="input-number" type="number">
                            </td>
                            <td colspan="3">
                                <input class="input-number" type="number">
                            </td>
                        </tr>
                        <!-- 临床路径结束 -->
                        <!-- 手术记录开始 -->
                        <tr>
                            <th rowspan="2">手术</th>
                            <th>I级别</th>
                            <th>II级别</th>
                            <th>III级别</th>
                            <th>IV级别</th>
                            <th>急诊</th>
                            <th>I类</th>
                            <th colspan="3">三级手术病例</th>
                            <th colspan="3">四级手术病例</th>
                        </tr>
                        <tr>
                            <td>
                                <input class="input-number" type="number">
                            </td>
                            <td>
                                <input class="input-number" type="number">
                            </td>
                            <td>
                                <input class="input-number" type="number">
                            </td>
                            <td>
                                <input class="input-number" type="number">
                            </td>
                            <td>
                                <input class="input-number" type="number">
                            </td>
                            <td>
                                <input class="input-number" type="number">
                            </td>
                            <td colspan="3">
                                <input class="input-number" type="text">
                            </td>
                            <td colspan="3">
                                <input class="input-number" type="text">
                            </td>
                        </tr>
                        <!-- 手术记录结束 -->
                        <tr>
                            <th rowspan="2">加班</th>
                            <th colspan="3">加班人员</th>
                            <th colspan="3">事由</th>
                            <th colspan="3">加班时间</th>
                            <th colspan="3">绩效分值</th>
                        </tr>
                        <tr>
                            <td colspan="3">
                                <Select v-model="model1" style="width:100%">
                                    <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
                                </Select>
                            </td>
                            <td colspan="3">
                                <input type="text">
                            </td>
                            <td colspan="3">
                                <input type="text">
                            </td>
                            <td colspan="3">
                                <input type="number">
                            </td>
                        </tr>
                    </tbody>
                </table>
            </form>
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      cityList: [
        {
          value: "New York",
          label: "张发智"
        },
        {
          value: "London",
          label: "张冠霖"
        },
        {
          value: "Sydney",
          label: "张二龙"
        },
        {
          value: "Ottawa",
          label: "张三林"
        },
        {
          value: "Paris",
          label: "王大陆"
        },
        {
          value: "Canberra",
          label: "陈先生"
        }
      ],
      model1: ""
    };
  }
};
</script>

<style lang="scss" scoped>
table {
  td:hover {
    background-color: rgba($color: rgb(95, 95, 235), $alpha: 0.15);
  }
  .input-number {
    width: 100%;
  }
  td {
    input {
      width: 100%;
    }
    select {
      width: 100%;
    }
  }
}
.card {
  padding: 20px;
  overflow: auto;
}
</style>
