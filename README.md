## Rust 学习

### 1.Cargo
Cargo 是Rust 的构建系统和包管理工具(构建代码、下载依赖库)

1. 创建项目 `cargo new hello_cargo`

2. `Cargo.toml`  是cargo的配置格式

   ```toml
   [package] #区域标题，表示下方内容是用来配置包(package)的
   name = "hello_cargo" #项目名
   version = "0.1.0"  #项目版本
   edition = "2021"  #使用的Rust版本
   
   # See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html
   
   [dependencies] #另一个区域的开始，它会列出项目的依赖项
   
   ```

   在Rust中，代码的包称为crate

3. `cargo build` 创建可执行文件，第一次运行`cargo build`会在顶层目录生成`cargo.lock`文件。该文件负责追踪项目以来的精确版本，不需要手动修改该文件。

4. `cargo run` 构建和运行`cargo` 项目 （编译代码+执行文件）

5. `cargo check` 检查代码，确保能通过编译，但是不产生任何可执行文件，使用`cargo check `检查代码，提高效率。

6. `cargo build --release` 为 发布构建，编译时会进行优化。

