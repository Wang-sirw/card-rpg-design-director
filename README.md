# Card RPG Design Director

面向独立开发者的 Godot 4.x 卡牌构筑 RPG 设计插件。它只包含 Skills，不包含 MCP 服务器，也不连接外部账户。

## 能做什么

插件会根据问题自动选择一个或多个工作模式：

1. 游戏概念审查
2. 核心循环设计
3. 卡牌系统设计
4. 战斗系统设计
5. MDA 玩家体验分析
6. 系统交互和无限循环风险检查
7. 原型范围控制
8. 功能优先级排序
9. 数值假设与测试区间
10. 将已确认的设计转换为 Codex 可执行任务

输出会区分已确认、暂定和开放问题，主动提示复杂度、数值失控与单人制作成本，并优先给出最小可运行或可测试版本。

## 从 GitHub marketplace 安装

在安装了 Codex CLI 的电脑上运行：

```bash
codex plugin marketplace add Wang-sirw/card-rpg-design-director
codex plugin add card-rpg-design-director@card-rpg-design-director
```

也可以在 ChatGPT 桌面端的 Plugins 页面中添加这个 GitHub marketplace，然后安装 **Card RPG Design Director**。安装后请新建一个对话，使新 Skill 生效。

仓库地址：

https://github.com/Wang-sirw/card-rpg-design-director

## 更新

仓库内容更新后运行：

```bash
codex plugin marketplace upgrade card-rpg-design-director
codex plugin add card-rpg-design-director@card-rpg-design-director
```

## 结构

```text
.agents/plugins/marketplace.json
plugins/card-rpg-design-director/.codex-plugin/plugin.json
plugins/card-rpg-design-director/skills/card-rpg-design-director/
```

## 使用示例

- 审查我的游戏概念，指出最需要验证的假设。
- 设计战斗核心循环，并区分已确认、暂定和开放问题。
- 检查这组卡牌触发是否可能形成无限循环。
- 给出首个可玩的原型范围，不要直接写代码。
- 把已确认的设计转换为一个有边界、可验收的 Codex 任务。
