---
{"dg-publish":true,"dg-permalink":"note/24","permalink":"/note/24/","tags":["Jetbrains","AICommits"],"created":"2024-07-21 13:27:04","updated":"2024-07-21 13:30:12"}
---

[[Jetbrains/AI Commits\|AI Commits]]

## 英文版

```
Write a commit message that accurately summarizes the changes made in the given `git diff` output, following the best practices and conventional commit convention as described below. Your response should look like this (no codeblock), the response must be the {locale} language:

<type>[optional scope]: <subject>

[optional body (bullet points)]

[optional footer(s)]

Example:
feat(components): add `AreaSelector` component

This commit added a component named `AreaSelector` for choosing area.

This component include these feature:
- Fetch areas form the API.
- Supports selecting city by province, selecting district by city, select street by district, and bidirectional binding value through `v-model`.
- Configurable properties such as `clearable` and `placeholder`.

This commit aims to add a new component designed to help users select regions more easily and accurately. With this component, users can browse and choose different regions more intuitively, enhancing user experience and operational efficiency.

Here are some best practices for writing commit messages:
- Write clear, concise, and descriptive messages that explain the changes made in the commit
- Use the present tense and active voice in the subject, for example, "fix bug" instead of "fixed bug"
- Use the imperative mood, which gives the subject a sense of command, e.g. "add feature" instead of "added feature"
- Limit the subject line to 72 characters or less
- Don't capitalize the first letter in subject
- Do not end the subject line with a period
- Any numbers or file names should be enclosed in backticks, e.g. "`0.1`" instead of "0.1", "`README.md`" instead of "README.md"
- Use a blank line between the subject and the body of the message
- Avoid using general terms like "update" or "change" in the subject, be specific about what was updated or changed
- Explain, What was done at a glance in the subject line, and provide additional context in the body of the message
- Why the change was necessary in the body of the message
- If the commit type is "feat" and the added content is a class, explain what members and methods the class contains, what the parameters of this methods are and what their types area, what the return value is and what type, and why this method is defind
- If the commit type is "feat" and the added content is a function, explain what the parameters of this function are and what their types are, what the return value is and what type, and why this function is defined
- If the commit type is "feat" and the added content is a Vue component, explain what the template of thie Vue component contains, what props it receives, and what the interaction logic is
- If the change contains breaking changes, use this format in the footer to explain the content of the breaking change: `BREAKING CHANGE: <description>`

Here are the commit types you can choose from:
- feat: Introduces a new feature to the codebase
- fix: Fix patches a bug in the codebase
- build: Changes that affect the build system or external dependencies (Usually associated with changes to build scripts, e.g. Gradle, NPM, Cargo). Its scope shoud be the lowercase name of these build systems, such as npm, gradle or cargo.
- chore: Miscellaneous commits, copyrights or other repo configs, usually used for files in non-src directories. (example scopes: eslint, prettier)
- ci: Changes to CI configuration files and scripts (example scopes: Travis, Circle, GitHub Actions)
- docs: Non-code changes, such as fixing typos or adding new documentation (example scopes: readme)
- style: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- refactor: A code change that neither fixes a bug nor adds a feature
- perf: A code change that improves performance
- test: Adding missing tests or correcting existing tests

Here is the output of the `git diff`:
--
{diff}
```

## 中文版

```
按照下面的 `git diff` 输出的内容中所作的更改根据下面所述的最佳实践和常规提交约定编写一条提交信息，准确总结。你的回复应该如下所示并且无代码块，回复必须是 {locale} 语言：

<类型>[可选的范围]: <主题>

[可选的正文 (要点)]

[可选的尾注]

例子:
feat(components): 增加 `AreaSelector` 组件

这个提交增加了一个名为 `AreaSelector` 的组件，用于选择地区。

该组件包含一下功能：
- 从 API 获取地区信息
- 支持通过省选择市，通过市选择区，通过区选择街道，并通过 `v-model` 双向绑定值
- 可配置的参数，例如 `clearable` 和 `placeholder`

这个提交旨在添加一个新组件，帮助用户更轻松和准确地选择地区。通过这个组件，用户可以更加直观地浏览和选择不同的地区，从而提升用户体验和操作效率。

以下是编写提交消息的一些最佳实践：
- 编写清晰、简洁且描述性强的提交消息，解释提交中所作的更改
- 在主题中使用现在时而不是过去时，例如“增加功能”而不是“增加了功能”
- 主题所在的行字符数量应小于或等于 72
- 主题的结尾不要有句号
- 任何数字或文件名都应括在反引号中，例如使用 `0.1` 替代 "0.1"，使用 `README.md` 替代 "readme.md"
- 在主题所在的行和正文之间空出一行
- 避免在主题中使用“更新”或“变更”等笼统术语，应具体说明更新或变更了哪些内容
- 在主题中用一句话概括做了什么，再在正文中详细说明做了什么
- 在正文中说明变更的必要性
- 在正文中说明为什么需要进行变更
- 如果提交的类型是 "feat"，且增加的内容是一个类，说明这个类包含哪些成员，哪些方法，这些方法的参数是什么，返回值是什么，为什么要定义这个方法
- 如果提交的类型是 "feat"，且增加的内容是一个函数，说明这个函数的参数是什么及是什么类型，返回值是什么及是什么类型，为什么要定义这个函数
- 如果提交的类型是 "feat"，且增加的内容是一个 Vue 组件，说明这个 Vue 组件的 template 包含哪些内容，接收哪些 props，交互逻辑是什么
- 如果更改包含破坏性变更，则在页脚使用该格式解释破坏性变更的内容 `BREAKING CHANGE: <描述>`

以下是你可以选择的提交类型：
- feat：为代码库引入新功能
- fix：修复代码库中的错误
- build：影响构建系统或外部依赖项的更改（通常与构建脚本的更改相关，例如 Gradle、NPM、Cargo）。其范围应为这些构建系统的小写名称，例如 npm、gradle 或 cargo。
- chore：杂项提交、版权或其他 repo 配置，通常用于非 src 目录中的文件。（示例范围：eslint、prettier）
- ci：CI 配置文件和脚本的更改（示例范围：Travis、Circle、GitHub Actions）
- docs：非代码更改，例如修复拼写错误或添加新文档（示例范围：readme）
- style：不影响代码含义的更改（空格、格式、缺少分号等）
- refactor：既不修复错误也不添加功能的代码更改
- perf：提高性能的代码更改
- test：添加缺失的测试或更正现有测试

以下是 `git diff` 输出的内容：
--
{diff}
```
## 参考

1. [Prompts](https://github.com/Blarc/ai-commits-intellij-plugin/discussions/18#discussioncomment-8776472)
2. [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/)