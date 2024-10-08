# css进阶

#### css级联层

级联层通过 @layer 规则来定义。每个层可以包含一组 CSS 规则，浏览器会根据这些层的顺序来确定样式的优先级。层的顺序越靠后，其优先级越高。

优先级的顺序由声明层的顺序来决定。在任何层之外声明的 CSS 样式会被按声明的顺序组合在一起，形成一个未命名的层，它会被当作最后声明的层

````
/* 定义基础样式层 */
@layer base {
    body {
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
    }
}

/* 定义组件样式层 */
@layer components {
    .button {
        background-color: blue;
        color: white;
        padding: 10px 20px;
        border: none;
        border-radius: 5px;
    }
}

/* 定义主题样式层 */
@layer themes {
    .dark-theme {
        body {
            background-color: #333;
            color: #fff;
        }

        .button {
            background-color: darkblue;
        }
    }
}
````

#### 层叠层
