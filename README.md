# Vocab Tester (词汇量测试官)

这是一个支持 **Gemini CLI** 和 **Claude Code** 双平台的扩展技能（Skill/Extension）。它使用语言学家 Paul Nation 提出的词频带采样法 (Frequency-based Sampling)，结合大模型强大的语义理解能力，为用户提供一个准确、自适应且带有游戏化反馈的英语词汇量测试体验。

## 特性

*   **科学依据:** 基于权威的 COCA 词库频率带划分（从基础生存 1k 词汇到母语者级别的 20k 生僻词汇）。
*   **语义判定:** 不需要做无聊的选择题，LLM 会直接根据你描述的中文或英文释义判定你是否理解了这个词。
*   **自适应跃迁:** 根据你的连胜状态快速跳级（曲速引擎机制），节省测试时间。
*   **无挫败感设计:** 答错或回答“不知道”不会有负面反馈，LLM 会自动回落调整难度。
*   **双平台支持:** 一份代码同时兼容 Claude Code 和 Gemini CLI 扩展生态。

## 安装方法

### 方式 1: Gemini CLI 直接安装
使用 Gemini CLI，直接通过 GitHub 链接或本地路径安装：
```bash
gemini extensions install https://github.com/wanghanlele12345/vocab-tester
```

### 方式 2: Claude Code 安装
使用 Claude Code，直接通过本地路径安装（克隆仓库后）：
```bash
git clone https://github.com/wanghanlele12345/vocab-tester.git
cd vocab-tester
claude skills install .
```

## 使用指南
进入命令行助手（Gemini CLI 或 Claude Code）后，输入：
> "启动 vocab-tester 测测我的词汇量"

测试官会主动和你打招呼并抛出第一个问题，直接回答单词的大意即可（例如回答“这是一种复合物”或“不知道”）。

## 核心算法参考
*   频率 1k-5k：涵盖日常交流、报刊阅读的基础词汇 (如: `tiny`, `compound`)
*   频率 6k-10k：涵盖专业领域、学术文献和 GRE 词汇 (如: `erratic`, `devious`)
*   频率 11k-20k+：极高阶阅读和母语者生僻词 (如: `ephemeral`, `quagmire`)

## 许可证
MIT License