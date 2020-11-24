### Select 选择器

:popper-append-to-body="false" 添加这个有bug => 会差几像素

```javascript
.el-select {
  .el-input {
    .el-input__inner {
      height: 33px;
      background-color: #0e2146;
      font-size: 11px;
      border: 1px solid #0e2146;
      color: #ffffff;
      &:hover {
        // border: 1px solid #ffe600;
      }
      // 鼠标按下
      &:focus {
        // border: 1px solid red;
      }
    }
    // 右侧三角符号
    .el-input__suffix {
        .el-input__suffix-inner {
          .el-input__icon {
            line-height: 25px;
          }
        }
      }
  }
  // 鼠标松开高亮
  .el-input.is-focus .el-input__inner {
    // border: 1px solid #00ff0d;
  }
  // 下拉菜单
  .el-select-dropdown {
    background-color: #0e2146;
    border: 1px solid #0e2146;
    .el-scrollbar {
      .el-scrollbar__wrap {
        .el-select-dropdown__list {
          .el-select-dropdown__item {
            font-size: 12px;
            color: #ffffff;
            // 鼠标移出颜色
            &.hover {
              background-color: #0ab9e5;
            }
            &:hover {
              background-color: #0ab9e5;
            }                       
            // 选择后的字体颜色
            &.selected {
              color: #ffffff;
              font-weight: 400;
            }
          }
        }
      }
    }
    // 三角形
    .popper__arrow {
        border-top-color: #0e2146 !important;
        border-bottom-color: #0e2146 !important;
      &::after {
        border-top-color: #0e2146 !important;
        border-bottom-color: #0e2146 !important;
      }
    }
  }
}
```



### el-tree

````javascript
.el-tree {
  background-color: #ffffff00;
  color: #ffffff;
  .el-tree-node {
    .el-tree-node__content {
      .el-tree-node__expand-icon {}
      .el-checkbox {}
      .el-tree-node__label {
        font-size: 12px;
      }
      &:hover {
        background-color: #074529;
      }
    }
    .el-tree-node__children {}
    // 鼠标点击后高亮
    &:focus>.el-tree-node__content {
      background-color: #074529;
    }
  }
}
````







### Checkbox 多选框

>  .el-checkbox-group {
>
> ​          .el-checkbox {
>
> ​           color: #ffffff;
>
> ​           padding-top: 10px;
>
> ​           .el-checkbox__input {}
>
> ​           .el-checkbox__label {
>
> ​            font-size: 12px;
>
> ​            width: 110px;
>
> ​           }
>
> ​          }
>
> ​         }



### input输入框

```javascript
.el-input {
  .el-input__inner {
    height: 37px;
    background-color: #0e2146;
    border: 1px solid #1b60a500;
    font-size: 11px;
    caret-color:#1f4796; // 光标颜色
    color: #ffffff;
    &:hover {
      border-color: #409eff;
    }
    // 鼠标点击后的高亮
    &:focus {
      border: 1px solid #409eff;
     }
    &::-webkit-input-placeholder {
      color:#1f4796; // 输入框内默认字体颜色
    }
  }
  // 右边放大镜按钮
  .el-input-group__append {
    background-color: #0e2146;
    border: 1px solid #1b60a5;
    border-left: 0
  }
}
```

![shu_ru_kuang](../../assets/shu_ru_kuang.png)



### button按钮

```java
.el-button {
  font-size: 10px;
  padding: 7px 10px;
  border-radius: 0;
  background: #009688;
  border-color: #009688;
  // 鼠标滑过
  &:hover {
    background: #017a6e;
    border-color: #017a6e;
  }
  // 鼠标按下
  &:active {
    background: #015c53;
    border-color: #015c53;
  }
}
```



### 表格

```javascript
.el-table {
  font-size: 12px;
  background-color: #ffffff00;
  color: #ffffff;
  .el-table__header-wrapper {
    .el-table__header {
      thead {
        color: #0bcff1;
        tr {
          th {
            background-color: #071229;
            text-align: center;
            border-bottom: 0 solid #EBEEF5;
            .cell {}
          }
        }
      }
    }
  }
  .el-table__body-wrapper {
    .el-table__body {
      tbody {
        tr {
          background-color: #ffffff00;
          td {
            text-align: center;
            padding: 7px 0;
            // 取消td的背景颜色
            background-color: #07122900;
            border: 0px solid #ffffff;
            .cell {
              .el-button {
                font-size: 10px;
                padding: 7px 10px;
                border-radius: 0;
                &:nth-child(1) {
                  background: #009688;
                  border-color: #009688;
                  &:hover {
                    background: #017a6e;
                    border-color: #017a6e;
                  }
                  &:active {
                    background-color: #015c53;
                    border-color: #015c53;
                  }
                }
                &:nth-child(2) {
                  background: #ff5722;
                  border-color: #ff5722;
                  &:hover {
                    background: #f05020;
                    border-color: #f05020;
                  }
                  &:active {
                    background-color: #bb3d16;
                    border-color: #bb3d16;
                  }
                }
              }
            }
          }
          &:hover>td {
            background-color: #074529;
            z-index: 10000;
          }
          // 选择tr偶数行
          &:nth-child(even) {
            background-color: #071229;
          }
        }
      }
    }
  }
  &::before {
    background-color: #0bcef100;
  }
}
```



### 对话框

```javascript
.el-dialog__wrapper {
    .el-dialog {
      background-color: #091733;
      .el-dialog__header {
        .el-dialog__title {
          color: #ffffff;
        }
        .el-dialog__headerbtn {}
      }
      .el-dialog__body {
        color: #ffffff;
        font-size: 12px;
      }
      .el-dialog__footer {
        .el-button {
          font-size: 10px;
          padding: 8px 12px;
        }
      }
    }
  }
```



### 分页

```javascript
.el-pagination {
  .el-pagination__total {
    font-size: 12px;
    color: #ffffff;
  }
  .el-pagination__sizes {
    .el-select {
      .el-input {
        .el-input__inner {
          font-size: 12px;
          color: #ffffff;
          background-color: #ff000000;
          border: 1px solid #1f50b3;
        }
        .el-input__suffix {}
      }
    }
  }
  .btn-prev {
    color: #ffffff !important;
    background-color: #ffffff00 !important;
    border: 1px solid #1f50b3;
    &:hover {
      color: #1f50b3 !important;
    }
    &:disabled {
      color: #757575 !important;
    }
  }
  .el-pager {
    li {
      font-size: 10px;
      background-color: #ffffff00 !important;
      border: 1px solid #1f50b3;
      color: #ffffff !important;
      margin: 0 5px;
      &:hover {
        color: #1f50b3 !important;
      }
      // 鼠标点击后高亮
      &.active {
        color: #ffffff !important;
        background-color: #0e84fd !important;
      }
      &:first-child {
        margin-left: 10px;
      }
      &:last-child {
        margin-right: 10px;
      }
    }
  }
  .btn-next {
    color: #ffffff !important;
    background-color: #ffffff00 !important;
    border: 1px solid #1f50b3;
    &:hover {
      color: #1f50b3 !important;
    }
    &:disabled {
      color: #757575 !important;
    }
  }
  .el-pagination__jump {
    color: #ffffff;
    font-size: 12px;
    .el-input {
      font-size: 12px;
      .el-input__inner {
        background-color: #0e85fd00;
        border: 1px solid #0e84fd;
        color: #ffffff;
        &:hover {
          // border: 1px solid #1765b3;
        }
        // 鼠标点击后的高亮
        &:focus {
          // border: 1px solid #409eff;
        }
      }
    }
  }
}
```



### 滚动条

````javascript
// 滚动条
  ::-webkit-scrollbar {
    width: 9px; /*对垂直流动条有效*/
    // height: 10px; /*对水平流动条有效*/
  }
  // 背景
  ::-webkit-scrollbar-track {
    -webkit-box-shadow: inset 0 0 6px rgb(9, 23, 52, .3); // 内阴影
    background-color: #091733;
    border-radius: 3px;
  }
  // 滑块
  ::-webkit-scrollbar-thumb{
    -webkit-box-shadow: inset 0 0 6px rgb(9, 23, 52, .3); // 内阴影
    background-color: #3e5381;
    border-radius: 30px;
  }
````



### 开关

```javascript
<template>
  <div>
    <input
      class="my_switch"
      type="checkbox"
      :style="{'--activeColor':activeColor,'--inactiveColor':inactiveColor}"
      :activeText="activeText"
      :inactiveText="inactiveText"
      :checked="checkedValue"
      @click="toggleClick"
    />
  </div>
</template>

<script>
export default {
  props: {
    checkedValue: {
      type: Boolean,
      default: false
    },
    activeText: {
      type: String,
      default: '启动'
    },
    activeColor: {
      type: String,
      default: '#409eff'
    },
    inactiveText: {
      type: String,
      default: '禁用'
    },
    inactiveColor: {
      type: String,
      default: '#f77463'
    }
  },
  methods: {
    toggleClick (e) {
      this.$emit('toggleClick', e.target.checked)
      console.log(this.$emit('toggleClick', e.target.checked))
    }
  }
}
</script>

<style scoped>
.my_switch {
  position: relative;
  width: 52px;
  height: 20px;
  border: 2px solid var(--activeColor);
  outline: 0;
  border-radius: 0;
  transition: background-color 0.1s, border 0.1s;
  appearance: none;
  outline: 0;
  background-color: var(--activeColor);
  border-radius: 15px;
  box-sizing: content-box;
  vertical-align: middle;
  cursor: pointer;
}
.my_switch:after {
  content: attr(activeText);
  color: var(--activeColor);
  font-size: 8px;
  line-height: 20px;
  text-align: center;
  position: absolute;
  top: 0;
  left: 0;
  width: 30px;
  height: 20px;
  border-radius: 15px;
  background-color: #fff;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.4);
  transition: transform 0.35s cubic-bezier(0.4, 0.4, 0.25, 1.35);
}
.my_switch:checked:after {
  content: attr(inactiveText);
  color: var(--inactiveColor);
  transform: translateX(22px);
}
.my_switch:checked {
  border-color: var(--inactiveColor);
  background-color: var(--inactiveColor);
}
</style>

```

