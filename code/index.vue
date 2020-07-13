<template>
  <div class="mod">
    <div class="hd">
      <div class="group">
        <img
          class="icon"
          src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/52c30bd0c1bf11ea95741b4db311ea49.png"
        />
        <img
          class="icon_2"
          src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/52939760c1bf11ea85d17108e1cf46aa.png"
        />
      </div>
      <span class="txt" :lines="1">4:21 PM</span>
      <div class="block">
        <div class="container"><div class="color" /></div>
        <img
          class="dot"
          src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/524661c0c1bf11ea97b3bba7a94e78d8.png"
        />
      </div>
    </div>
    <div class="bd">
      <div class="group_2">
        <img
          class="img"
          src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/53034920c1bf11eab8dae12435ac7b24.png"
        />
      </div>
      <span class="word" :lines="1">爱豆主页</span>
      <img
        class="icon_3"
        src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/5322df10c1bf11ea8c2f9bd01ca09a08.png"
      />
    </div>
    <div class="main">
      <img
        class="layer"
        src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/536e6700c1bf11ea804f9bc89db4bfb9.png"
      />
      <div class="block_3">
        <img
          class="largeIcon"
          src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/53ad1db0c1bf11ea9b3c37aa03fbe4d5.png"
        />
        <div class="block_2">
          <img
            class="avator"
            src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/53ef08b0c1bf11eab09ddd512a80cce6.png"
          />
          <div class="outer">
            <span class="info" :lines="1">莫尼卡·贝鲁奇</span>
            <span class="text" :lines="1">粉丝：98767868709</span>
            <div class="tagWrap">
              <span class="tag" :lines="1">已加入</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="submain"
      :position-nav="top"
      :is-scroll="false"
      :is-show-line="true"
    >
      <div class="empty" :lines="1" :content="goods" />
      <div class="div" :lines="1" />
      <span class="text_2" :lines="1">排名</span>
    </div>
    <div class="ft" :finished="false">
      <div class="row1" :title="02">
        <div class="group_3">
          <img
            class="icon_4"
            src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/51ca53f0c1bf11eaad21171147243346.png"
          />
          <img
            class="icon_5"
            src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/519b54b0c1bf11eaa8363f05c9fbc4ae.png"
          />
          <span class="brianRodriguez" :lines="1">Brian Rodriguez</span>
        </div>
        <span class="price" :lines="1">¥1678,89</span>
      </div>
      <div class="row2" :title="01">
        <div class="container_2">
          <img
            class="icon_6"
            src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/52212680c1bf11ea8c3c31a19300e71c.png"
          />
          <img
            class="icon_7"
            src="https://ai-sample.oss-cn-hangzhou.aliyuncs.com/test/51f7cc90c1bf11eaa2349b1fb7c7c18e.png"
          />
          <span class="brianRodriguez_2" :lines="1">Brian Rodriguez</span>
        </div>
        <span class="money" :lines="1">¥1678,89</span>
      </div>
    </div>
  </div>
</template>
<script>
import { fetch } from 'whatwg-fetch';
export default {
  data() {
    return {
      stateData: 'test',
      constants: {}
    };
  },
  methods: {
    isReadCountShow(readCount) {
      return readCount > 300;
    },
    fetch_example() {
      fetch('https://jsonplaceholder.typicode.com/todos/1', {
        method: 'GET',
        body: {}
      })
        .then(response => response.json())
        .then((data, error) => {
          console.log(dataHandler);
          return data;
        })
        .catch(e => {
          console.log('error', e);
        });
    },
    dataHandler(dataMap) {
      console.log('dataHandler 11');
      return dataMap;
    }
  },
  created() {
    console.log('constructor');
    this.fetch_example();
    this.dataHandler();
  },
  beforeUpdate() {
    console.log('getDerivedStateFromProps');
  }
};
</script>
<style src="./index.response.css" />
