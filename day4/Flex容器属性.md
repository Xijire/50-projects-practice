### Flex容器属性
这些属性是设置在Flex容器上的，用于控制其子项的排列方式。

1. **`display`**
   - 值：`flex` 或 `inline-flex`
   - 功能：将元素设置为Flex容器，使其子元素变成Flex子项。
   - 示例：
     ```css
     .container {
         display: flex;
     }
     ```

2. **`flex-direction`**
   - 值：`row`（默认）、`row-reverse`、`column`、`column-reverse`
   - 功能：定义主轴的方向，决定子项的排列方向。
     - `row`：水平从左到右排列。
     - `row-reverse`：水平从右到左排列。
     - `column`：垂直从上到下排列。
     - `column-reverse`：垂直从下到上排列。

3. **`flex-wrap`**
   - 值：`nowrap`（默认）、`wrap`、`wrap-reverse`
   - 功能：控制子项是否在Flex容器中换行。
     - `nowrap`：不换行。
     - `wrap`：换行。
     - `wrap-reverse`：反向换行（从下到上）。

4. **`flex-flow`**
   - 值：`<flex-direction>` 和 `<flex-wrap>` 的组合（例如：`row wrap`）
   - 功能：简写属性，用于同时设置`flex-direction`和`flex-wrap`。

5. **`justify-content`**
   - 值：`flex-start`（默认）、`flex-end`、`center`、`space-between`、`space-around`、`space-evenly`
   - 功能：在主轴方向上对齐子项。
     - `flex-start`：靠主轴起点对齐。
     - `flex-end`：靠主轴终点对齐。
     - `center`：居中对齐。
     - `space-between`：子项之间均匀分布，第一个和最后一个子项靠边。
     - `space-around`：子项之间均匀分布，两端有一半的空间。
     - `space-evenly`：子项之间和两端的间距相等。

6. **`align-items`**
   - 值：`stretch`（默认）、`flex-start`、`flex-end`、`center`、`baseline`
   - 功能：在交叉轴方向上对齐子项。
     - `stretch`：如果没有设置高度或宽度，子项会拉伸填满容器。
     - `flex-start`：靠交叉轴起点对齐。
     - `flex-end`：靠交叉轴终点对齐。
     - `center`：居中对齐。
     - `baseline`：按照子项的基线对齐。

7. **`align-content`**
   - 值：`flex-start`、`flex-end`、`center`、`space-between`、`space-around`、`stretch`
   - 功能：控制多行Flex子项的对齐方式，仅在Flex容器有多行子项时起作用。

### 二、Flex子项属性
这些属性是设置在Flex子项上的，用于控制子项的尺寸、排列和行为。

1. **`order`**
   - 值：整数，默认为0
   - 功能：控制Flex子项的排列顺序，值越小，排列越靠前。可以为正数或负数。

2. **`flex-grow`**
   - 值：数字，默认为0
   - 功能：定义子项在容器中剩余空间的分配比例。例如，`flex-grow: 1`表示如果有多余空间，子项将按比例占用这些空间。

3. **`flex-shrink`**
   - 值：数字，默认为1
   - 功能：定义子项在容器空间不足时的缩小比例。例如，`flex-shrink: 1`表示当空间不足时，子项会按比例缩小。

4. **`flex-basis`**
   - 值：长度值（如`20%`、`200px`）或`auto`（默认）
   - 功能：设置子项的初始大小。如果设置为`auto`，则根据内容或宽高属性确定。

5. **`flex`**
   - 值：`flex-grow`、`flex-shrink`和`flex-basis`的简写形式（例如：`flex: 1 1 200px`）
   - 功能：用于简写设置子项的`flex-grow`、`flex-shrink`和`flex-basis`属性。

6. **`align-self`**
   - 值：`auto`（默认）、`flex-start`、`flex-end`、`center`、`baseline`、`stretch`
   - 功能：允许单独的Flex子项覆盖`align-items`设置，对齐在交叉轴上的位置。

