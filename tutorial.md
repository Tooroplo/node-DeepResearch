# Windows 系统安装 Node DeepResearch 教程

## 项目介绍

OpenAI 最近推出的 Deep Research 功能是一个高级的 AI Agent，能够通过自动化的多步骤联网研究任务生成全面的报告。由于该功能仅对美国地区的 Pro 用户开放（每月 200 美元），我们将使用 Jina AI 开源的 Node DeepResearch 项目作为替代方案。

该项目完全模拟了 OpenAI 的 DeepResearch 功能，只需要免费的 Gemini API Key 和 Jina AI API Key 即可使用。

## 安装步骤

### 1. 获取必要的 API Keys

#### 获取 Gemini API Key
1. 访问 [Google AI Studio](https://makersuite.google.com/app/apikey)
2. 使用 Google 账号登录
3. 点击右上角的蓝色按钮"获取 API key"
4. 在新页面点击"创建 API key"
5. 选择项目并创建
6. 复制并保存生成的 API key

#### 获取 Jina AI API Key
1. 访问 [Jina AI](https://jina.ai/reader)
2. 注册并登录账号
3. 复制并保存 API key

### 2. 安装必要软件

#### 安装 Node.js
1. 访问 [Node.js 官网](https://nodejs.org/)
2. 下载 Windows 版本的 LTS 安装包
3. 运行下载的安装包，按照安装向导完成安装
4. 验证安装：
   - 打开命令提示符（Win + R，输入 cmd）
   - 输入以下命令验证安装：
   ```bash
   node -v
   npm -v
   ```

#### 安装 Git
1. 访问 [Git 官网](https://git-scm.com/download/win)
2. 下载 Windows 版本
3. 运行安装程序，使用默认设置即可
4. 验证安装：
   ```bash
   git --version
   ```

### 3. 项目配置

#### 设置环境变量
1. 打开命令提示符（以管理员身份运行）
2. 输入以下命令（替换为您的实际 API Keys）：
   ```bash
   set GEMINI_API_KEY=your_gemini_api_key
   set JINA_API_KEY=your_jina_api_key
   ```

#### 克隆并安装项目
1. 打开命令提示符，进入您想安装项目的目录
2. 克隆项目：
   ```bash
   git clone https://github.com/jina-ai/node-DeepResearch.git
   ```
3. 进入项目目录：
   ```bash
   cd node-DeepResearch
   ```
4. 安装依赖：
   ```bash
   npm install
   ```

### 4. 运行项目

#### 方式一：命令行运行
测试简单查询：
```bash
npm run dev "1+1="
```

测试复杂查询：
```bash
npm run dev "your complex query here"
```

#### 方式二：作为服务运行
启动服务：
```bash
npm run serve
```
服务将在 http://localhost:3000 运行

### 5. 创建图形界面（可选）

如果您想要一个更友好的用户界面，可以使用 Python 的 Gradio 框架：

1. 安装 Python：
   - 访问 [Python 官网](https://www.python.org/downloads/)
   - 下载 Python 3.11 版本（推荐）
   - 运行安装程序，确保勾选"Add Python to PATH"

2. 安装必要的 Python 包：
   ```bash
   pip install gradio requests
   ```

3. 创建 UI 界面：
   - 创建文件 `app.py`
   - 将提供的 Gradio UI 代码复制到文件中
   - 运行界面：
   ```bash
   python app.py
   ```

## 使用示例

1. 简单计算：
   ```bash
   npm run dev "1+1="
   ```

2. 数值比较：
   ```bash
   npm run dev "9.9和9.11哪个大"
   ```

3. 复杂查询：
   ```bash
   npm run dev "微调Llama3的超参数设置"
   ```

## 常见问题解决

1. 如果遇到 npm 版本问题，可以继续使用当前版本，不影响项目使用
2. 确保命令提示符以管理员身份运行
3. 如果环境变量设置后不生效，请重新打开命令提示符
4. 确保网络连接稳定，因为项目需要进行网络搜索

## 注意事项

- 所有命令都需要在项目目录下执行
- API Keys 请妥善保管，不要分享给他人
- 建议定期更新项目以获取最新功能
- 使用过程中如遇到问题，可以查看项目的 GitHub Issues

[本教程](https://youtu.be/vrpraFiPUyA) 到此结束，如果您在安装过程中遇到任何问题，欢迎查看项目的官方文档或提交 Issues。
