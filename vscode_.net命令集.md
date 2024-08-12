# 所需扩展

- C# Dev Kit
- Material Icon Theme
- NuGet Gallery
- SQLite

## NuGet:

- Core.Design

- Core.SQLite

- AspNetCore

- # 1.0如何用vscode创建.net项目

### 1.1创建目录并进入该目录
`mkdir name`
`cd name`

### 1.2创建解决方案文件 .sln
`dotnet new sln`

### 1.3创建 ASP.NET Core Web API 项目
```bash
dotnet new webapi -n API
```



### 1.4查看 dotnet sln 命令的帮助信息
dotnet sln -h

>使用法:
>  dotnet sln <SLN_FILE> [command] [options]
>
>引数:
>  <SLN_FILE>  操作するソリューション ファイル。指定しない場合、コマンドによって現在のディレクトリから検索されます。 [default: /Users/jiangwencheng/Documents/ASP_AngularLearn/DatingApp/]
>
>オプション:
>  -?, -h, --help  コマンド ラインのヘルプを表示します。
>
>コマンド:
>  add <PROJECT_PATH>     1 つ以上のプロジェクトをソリューション ファイルに追加します。
>  list                   ソリューション ファイル内のすべてのプロジェクトを一覧表示します。
>  remove <PROJECT_PATH>  1 つ以上のプロジェクトをソリューション ファイルから削除します。
>
>

### 1.5将项目 API/API.csproj 添加到解决方案中
```bash
dotnet sln add API
```



### 1.6列出解决方案中的所有项目
dotnet sln list

### 1.7用 Visual Studio Code 打开项目
code .

### 1.8运行项目
dotnet run

### 1.9列出可以创建的所有文件类型
dotnet new list

# 2.0项目中操作

## 2.1允许热加载

```bash
dotnet watch
```

**如果程序发生了问题记得回到终端检查一下原因**

## 2.2信任https

```bash
dev-certs https --trust
```


## 2.3安装数据库迁移工具----migration
```bash
dotnet tool install --global dotnet-ef
```


## 2.4生成第一个数据库迁移文件
```bash
dotnet ef migrations add InitialCreate -o Data/Miagrations
```

## 2.5dotnet ef

>Options:
>  --version        Show version information
>  -h|--help        Show help information
>  -v|--verbose     Show verbose output.
>  --no-color       Don't colorize output.
>  --prefix-output  Prefix output with level.
>
>Commands:
>
>```c#
>  database    Commands to manage the database.   dotnet ef database -h
>  dbcontext   Commands to manage DbContext types.
>  migrations  Commands to manage migrations.
>```
>
>Use "dotnet ef [command] --help" for more information about a command.



