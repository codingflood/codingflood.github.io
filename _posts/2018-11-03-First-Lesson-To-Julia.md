---
title: julia基础第一课

author: Ａlgar

date: 2018-11-03

---

## julia基础操作

1.运行julia

> 打开终端键入julia回车，出现如图所示界面：

![open julia](/assets/img/fltjulia1.png)

> 或者，在文本编辑器中写好代码，把文件保存为.jl格式，然后在打开终端进入文件所在文件夹，然后在终端中键入:julia 文件名.jl回车，即可按文件编辑好的代码运行。

2.退出julia

> 按住control然后按d键，或者键入exit()回车退出

3.代码运行

- 在终端中打开Julia运行

![run in terminator](/assets/img/LJulia1.png)

- 直接在终端shell界面运行脚本，视脚本内容而定，脚本后面可以带多个参数，注意空格是英文状态下输入的空格

```
    julia script.jl arg1 arg2 ...
```

>例如，把收下内容保存为hello.jl

```
    for a in ARGS
        println(a, "，今天过来喝酒吧！")
    end
```

>然后打终端进入文件所在目录

![hello.jl](/assets/img/LJulia2.png)

- 在终端shell界面直接计算或运行表达式

```
    julia -e 'println(PROGRAM_FILE); for x in ARGS; println(x); end' Hello world "Hello world"
```
![helloworld](/assets/img/LJulia3.png)

4.Julia中命令选项及其代表意义

- 示例格式

```
    julia [switches] -- [programfile] [args...]
```

- 详细列表


<table border="1">
    <tr bgcolor="Beige">
        <th>Switch</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>-v, --version</td>
        <td>显示版本信息</td>
    </tr>
    <tr bgcolor="Azure">
        <td>-h, --help</td>
         <td>输出帮助信息</td>
    </tr>
    <tr>
        <td>-J, --sysimage &lt;file&gt;</td>
        <td>以指定的系统映像文件启动</td>
    </tr>
    <tr bgcolor="Azure">
        <td>-H, --home &lt;dir&gt;</td>
        <td>设定julia可执行文件目录</td>
    </tr>
    <tr>
        <td>--startup-file={yes|no}</td>
        <td>是否载入~/.julia/config/startup.jl</td>
    </tr>
    <tr bgcolor="Azure">
        <td>--handle-signals={yes|no}</td>
        <td>启用或关闭信号处理程序</td>
    </tr>
    <tr>
        <td>--sysimage-native-code={yes|no}</td>
        <td>如可用，使用或不用系统映像中的编译好的代码</td>
    </tr>
    <tr bgcolor="Azure">
        <td>--compiled-modules={yes|no}</td>
        <td>启用或关闭增量预编译模块</td>
    </tr>
    <tr>
        <td>-e, --eval &lt;expr&gt;</td>
        <td>计算表达式</td>
    </tr>
    <tr bgcolor="Azure">
        <td>-E, --print &lt;expr&gt;</td>
        <td>计算表达式并输出结果</td>
    </tr>
    <tr>
        <td>-L, --load &lt;file&gt;</td>
        <td>立即向所有进程加载给定文件</td>
    </tr>
    <tr bgcolor="Azure">
        <td>-p, --procs {N|auto}</td>
        <td>发起整数Ｎ个附加本地工作进程，或依本地cpu线程数（逻辑核心数）自动发起</td>
    </tr>
    <tr>
        <td>--machine-file &lt;file&gt;</td>
        <td>在文件指定的各主机中运行进程</td>
    </tr>
    <tr bgcolor="Azure">
        <td>-i</td>
        <td>交互模式，交互解析器运行，并且为isinteractive()真</td>
    </tr>
    <tr>
        <td>-q, --quiet</td>
        <td>静默启动：无标语和交互解析器警告</td>
    </tr>
    <tr bgcolor="Azure">
        <td>--banner={yes|no|auto}</td>
        <td>启用或关闭“启动标语,或系统自动处理”</td>
    </tr>
    <tr>
        <td>--color={yes|no|auto}</td>
        <td>使用或不使用彩色文本，或系统自动处理</td>
    </tr>
    <tr bgcolor="Azure">
        <td>--history-file={yes|no}</td>
        <td>载入或保存历史文件</td>
    </tr>
    <tr>
        <td>--depwarn={yes|no|error}</td>
        <td>使用或不使用语法和方法的弃用特征警告,或用error把警告提示转为错误提示</td>
    </tr>
    <tr bgcolor="Azure">
        <td>--warn-overwrite={yse|no}</td>
        <td>启用或关闭方法覆盖警告</td>
    </tr>
    <tr>
        <td>-C, --cpu-target &lt;target&gt;</td>
        <td>由目标设备限制CPU使用特性，julia -C help参见可操作选项</td>
    </tr>
    <tr bgcolor="Azure">
        <td>-O, --optimize={0,1,2,3}</td>
        <td>设置优先级，默认为２，不设定则为３</td>
    </tr>
    <tr>
        <td>-g, -g &lt;level&gt;</td>
        <td>设置调试信息生成的级别，默认为１，２则为不设</td>
    </tr>
    <tr bgcolor="Azure">
        <td>--inline={yes|no}</td>
        <td>控制是否允许内联，包括方法重写</td>
    </tr>
    <tr>
        <td>--check-bounds={yes|no}</td>
        <td>Emit bounds checks always or never (ignoring declarations)</td>
    </tr>
    <tr bgcolor="Azure">
        <td>--math-mode={ieee,fast}</td>
        <td>Disallow or enable unsafe floating point optimizations (overrides @fastmath declaration)</td>
    </tr>
    <tr>
        <td>--code-coverage={none|user|all}</td>
        <td>Count executions of source lines</td>
    </tr>
    <tr bgcolor="Azure">
        <td>--code-coverage</td>
        <td>equivalent to --code-coverage=user</td>
    </tr>
    <tr>
        <td>--track-allocation={none|user|all}</td>
        <td>Count bytes allocated by each source line</td>
    </tr>
    <tr bgcolor="Azure">
        <td>--track-allocation</td>
        <td>equivalent to --track-allocation=user</td>
    </tr>
</table>


---

 相关资源列表及在线教程见[https://julialang.org/learning/](https://julialang.org/learning/)

