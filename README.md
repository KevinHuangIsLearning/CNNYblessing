# 新年祝福贺卡 - 除夕专享

一个新中式风格的除夕祝福贺卡网页。

🔗 **在线生成器：** https://kevinhuangislearning.github.io/CNNYblessing/generate.html

🎀 **样例效果：** https://kevinhuangislearning.github.io/CNNYblessing/

## 功能特点

- 🎨 新中式设计风格，浅米色宣纸质感背景
- 📜 卷轴展开动画效果
- ⌨️ 打字机文字显示效果
- 🏮 金色粒子飘落特效
- 📝 红印章装饰
- 📱 完美响应式设计，支持手机端浏览
- 🔗 支持 URL 参数自定义内容
  - 简单模式：分块填写名字、称呼、祝福语
  - 高级模式：直接输入完整正文
- ✍️ 高级模式支持完整 Markdown 语法和 LaTeX 数学公式
  - 加粗：`**文字**`
  - 斜体：`*文字*`
  - 行内公式：`$E=mc^2$`
  - 块级公式：`$$\int_0^\infty e^{-x^2}dx$$`
  - 列表、代码等完整 Markdown 功能
- 🖼️ 支持导出为 SVG 或 PNG 图片，可直接嵌入 markdown

## 使用方法

### 图形化生成器（推荐）

打开 `generate.html` 文件，通过表单填写信息即可：
- 填写各项自定义内容
- 点击「生成 URL」可复制链接或 Markdown
- 点击「预览」可在页面内预览效果
- 点击「导出 SVG」或「导出 PNG」直接下载图片

### 直接打开

打开 `index.html` 文件即可使用。

### URL参数自定义

通过URL参数可以动态修改贺卡内容：

#### 简单模式（分块填写）

| 参数 | 说明 | 默认值 |
|------|------|--------|
| `name` | 名字（可选） | - |
| `title` | 称呼 | 老师 |
| `blessing` | 祝福语 | 新春快乐，身体安康，桃李满天下，万事皆顺遂 |
| `title_text` | 标题文字 | 岁华新至，感念师恩 |
| `signature` | 署名 | Kevin Huang |

#### 高级模式（完整正文）

支持完整 Markdown 语法和 LaTeX 数学公式！

| 参数 | 说明 | 默认值 |
|------|------|--------|
| `message` | 完整正文（支持 Markdown + LaTeX，使用后忽略简单模式参数） | - |
| `title_text` | 标题文字 | 岁华新至，感念师恩 |
| `signature` | 署名 | Kevin Huang |

**Markdown 语法示例：**
- 加粗：`**文字**`
- 斜体：`*文字*`
- 行内公式：`$E=mc^2$`
- 块级公式：`$$\int_0^\infty e^{-x^2}dx = \frac{\sqrt{\pi}}{2}$$`
- 列表：`- 项目` 或 `1. 项目`
- 代码：`` `代码` ``

#### 导出参数

| 参数 | 说明 | 默认值 |
|------|------|--------|
| `export_to_pic` | 是否导出为图片模式 | false |
| `png` | 导出为 PNG（仅在export_to_pic=true时有效） | false |

### 示例

```
# 基本使用
index.html

# 自定义称呼
index.html?title=王老师

# 自定义名字和称呼
index.html?name=张&title=教授

# 自定义祝福语
index.html?blessing=新年快乐，工作顺利，阖家幸福

# 自定义标题和署名
index.html?title_text=龙年大吉&signature=张三

# 全部自定义（简单模式）
index.html?name=李&title=老师&blessing=龙年大吉，万事如意，心想事成&title_text=新春快乐&signature=李四

# 完整正文自定义（高级模式）
index.html?message=亲爱的老师，值此除夕佳节，感谢您过去的悉心教导。%0A祝您：新年快乐，万事顺遂。&title_text=新春快乐&signature=李四

# Markdown + LaTeX 示例
index.html?message=亲爱的**老师**，值此除夕佳节，感谢您过去的悉心教导。%0A%0A祝您：新年快乐，$e^{i\pi} + 1 = 0$，万事顺遂。%0A%0A**祝福列表：**%0A- 身体健康%0A- 工作顺利%0A- 桃李满天下&title_text=新春快乐&signature=李四

# 导出为SVG图片
index.html?export_to_pic=true&name=王&title=老师

# 导出为PNG图片
index.html?export_to_pic=true&png=true&name=王&title=老师
```

### Markdown嵌入

可以直接将导出 URL 作为图片链接嵌入 markdown：

```markdown
![新年祝福](https://kevinhuangislearning.github.io/CNNYblessing/index.html?export_to_pic=true&name=张&title=老师)
```

## 技术栈

- HTML5
- CSS3 (动画、响应式)
- JavaScript (原生)
- Marked.js (Markdown 解析)
- KaTeX (LaTeX 数学公式渲染)

## 项目结构

```
.
├── index.html    # 贺卡主页面
├── generate.html # 图形化生成器页面
└── README.md     # 说明文档
```

## 本地预览

```bash
# 使用Python启动本地服务器
python3 -m http.server 8000

# 或使用其他方式
# Node.js: npx serve
# PHP: php -S localhost:8000
```

然后在浏览器中访问 `http://localhost:8000`
