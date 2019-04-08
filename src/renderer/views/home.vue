<style scoped>
  .layout{
    background: #f5f7f9;
    position: relative;
    border-radius: 4px;
    overflow: hidden;
  }
  .layout-header-bar{
    background: #fff;
    box-shadow: 0 1px 1px rgba(0,0,0,.1);
  }

</style>
<template>
  <div class="layout">

    <div style="position: fixed; height: 20px;width:100%;overflow: hidden;background-color: #1f292e;
        display: flex; justify-content: space-between;align-items: center;  -webkit-app-region: drag">
      <div> </div><div style="color:white">神州浩天监控平台 1.0</div>
      <div style="display: flex;padding-right: 30px; width:130px;flex-direction: row;justify-content: space-between;">
        <div style=" width:16px;height: 16px ;background-color: red;border-radius: 8px"></div>
        <div style=" width:16px;height: 16px ;background-color:yellow ;border-radius: 8px"></div>
        <div style=" width:16px;height: 16px ;background-color: green;border-radius: 8px"></div>
      </div>
    </div>

    <Sider :style="{position: 'fixed',marginTop:'20px', height: '100vh', left: 0, overflow: 'auto'}">
      <Menu active-name="1-2" theme="dark" width="auto" :open-names="['1']">
        <Submenu name="1">
          <template slot="title">
            <Icon type="ios-navigate"></Icon>
            Item 1
          </template>
          <MenuItem name="1-1">Option 1</MenuItem>
          <MenuItem name="1-2">Option 2</MenuItem>
          <MenuItem name="1-3">Option 3</MenuItem>
        </Submenu>
        <Submenu name="2">
          <template slot="title">
            <Icon type="ios-keypad"></Icon>
            Item 2
          </template>
          <MenuItem name="2-1">Option 1</MenuItem>
          <MenuItem name="2-2">Option 2</MenuItem>
        </Submenu>
        <Submenu name="3">
          <template slot="title">
            <Icon type="ios-analytics"></Icon>
            Item 3
          </template>
          <MenuItem name="3-1">Option 1</MenuItem>
          <MenuItem name="3-2">Option 2</MenuItem>
        </Submenu>
      </Menu>
    </Sider>
    <Layout :style="{marginLeft: '200px'}">
      <Header :style="{background: '#fff', boxShadow: '0 2px 3px 2px rgba(0,0,0,.1)'}"></Header>
      <Content :style="{padding: '0 16px 16px'}">
        <Breadcrumb :style="{margin: '16px 0'}">
          <BreadcrumbItem>Home</BreadcrumbItem>
          <BreadcrumbItem>Components</BreadcrumbItem>
          <BreadcrumbItem>Layout</BreadcrumbItem>
        </Breadcrumb>

          <div style="height: 600px">Content</div>

      </Content>
    </Layout>

  </div>
</template>
<script>
  export default {

  }
</script>
