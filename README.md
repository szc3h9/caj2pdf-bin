# README

caj2pdf 是一个用于将 CAJ 文件转换为 PDF 的命令行工具。项目采用 AI 辅助开发方式进行实现，当前仓库只提供已编译的二进制文件，不提供源代码公开下载。

## 项目说明

- 工具名称：`caj2pdf`
- 功能：将 `.caj` 文件转换为 `.pdf`
- 当前版本：`0.1.1`
- 更新内容：支持传统 CAJ 对象片段重建 PDF，解析 CAJ 头部索引与 PDF 对象片段，补建唯一根页树、Catalog 和 xref
- 开发方式：AI 辅助开发
- 源代码状态：源代码未开源
- 二进制文件：已编译程序可免费使用

> 说明：当前仓库仅包含可执行文件，不包含完整源码工程。若您使用的是本仓库中的二进制版本，可直接运行命令进行转换。

---

## 目录结构

```text
caj2pdf-bin/
├── caj2pdf-0.1.1-windows-x64.exe
├── caj2pdf-0.1.1-x86_64-unknown-linux-musl
└── README.md
```

---

## 可用文件

### Windows

```text
caj2pdf-0.1.1-windows-x64.exe
```

### Linux

```text
caj2pdf-0.1.1-x86_64-unknown-linux-musl
```

---

## 命令行使用说明

### 基本语法

```bash
caj2pdf [--force] <input.caj> [output.pdf]
```

### 参数说明

- `--force` / `-f`：覆盖已存在的输出文件
- `-h` / `--help`：显示帮助信息
- `-V` / `--version`：显示版本号和构建时间
- `--copyright`：显示版权信息、版本号和构建时间

---

## 使用教程

### 1. 查看帮助

#### Windows

```powershell
.\caj2pdf-0.1.1-windows-x64.exe --help
```

#### Linux

```bash
./caj2pdf-0.1.1-x86_64-unknown-linux-musl --help
```

输出示例：

```text
Usage: caj2pdf [--force] <input.caj> [output.pdf]

Options:
  -f, --force      Replace an existing output file
  -h, --help       Show this help
  -V, --version    Show version and build time
      --copyright  Show version, copyright, and build time
```

### 2. 转换单个 CAJ 文件

#### Windows

```powershell
.\caj2pdf-0.1.1-windows-x64.exe .\input.caj
```

说明：如果未指定输出文件名，程序会自动使用同名的 PDF 文件名生成输出。

#### Linux

```bash
./caj2pdf-0.1.1-x86_64-unknown-linux-musl ./input.caj
```

### 3. 指定输出 PDF 路径

#### Windows

```powershell
.\caj2pdf-0.1.1-windows-x64.exe .\input.caj .\output\result.pdf
```

#### Linux

```bash
./caj2pdf-0.1.1-x86_64-unknown-linux-musl ./input.caj ./output/result.pdf
```

### 4. 覆盖已有文件

如果目标 PDF 已存在，若不使用 `--force`，程序可能无法覆盖原文件。

#### Windows

```powershell
.\caj2pdf-0.1.1-windows-x64.exe --force .\input.caj .\output\result.pdf
```

#### Linux

```bash
./caj2pdf-0.1.1-x86_64-unknown-linux-musl --force ./input.caj ./output/result.pdf
```

### 5. 查看版本信息

#### Windows

```powershell
.\caj2pdf-0.1.1-windows-x64.exe --version
```

#### Linux

```bash
./caj2pdf-0.1.1-x86_64-unknown-linux-musl --version
```

---

## 示例流程

```powershell
# 进入目录
cd .	ools

# 转换 CAJ 文件
.\caj2pdf-0.1.1-windows-x64.exe .\book.caj .\book.pdf
```

转换完成后，`book.pdf` 即可直接打开查看。

---

## 适用场景

- 电子书/教材 CAJ 格式转 PDF
- 需要批量导出 CAJ 文档内容时使用
- Windows / Linux 环境下的轻量命令行转换

---

## 免责声明

- 本项目仅提供已编译好的二进制可执行文件，供免费使用。
- 源代码未公开，不在本仓库中提供源码工程文件。
- 使用者需遵守各自环境、文件版权和合法使用要求。

---

## 备注

如果你需要进一步扩展这个工具，例如：

- 增加批量转换脚本
- 支持批量目录遍历
- 增加日志输出
- 自动化 Windows / Linux 安装脚本

可以继续在这个项目基础上扩展功能。
