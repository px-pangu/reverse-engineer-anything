# REA · 逆向工程 · Reverse Engineer Anything

> 对原生程序、托管代码、Electron/JS、打包产物、固件与浏览器目标做逆向分析：解释功能、比对版本、反编译、指导重建

![Type](https://img.shields.io/badge/type-Agent%20Skill-4a6b7c)
![Upstream](https://img.shields.io/badge/upstream-reverse-engineer-anything%20v42-8f8a80)
![License](https://img.shields.io/badge/license-归原作者-b8935a)

> ⚠️ 本仓库是个人使用环境中的 Skill 归档副本，**版权归原提供方**：reverse-engineer-anything v42

## 这是什么

REA 是一套**以出货产物为证据**的逆向分析流程。当你的判断必须依赖「实际编译出来的东西」而不是源码仓库时用它：解释某个功能怎么实现、两个版本差了什么、某个行为为什么出现。

> 不适用：在源码仓库里做普通的架构分析。那种情况直接读代码更快。

## 目标路由

先判断目标类型，再决定工具链：

| 目标 | 典型手段 |
|---|---|
| 原生（Native） | 反汇编、符号恢复、字符串与调用图 |
| 托管（.NET / JVM） | 反编译到 IL / 字节码级 |
| Electron / JavaScript | asar 解包、bundle 还原、主进程与渲染进程分离 |
| 打包产物（installer / packer） | 脱壳、资源雕刻 |
| 固件 | 文件系统识别、熵分析、交叉引用 |
| 浏览器目标 | 被动运行时证据、网络与存储取证 |

## 工作方式

1. **结论先行**：先给结论与置信度，再给证据链
2. **只读相关指南**：按路由结果加载对应参考，不全量加载
3. **必要时才连接运行时**：能不跑就不跑
4. 任务结束前给出「可复现的证据路径」，让别人能自己验证

## 目录结构

```
reverse-engineer-anything/
├─ SKILL.md      路由规则 · 工作纪律 · 参考索引
└─ references/   各目标类型的操作指南与工具说明
```

## 使用边界

仅用于你有权分析的软件：自己买的、自己写的、明确授权审计的、或用于互操作性与安全研究的。**不要用于绕过授权、破解商用软件或规避技术保护措施。**

## 许可

原包未声明开源许可，著作权归原作者所有。本仓库仅为个人归档，**不作出任何再许可**，详见 `NOTICE.md`。


## 安装

```bash
git clone https://github.com/px-pangu/reverse-engineer-anything.git ~/.workbuddy/skills/reverse-engineer-anything
# Claude Code：~/.claude/skills/reverse-engineer-anything
```

> 若原包依赖 CLI（如 `kdocs`、`ima`、`wecom`、`pdfkit`），需先按 `SKILL.md` 的安装与认证段落配置本机环境。**仓库内不含任何凭据。**

