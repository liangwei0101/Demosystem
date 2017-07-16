<template>
  <div class="layout">
    <Menu mode="horizontal" theme="dark" active-name="1">
      <div class="layout-nav">
        <Menu-item name="1">
          <Icon type="ios-analytics"></Icon>
          成交展示
        </Menu-item>
        <Menu-item name="2">
          <Icon type="ios-keypad"></Icon>
          数据导入
        </Menu-item>
        <Menu-item name="3">
          <Icon type="ios-navigate"></Icon>
          其他
        </Menu-item>
      </div>
    </Menu>
    <div class="layout-breadcrumb">
      <Breadcrumb>
        <Breadcrumb-item href="#">首页</Breadcrumb-item>
        <Breadcrumb-item href="#">应用中心</Breadcrumb-item>
        <Breadcrumb-item>某应用</Breadcrumb-item>
      </Breadcrumb>
    </div>
    <div class="layout-content">
    </div>
    <div class="layout-copy">
      2017 &copy; liangwei
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        columns1: [
          {
            title: '姓名',
            key: 'name'
          },
          {
            title: '年龄',
            key: 'age'
          },
          {
            title: '地址',
            key: 'address'
          }
        ],
        columns9: [
          {
            title: '姓名',
            key: 'name'
          },
          {
            title: '年龄',
            key: 'age',
            className: 'demo-table-info-column'
          },
          {
            title: '地址',
            key: 'address'
          }
        ],
        data1: [
          {
            name: '王小明',
            age: 18,
            address: '北京市朝阳区芍药居'
          },
          {
            name: '张小刚',
            age: 25,
            address: '北京市海淀区西二旗'
          },
          {
            name: '李小红',
            age: 30,
            address: '上海市浦东新区世纪大道'
          },
          {
            name: '周小伟',
            age: 26,
            address: '深圳市南山区深南大道'
          }
        ],
        data8: [
          {
            name: '王小明',
            age: 18,
            address: '北京市朝阳区芍药居'
          },
          {
            name: '张小刚',
            age: 25,
            address: '北京市海淀区西二旗',
            cellClassName: {
              age: 'demo-table-info-cell-age',
              address: 'demo-table-info-cell-address'
            }
          },
          {
            name: '李小红',
            age: 30,
            address: '上海市浦东新区世纪大道'
          },
          {
            name: '周小伟',
            age: 26,
            address: '深圳市南山区深南大道',
            cellClassName: {
              name: 'demo-table-info-cell-name'
            }
          }
        ]
      }
    },
    methods: {
      rowClassName (row, index) {
        if (index === 1) {
          return 'demo-table-info-row'
        } else if (index === 3) {
          return 'demo-table-error-row'
        }
        return ''
      }
    }
  }
</script>
<style>
  .layout{
    border: 1px solid #d7dde4;
    background: #f5f7f9;
  }
  .layout-nav{
    width: 420px;
    margin: 0 auto;
  }
  .layout-assistant{
    width: 300px;
    margin: 0 auto;
    height: inherit;
  }
  .layout-breadcrumb{
    padding: 10px 15px 0;
  }
  .layout-content{
    min-height: 200px;
    margin: 15px;
    overflow: hidden;
    background: #fff;
    border-radius: 4px;
  }
  .layout-copy{
    text-align: center;
    padding: 10px 0 20px;
    color: #9ea7b4;
  }
</style>
