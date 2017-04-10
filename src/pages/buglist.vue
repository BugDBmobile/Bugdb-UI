<template>
    <div class="bug-view">
    <f7-searchbar cancel-link="Cancel" search-list="#bug-list"
    @searchbar:search="onSearch" @searchbar:enable="onEnable"
    @searchbar:disable="onDisable" @searchbar:clear="onClear">
    <div slot="before-input"  >
       <select name="searchType">
       <option value="bugId" selected>bugId</option>
       <option value="bugText">bugText</option>
      </select>
    </div>
    </f7-searchbar>
    <f7-list class="searchbar-not-found">
        <f7-list-item title="Nothing found"></f7-list-item>
     </f7-list>
    <f7-list media-list class="searchbar-found" id="bug-list">
      <f7-list-item link="/form/"
        v-for="n in items"
        :key="n"
        :title="'bugId: ' + n "
        :subtitle="'submited Time ' + n"
        :media="'<img src=\'http://lorempixel.com/160/160/people/' + n%10 + '\' width=\'80\'>'"
        text="bugsubject"
        :data="n"
        badge="5" badge-color="red"
      ></f7-list-item>
      <!-- 加载提示符 -->
      <div id="list-pre" class="infinite-scroll-preloader" v-show="showPreloader">
        <div class="preloader"></div>
      </div>
    </f7-list>

    <!--infinite-scroll @infinite="onInfinite"
        <card v-for="(item, index) in timeline" :key="item.id" :data="item" @card:content-click="routeToPost"></card>
      -->
      </div>
</template>
<style>
    .infinite-scroll-preloader {
      margin-bottom: 1px;
      text-align: center;
    }
    .infinite-scroll-preloader .preloader {
      width:34px;
      height:34px;
    }
</style>
<script>
var timeout;
export default {
  data: function () {
    return {
      counter: 6,
      items: [1,2,3,4,5,6],
      showPreloader:false
    }
  },
  props :['userId'],
  methods: {
      loadOrg: function (){
        this.showPreloader = true;
        console.log("working loadorg");
        var self = this;
        clearTimeout(timeout);
        timeout = setTimeout(function () {
          for (var i = self.counter; i < self.counter + 3; i++) {
            self.items.push(i);
          }
          self.counter = i;
          this.showPreloader = false;
        }, 1000);
      },
      onSearch: function (query, found) {
        console.log('search', query);
      },
      onClear: function (event) {
        console.log('clear');
      },
      onEnable: function (event) {
        console.log('enable');
      },
      onDisable: function (event) {
        console.log('disable');
      },
      getBugInfo(data) {
          this.$f7.mainView.router.load({url:`/form/?bugId=${data}`});
        }
      }
}
</script>
