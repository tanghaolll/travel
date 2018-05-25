<template>
 <div>
    <table border="1" width="500px" style="height: 400px;margin-right: 200px;">
      <tr>
        <th>颜色分类</th>
        <td>尺寸</td>
      </tr>
      <template v-for="item in dataList">
        <tr>
          <td :rowspan="item.ptSpecificationValueData.length">{{item.ptSpecificationName}}</td>
          <td>{{item.ptSpecificationValueData[0].ptSpecificationValueValue}}</td>
        </tr>
        <tr v-for="son in item.ptSpecificationValueData.length-1">
          <td >{{item.ptSpecificationValueData[son].ptSpecificationValueValue}}</td>
        </tr>
      </template>

    </table>
  </div>
</template>

<script>
export default {
  name: 'DemoTable',
  data() {
      return {
        dataList: [
          {
            "ptSpecificationId": "1111",
            "ptSpecificationName": "红色",
            "ptSpecificationValueData": [
              {
                "ptSpecificationValueId": "sadasd",
                "ptSpecificationValueValue": "1",
              },
              {
                "ptSpecificationValueId": "1239977",
                "ptSpecificationValueValue": "2",
              }
              ,
              {
                "ptSpecificationValueId": "1239977",
                "ptSpecificationValueValue": "3",
              }
            ]
          },
          {
            "ptSpecificationId": "1111",
            "ptSpecificationName": "蓝色",
            "ptSpecificationValueData": [
              {
                "ptSpecificationValueId": "sadasd",
                "ptSpecificationValueValue": "11",
              },
              {
                "ptSpecificationValueId": "1239977",
                "ptSpecificationValueValue": "22",
              },
              {
                "ptSpecificationValueId": "1239977",
                "ptSpecificationValueValue": "33",
              }
              ,
              {
                "ptSpecificationValueId": "1239977",
                "ptSpecificationValueValue": "44",
              }
              ,
              {
                "ptSpecificationValueId": "1239977",
                "ptSpecificationValueValue": "55",
              }
            ]
          }
        ]

      }
    },
    components: {},
    methods: {
      objectSpanMethod({row, column, rowIndex, columnIndex}) {

      }
    }
}
</script>

<style>

</style>
