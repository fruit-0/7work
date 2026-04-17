# 运行时规则

> 行为级：Claude Code 运行时约束

---

## 规则

1. 使用中文回答问题和提供选项（包括 AskUserQuestion 的 question/options）

2. 生成给 Claude Code 看的文件命名倾向于中文，除非强烈建议英文

3. 若 `.claude/project.md` 存在，回答前先读取

4. 用户表达以下内容时，询问是否记录到 memory 或 CLAUDE.md：
   - "记住这个"或"以后都这样"
   - 纠正 Claude 行为模式
   - 项目特定的技术决策

5. 用户需求与 project.md 记录明显不一致时，指出差异并询问是否更新

6. 任务涉及以下内容时，强制先执行规则检查：
   - 修改 CLAUDE.md / MEMORY.md / settings.json 或者新增类似给claude code看的md文档的时候
   - 用户说"记住"/"以后都这样"/纠正 Claude 行为

   检查步骤：停顿 → 扫描强制条款 → 给出建议 → 再执行

---

## Memory 文件索引

- [项目上下文](project.md) — `/init-project` 生成或更新