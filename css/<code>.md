##### 解决 `<code>` 标签自动换行问题
```css
code {
  display: block;
  overflow: auto;
  white-space: normal;
  word-wrap: break-word;   /* 自动换行 */
  word-break: break-all;  /* 英文单词断行 */
}
```
