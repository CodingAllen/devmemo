# macOS上管理Node.js版本指南

## 安装NVM（Node Version Manager）

1. 使用curl安装NVM：
   ```bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
   ```

2. 配置shell：
   将以下内容添加到你的shell配置文件（~/.bash_profile, ~/.zshrc, ~/.profile, 或 ~/.bashrc）：

   ```bash
   export NVM_DIR="$HOME/.nvm"
   [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
   [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
   ```

3. 重新加载配置：
   ```bash
   source ~/.bashrc  # 或你的对应配置文件
   ```

## 使用NVM管理Node.js

1. 安装Node.js版本：
   ```bash
   nvm install 14  # 安装Node.js 14.x
   nvm install 16  # 安装Node.js 16.x
   nvm install --lts  # 安装最新LTS版本
   ```

2. 切换Node.js版本：
   ```bash
   nvm use 14  # 切换到Node.js 14.x
   nvm use 16  # 切换到Node.js 16.x
   ```

3. 设置默认版本：
   ```bash
   nvm alias default 14  # 将Node.js 14.x设为默认
   ```

4. 项目特定版本：
   在项目根目录创建.nvmrc文件：
   ```bash
   echo "14" > .nvmrc
   ```
   然后在项目目录中运行：
   ```bash
   nvm use
   ```

## 维护和更新

1. 查看已安装版本：
   ```bash
   nvm ls
   ```

2. 查看可安装版本：
   ```bash
   nvm ls-remote
   ```

3. 更新npm：
   ```bash
   nvm install-latest-npm
   ```

4. 卸载特定版本：
   ```bash
   nvm uninstall 14
   ```

5. 更新到最新LTS版本：
   ```bash
   nvm install lts/* --reinstall-packages-from=current
   nvm use lts/*
   nvm alias default node
   ```

## 安全建议

- 定期更新到最新的LTS版本
- 删除不再使用的旧版本
- 使用官方源安装包
- 在切换版本后检查全局包的兼容性

遵循这些步骤，你可以有效地在macOS上管理多个Node.js版本，确保开发环境的灵活性和安全性。
