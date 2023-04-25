# proj182-xiaomi-nuttx-smp-scheduler
基于NuttX RTOS的符合POSIX规范和SMP系统的高效任务调度器实现


## 基于NuttX RTOS的符合POSIX规范和SMP系统的高效任务调度器实现

### 赛题地址

NA

### 赛题要点/解析

#### 项目介绍

##### 平台介绍

**关于Vela**：[Vela](https://iot.mi.com/vela)是小米公司基于开源实时操作系统NuttX打造的物联网嵌入式软件平台，Vela在各种物联网硬件平台上提供统一的软件服务，支持丰富的组件和易用的框架，用于打通碎片化的物联网应用场景。

**关于NuttX**：[NuttX](https://nuttx.apache.org/docs/latest/)是一个在IoT、分布式嵌入式系统、无人机系统中广泛使用的RTOS，第一个版本由 Gregory Nutt 于 2007 年发布。NuttX 可以支持 8 位到64位的处理器，支持risc-v，arm，mips，x86等主流芯片平台，按照POSIX和 ANSI 标准进行设计，支持MMU和MPU，支持多线程和进程。2019年NuttX在小米的推动下正式进入Apache基金会，小米多位资深工程师参与了 [NuttX社区](https://github.com/apache/incubator-nuttx) 的开发和架构设计。经过多年的不懈努力，NuttX功能丰富，性能稳定，商业化成熟度高，在各种物联网产品上得到了广泛的应用。

##### 项目意义

在RTOS领域，SMP多核系统下的任务调度策略是操作系统优化的重要主题，任务调度作为OS中最常发生的几个事件，提升调度系统的效率能够有效地提升系统的整体运行效率。 POSIX规范中给出了多核调度器的实现要求。本项目的目标是基于NuttX已有的多核支持，实现一个符合POSIX规范的多核调度器，进一步优化NuttX在SMP系统上的工作效率。

#### 功能点

注：所有功能点应能在K210板卡上运行并演示

• 符合POSIX规范，支持FIFO、RR、Sporadic调度策略

• 对称式调度器（每个核心维护自己的task list）or 其他更优的无锁实现

• 适配K210板卡，并考虑多平台的可扩展（ARM、Xtensa）

### 项目导师

• 黄齐，Bytecode Alliance RC / WAMR TSC Member , huangqi3@xiaomi.com

• 小米公司Vela研发团队（含NuttX社区主要代码提交人）

#### 难度

中高

#### 参考资料

• [https://nuttx.apache.org/docs/latest/](https://github.com/acoinfo/sylixos_oscomp_2021/tree/master/Dual-OS-OpenAMP) ：NuttX的最新文档，可以直接下载并按照要求配置和使用K210板卡

• https://github.com/apache/incubator-nuttx/tree/master/boards/risc-v/k210/maix-bit ：NuttX文档中对K210板卡的配置和使用说明

• https://pubs.opengroup.org/onlinepubs/009695399/functions/xsh_chap02_08.html ：Open Group关于调度策略的指导手册 ：

• https://github.com/apache/incubator-nuttx/tree/master/sched/sched

• https://nuttx.apache.org

• https://www.cs.uic.edu/~jbell/CourseNotes/OperatingSystems/5_CPU_Scheduling.html ：调度器的一些基本知识

#### 预期目标

注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

• 完成每个cpu core local的调度器，减少当前代码中全局锁的使用

### 对参赛队提供的支持

• NuttX的内核实现及改进方向

• 针对NuttX实时操作系统和Vela平台业界最专业权威的技术支持和指导
