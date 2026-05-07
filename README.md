# 🚀 Campus Market - 正确的启动方式

## 📍 项目位置
```
F:\campus-market
```

---

## ⚡ 最简单的启动方式

### 方式 1：直接运行脚本（推荐）

1. **打开 PowerShell**
   - 在 `F:\campus-market` 文件夹中
   - 按住 `Shift` + 右键
   - 选择"在此处打开 PowerShell 窗口"

2. **运行安装脚本**
   ```powershell
   .\install.ps1
   ```
   按 Enter

3. **等待安装完成**
   - 脚本会自动检查 Python 和 Node.js
   - 自动安装所有依赖
   - 完成后会暂停

4. **启动项目**
   ```
   双击 run.bat
   ```

5. **打开浏览器**
   ```
   http://localhost:5173
   ```

---

## ⚡ 方式 2：如果提示权限错误

如果看到"不是此版本中的有效语句分隔符"错误，运行：

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
```

然后再运行：
```powershell
.\install.ps1
```

---

## ⚡ 方式 3：使用批处理脚本

如果 PowerShell 有问题，使用批处理脚本：

```
双击 install.bat
```

---

## ⚡ 方式 4：手动安装

### 打开 PowerShell，运行：

**安装后端依赖：**
```powershell
cd F:\campus-market\backend
python -m pip install -r requirements.txt
```

**安装前端依赖：**
```powershell
cd F:\campus-market\frontend
npm install
```

---

## 🆘 常见错误

### 错误 1："不是此版本中的有效语句分隔符"

**原因**：PowerShell 执行策略限制

**解决**：
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
.\install.ps1
```

### 错误 2："Python 未安装"

**解决**：
1. 下载 Python 3.11+：https://www.python.org/downloads/
2. 安装时勾选 "Add Python to PATH"
3. 重启电脑

### 错误 3："Node.js 未安装"

**解决**：
1. 下载 Node.js 18+：https://nodejs.org/
2. 安装（默认选项）
3. 重启电脑

### 错误 4：网址打不开

**运行诊断工具：**
```
双击 diagnose.bat
```

---

## 📚 脚本说明

| 脚本 | 用途 |
|------|------|
| `install.ps1` | PowerShell 安装脚本（推荐） |
| `install.bat` | 批处理安装脚本 |
| `run.bat` | 启动项目 |
| `diagnose.bat` | 诊断问题 |

---

## ✅ 启动成功的标志

### 后端窗口显示：
```
INFO:     Uvicorn running on http://127.0.0.1:8000
INFO:     Application startup complete
```

### 前端窗口显示：
```
VITE v5.0.8  ready in 123 ms
➜  Local:   http://localhost:5173/
```

---

## 🎉 完成！

现在您可以：
1. 运行 `.\install.ps1` 安装依赖
2. 双击 `run.bat` 启动项目
3. 访问 http://localhost:5173

**就这么简单！** ✨
