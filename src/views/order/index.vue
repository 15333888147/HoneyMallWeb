<template>
  <div class="app-container">
    <el-button type="primary">新增</el-button>

    <el-table :data="userList" style="width: 100%;margin-top:30px;" border>
      <el-table-column align="center" width="220" prop="id" label="编号" />
      <el-table-column align="center" width="220" prop="name" label="姓名" />
      <el-table-column align="header-center" width="220" prop="phone" label="手机号" />
      <el-table-column align="center" label="操作">
        <template slot-scope="scope">
          <el-button type="primary" size="small" @click="handleEdit(scope)">修改</el-button>
          <el-button type="danger" size="small" @click="handleDelete(scope)">删除</el-button>
        </template>
      </el-table-column>
    </el-table>

  </div>
</template>

<script>

export default {
  name: 'Order',
  data() {
    return {
      userList: []
    }
  },
  mounted() {
    this.userListFunction()
  },
  methods: {
    userListFunction() {
      this.userList = [{ id: 1, name: '测试', phone: '1524214567' }, { id: 2, name: '测试', phone: '1524214567' }, { id: 3, name: '测试', phone: '1524214567' }]
    }
  }
}
</script>
