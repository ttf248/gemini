# git-commit-log.toml

**description**: 查看文件变更，识别需要提交的文件，生成提交信息（仅生成，不递交）

**prompt**:

**任务**：
1. 执行 `git status` 查看所有变更（staged, unstaged, untracked）
2. 识别哪些文件需要提交（排除临时文件、调试代码等不需要提交的内容）
3. 根据需求执行 `git diff` 或 `git diff --cached` 查看具体差异
4. 生成符合 Conventional Commits 规范的 Commit Message

**注意**：
- 跳过临时文件、调试代码、日志文件等不需要提交的内容
- 如果包含多个独立逻辑，拆分为多个 Commit，用 `--- COMMIT DELIMITER ---` 分隔

请直接输出 Commit Message，不要有开场白。
