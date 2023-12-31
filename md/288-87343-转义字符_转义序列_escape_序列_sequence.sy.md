---
show: step
version: 1.0
enable_checker: true
---

# 转义序列

## 回忆上次内容

- 上次研究了 现代的 换挡符
	- shift
	- capslock
- 编码
	- 从电报用的摩斯码
	- 进化到电传打字机的波特码(ITA1)
	- 继续如何变化呢？
	- 会进化到我们熟悉的ASCII编码吗？

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230129-1674959059173)

- 黑暗森林里面的东西
	- 已经发现了`\n` 和 `\r`
	- 还有什么 `特殊`字符 吗？🤔

### 搜索 ASCII

- 找到 `ascii`的定义

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210224-1614132466771)

- 还有 好多 
	- 类似于`\n`、`\r`的 特殊字符

### 动手试试

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210224-1614132527364)

- 总结一下 
	- 各种 转义字符

### 转义总结

- `\a`
  - 响铃 ␇ (bell)
  - 电传打字机 回车前 都会预警`响铛`
	- 避免 回车过程中 误打字符
  - 可以 
	- 手动发送编码
		- 敲一下 这个铃铛
  - 后来 
	- 是让 蜂鸣器 鸣叫

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230129-1674959156825)

- `\b`
  - BackSpace
  - 退回一格
- `\t`
  - table
  - 水平制表符
  - Horizontal Tab
  - 效果是空四个格
- `\v`、`\f`
  - 效果就是 
	- 纯喂纸 不回车

### 黑暗森林

- 再看 ascii码表
	- 黑暗森林 
		- 很多部分 已经 `展示`出来 了
		- 好像也没有 那么`神秘` 了

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221021-1666357755757)

- 为什么 只能`\n`
	- 难道 `/n` 不行么？
	- 动手 试试！

### 实验

- 确实 不行!

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210923-1632393662999)

- `ascii`的定义 是 `源头`
- python 对于这些字符的解释
	- 是跟 c语言 学的
- 这些特殊的东西
	- 都和 `\`反斜杠 
		- 这个字符相关联
- 为什么呢？

### 反斜杠

- 为什么管 这个方向的斜杠
	- 叫 `反斜杠` 呢？
- 斜杠是 成对儿的
  - 有 斜杠 
	- slash 
	- / 

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210224-1614171719752)

- 就有 反斜杠
	- backslash
	- \

### slash

- 我们一般都是  `右`利手
  - 从上往下砍
	- 都是 右上到左下 
	- slash 很顺手
	- slash 这个词本身就是砍
	- 用鞭子或者锋利的刃来砍
		- 暴力的砍
		- 主要是对于树来说的
    - 顺手的就是 slash

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230129-1674960020430)

- 反过来不顺手的就是 
	- backslash
	- 对应的是不正常的
	- 转化含义的 

### 转义字符

- 反斜杠的作用是 转义
	- 有 逆向思维的感觉
	- \自身 无法 
		- 构成一个 具体的字符
	- 而是 要和后面的字符 一起
		- 构成一个 `转义字符`

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230109-1673239085837)

- 转义用的 是
	- `反`斜杠
	- \ 
	- backslash

### 转义 Escape

- `\`反斜杠(backslash)
	- 加了其他字符 之后
		- 字符 就不是 原来的字面意思 了
- 就转义了
	- 转义转义 
	- 转化含义

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210224-1614157679393)

- 所以`\`反斜杠 这个字符
	- 也叫做转义字符
		- `Escape character`
- `\b` 这两个字符的序列
	- 算是一个 转义序列 
		- `Escape sequence`
		- `\` 这个转义字符
		- 会让 `\b`转义序列 
		- 转义为 `Backspace` 
			- 退格这`1`个字符
- 这个退格 是 
	- 转义序列`\b` 转化含义之后的 含义
	- 这个 转化后的 含义 
		- 对应 `1`个 ascii字符
- 可以 在键盘
	- 找到 `\b` 这个字符 吗？

### 键盘

- 就是 `\b`
	- 键盘上的<kbd>退格</kbd>
		- 对应的ascii值 就是 `8`

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210226-1614310192087)

- 转义的`本质` 是什么 呢?

### 转义`本质`

- 转义转义 转换含义!!!😡
  - `\n`本来是 两个字符
  - 转义字符`\`反斜线
	- 把自己 和后面的字符`n` 一起
	- 构成了 转义序列`\n`
  - 转换含义 成为 一个`新`的含义
- 原来的字符是`\`和`n`
  - 转成新的含义为`换行`

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220414-1649941727864)

- `\r`就不是 `\`和`r` 了
	- `\r` 是一个`整体`
	- 对应 一个字符
	- 整个 对应 ascii 中
		- 序号`13`的字符

### 试试

- 就像 `a` 对应 `65` 一样
	- `\b` 对应 `8`
- `\b` 在 python3 的作用
	- 退格
	- 你发现了 `12\ba` 变成 `1a` 了么？

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210923-1632394056849)

- `\b`、`\x08`、`chr(8)` 是 同一个字符
- 但是这个`\x08` 
	- 是什么意思？

### 继续转义

- 这个`x08` 刚好是
	- 退格对应字符的 ascii值
    - <kbd>退格</kbd> 对应的值是 `8`

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221018-1666061961593)

- 但这个 8 是
  - (`0x08`)<sub>16进制</sub>
  - 但是这个 `x` 是什么意思来着？

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210224-1614158000148)

- `x` 的意思是 `hexadecimal`
	- hex 就是 大着舌头说six
	- 后面 `2`位 `16`进制数
	- 刚好 对应 一个字节

## 总结
- 什么是 转义？
	- 转义转义 转化含义
	- `\` 是 转义字符
	- `\n`、`\r`是 转义序列
- 还有什么 转义序列 吗？
  - `\a`是 响铃
  - `\b` 退格键
  - `\t` 水平制表符 tab键
  - `\v`、`\f` 实现喂纸不回车
- 通过 16进制数值 转义
  - `\xhh`
  - 输出 (`hh`)<sub>`16进制`</sub>对应的`ascii`字符
- 如果我们不输入`x`
  - 会发生什么呢？

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220918-1663508014283)

- 为什么会输出 `S` 呢？🤔
- 我们下次再说！👋
