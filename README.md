# 新年祝福贺卡 - 除夕专享

一个新中式风格的除夕祝福贺卡网页。

## 功能特点

- 🎨 新中式设计风格，浅米色宣纸质感背景
- 📜 卷轴展开动画效果
- ⌨️ 打字机文字显示效果
- 🏮 金色粒子飘落特效
- 📝 红印章装饰
- 📱 完美响应式设计，支持手机端浏览
- 🔗 支持URL参数自定义内容

## 使用方法

### 直接打开

打开 `index.html` 文件即可使用。

### URL参数自定义

通过URL参数可以动态修改贺卡内容：

| 参数 | 说明 | 默认值 |
|------|------|--------|
| `name` | 名字（可选） | - |
| `title` | 称呼 | 老师 |
| `blessing` | 祝福语 | 新春快乐，身体安康，桃李满天下，万事皆顺遂 |

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

# 全部自定义
index.html?name=李&title=老师&blessing=龙年大吉，万事如意，心想事成
```

## 技术栈

- HTML5
- CSS3 (动画、响应式)
- JavaScript (原生，无依赖)

## 项目结构

```
.
├── index.html  # 主文件（包含HTML、CSS、JS）
└── README.md   # 说明文档
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

## 署名

Kevin Huang
