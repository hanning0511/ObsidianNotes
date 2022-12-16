### eBPF 简介

eBPF (extended Berkeley Packet Filter) 是一种可以在 Linux 内核中运行用户编写的程序，而不需要修改内核代码或加载内核模块的技术。

简单说，eBPF 让 Linux 内核变得可编程化了。

eBPF 程序是一个事件驱动模型。Linux 内核提供了各种 hook point，比如 system calls, function entry/exit, kernel tracepoints, network events 等。

eBPF 程序通过实现想要关注的 hook point 的 callback，并把这些 callback 注册到相应的 hook point 来完成“内核编程”。

### eBPF 程序的执行流程

