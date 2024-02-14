<template>
    <div class="bookmark-label-container" >
      <div class="bookmark-scroll">
        <a v-for="(button, index) in buttons" :key="index" :href="button.link" target="_blank" class="bookmark-label">
          {{ button.text }}
        </a>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        buttons: [
          { text: '哔哩哔哩', link: 'https://www.bilibili.com' },
          { text: '力扣', link: 'https://leetcode.cn' },
          // Add more buttons as needed
        ],
        isScrolling: true
      };
    },

};
  </script>
  
  <style>
.bookmark-label-container {
  position: fixed;
  bottom: 110px;
  left: 50%;
  transform: translateX(-50%); /* 让容器水平居中 */
  width: 90%;
  overflow: hidden;
  display: flex; /* 使用 Flex 布局 */
  justify-content: center; /* 让按钮水平居中对齐 */
}

.bookmark-scroll {
  display: flex;
  width: max-content;
}

.bookmark-label {
  cursor: pointer;
  height: 100px;
  width: 120px;
  padding: 0 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: rgba(0, 0, 0, 0.24);
  border-radius: 8px;
  font-size: 16px;
  transition: background-color 0.3s, box-shadow 0.3s;
  margin-right: 10px; /* Adjust as needed for spacing between buttons */
  text-decoration: none; /* Remove underline */
  color: inherit; /* Inherit text color */
  color: #fff;
}

.bookmark-label:hover {
  background-color: var(--hover-color);
}
  </style>
  