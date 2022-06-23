<template>
  <div>
    <h1> Table View</h1>

    <el-row :gutter="40" type="flex" class="row-bg" justify="center">

      <el-col style='background-color:red' :span="2">
        bla bla
      </el-col>
      <el-col style='background-color:rgba(200,240,240,240)' :span="18">

        <el-table v-loading=loading :data="tableData" style="width: 100%">

          <el-table-column prop="date" label="Minha Data" width="180">
          </el-table-column>

          <el-table-column prop="name" label="Nome" width="180">
          </el-table-column>

          <el-table-column prop="address" label="Endereço" width="180">
          </el-table-column>

        </el-table>
        <el-pagination background layout="prev, pager, next" :total="1000">
        </el-pagination>
      </el-col>
      <el-col style='background-color:red' :span="2">ble</el-col>

    </el-row>

    <el-row :gutter="40" type="flex" class="row-bg" justify="center">

      <ul id="example-1">
        <li v-for="item in tableData" :key="item.name">
          <div style=''>
            {{ item.name }},{{ item.date }}
          </div>
        </li>
      </ul>

    </el-row>

  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "TableView",
  data: function () {
    return {
      count: 0,
      loading: false,
      tableData: [],
    };
  },
  mounted() {
    var self = this;
    console.log("mounted");
    this.loading = true;

    setTimeout(
        
        function () {
      self.tableData = [
        {
          date: "2016-05-03",
          name: "Tom",
          address: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          name: "Tom",
          address: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          name: "Tom",
          address: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          name: "Tom",
          address: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          name: "Tom",
          address: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          name: "Tom",
          address: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          name: "Tom",
          address: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          name: "Tom",
          address: "No. 189, Grove St, Los Angeles",
        },
        {
          date: "2016-05-03",
          name: "Tom",
          address: "No. 189, Grove St, Los Angeles",
        },
      ];
      self.loading = false;
    }, 1000);
  },
};
</script>
