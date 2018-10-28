# principlesOfcomputer
#### 计算机系统：硬件->计算机的实体，如主句、外设等 。软件->由具有各类特殊功能的信息（程序）组成。
#### 软件：系统软件-> 用来管理整个计算机系统，语言处理程序、操作系统、服务型程序（天河2里的数学库）、数据库管理系统、网络软件。应用软件->按任务需要编织成的各种程序。
#### 简单的一个层次结构 软件、硬件=>应用软件、系统软件、硬件
#### 计算机系统的层次结构
     高级语言：虚拟机器（m4）-> 用编译程序翻译成汇编语言程序 
     汇编语言：虚拟机器（m3) -> 用汇编程序翻译成机器语言程序 
     操作系统：虚拟机器 (m2) -> 用机器语言解释操作系统
     机器语言：实际机器（m1）-> 用微指令解释机器指令
     微指令系统: 微程序机器（m0）-> 有硬件直接执行微指令
     m4->m3->m2->m1->m0 
#### 系统复杂性管理的方法
#### 抽象
     抽象->对于一个过程或者一件制品的某些细节有目的的隐藏，以便把其他方面、细节或者结构表达得更加清楚---百度百科
     抽象->指高级的模型，和低级的实体相对---维基百科
     抽象->隐藏系统中不重要的细节--- David harris
### 计算机组成与计算机体系结构从研究内容上有什么区别？ 
#### 计算机体系结构
     程序员所见到的计算机系统的属性改脸型的结构与功能特性
     (指令系统、数据类型、寻址技术、I/0机理)
#### 计算机组成
     实现计算机体系结构所体现的属性
     (具体指令的实现)
### 计算机的基本组成 
#### 冯.诺依曼计算机的特点  
     计算机由五大部件组成 运算器 控制器 存储器 输入设备 输出设备
     指令和数据以同等地位存于存储器，可按地址寻访
     指令和数据用二进制表示
     指令由操作码和地址码组成
     存储程序  
     以运算器位中心 
### 现代计算机硬件框图
#### 系统复杂化管理的方法-2（3Y）
     层次化：将被设计的系统划分为多个模块或子模块 
     模块化：有明确定义的功能和接口
     规则性：模块更容易被重用  

#### 一个现实中的问题，如用计算机来解决？

#### 是不是所有的问题都可以用计算的方法来解决？                  
### 计算机的工作步骤
#### 上机前的准备
     建立数学模型
       u=UmSinwt
     确定计算方法
       sinx=x
     编程举例
       计算 ax²+bx+c=(ax+b)x+c
       取x 至运算器中  取x至运算器中
       乘以x在运算器中  乘以a在运算器中
       乘以a在运算器中 加b在运算器中  
       存ax²在存储器中 乘以x在运算器中
       取b至运算器中   加c在运算器中
       乘以x在运算器中
       加ax²载运算器中
       加c在运算器中 
     指令格式举例
     取数
#### 存储器的基本组成
     存储体-存储单元-存储元件（0/1）
     大楼-房间-床位   （无人/有人）
     存储单元 存放一串二进制代码
     存储字 存储单元中二进制代码的组合、
     存储字长 存储单元中二进制代码的位数
     每个存储单元赋予一个地址           
     按地址寻访
     MAR 存储器地址寄存器
         反映存储大暖的个数
     MDR 存储器数据寄存器
         反映存储字长
#### 运算器的基本组成及操作过程 
     ALU
            ACC       MQ       X
     加法   被加数              加数
            和                 减数
     
     减法   被减数              减数    
            差

     乘法   乘积高位  乘数
                     乘积低位
     
     除法   被除数    商        除数
            余 
#### 控制器的基本组成
     完成一条指令->取指令 PC、分析指令 IR、执行指令 CU
     PC存放当前欲执行指令的地址，具有计数功能（PC）+1->pc
     IR 存放当前欲执行的指令
#### 主机完成一条指令的过程
     ax²+bx+c程序的运行过程
     将程序通过输入设备送至计算机
     程序首地址->PC
     启动程序运行
     取指令 PC->MAR->M->MDR->IR
     分析指令 IR->CU
     执行指令 IR->MAR->M->MDR->ACC
#### 计算机硬件的主要技术指标
     机器字长 CPU一次能处理数据的位数
              与CPU中的寄存器位数有关
     运算速度 主频、核数->每个核支持的线程数、吉普森法
             CPI-> 执行一条指令所需要时钟周期
             MIPS-> 每秒执行百万的指令 
             FLOPS-> 每秒浮点运算次数 

     存储容量 存放二进制信息的总位数 
     主存容量 存储单元个数*存储字长 
              如MAR MDR 容量
                10 8 1K*8位
                16 32 64K*32位 

             字节数
                    如
     辅存容量 字节数                
#### 什么是总线
     总线是连接各个部件的信息传输线，是各个部件共享的传输介质
#### 总线的分类
     1.片内总线 芯片内部的总线
     2.系统总线 计算机各部件之间的信息传输线
       数据总线 双向 与机器字长、存储字长有关
       地址总线 单向 与存储地址、I/O地址有关
       控制总线 有出 有入 
     3.通信总线 用于计算机系统之间或计算机系统与其他系统之间的通信
#### 总线特性
     1.机械特性  尺寸、形状、管脚数及排列顺序
     2.电气特性  传输方向和有效地电平范围
     3.功能特性  每根传输线的功能 地址、数据、控制
     4.时间特性  信号之间的时序关系
#### 总线的性能指标
     1.总线宽度          数据线的根数  
     2.标准传输率        每秒传输的最大字节数
     3.时钟同步/异步     同步、不同步
     4.总线复用          地址线与数据线复用
     5.信号线数          地址线、数据线和控制线的总和
     6.总线控制方式      突发、自动、仲裁、逻辑、计数
     7.其他指标          负载能力
#### 总线标准      
### 总线结构
#### 多总线结构
     1.双总线结构
     2.三总线结构 
### 总线控制  
#### 总线判优控制
     1.基本概念
     主设备（模块）对总线有控制权
     从设备（模块）响应从主设备发来的总线命令
     总线判优控制 
     集中式  链式查询 计数器定时查询 独立请求方式
     分布式

     链式查询
#### 总线通信控制
1.目的 解决通信双方协调配合问题
2.总线传输周期
  申请分配阶段 主模块申请，总线仲裁决定
  寻址阶段 主模块向从模块给出地址和命令
  传输阶段 主模块和从模块交换数据
  结束阶段  主模块撤销相关信息0
#### 总线通信的四种方式
   同步通信 由统一时标控制数据传送
   异步通信 采用应答方式，没有公共时钟标准
   半同步通信 同步、异步结合
       同步 发送方 用系统时钟前沿发信号
            接收方 用系统时钟后沿 判断、识别
       异步 允许不同速度的模块和谐工作
       增加一条“等待”响应信号

       T1 主模块发地址
       T2 主模块发命令
       Tw 当WAIT为低电平时，等待T
       Tw 当WAIT为低电平时，等待T
       .
       .
       .
       T3 从模块提供数据
       T4 从模块撤销数据，主模块撤销命令  
   分离式通信 充分挖掘系统总线每个瞬间 
       一个总线传输周期
       子周期1 主模块申请占用总线，使用完后既放弃总线的使用权
       子周期2 从模块申请占用总线，将各种信息送至线上
#### 以上三种通信的共同点
     一个总线传输周期（以输入数据为列）
     主模块发地址、命令  //占用总线
     从模块准备数据     // 不占用总线
     从模块箱主模块发送数据 //占用总线
#### 分离式通信特点 
     1.各模块有权申请占用总线
     2.采用同步方式通信，不等对方回答
     3.各模块准备数据时。不占用总线
     4.总线被占用时，无空闲
### 存储器
#### 存储器分类
     按存储介质分类
       半导体存储器 TTL、MOS 易失
       磁表面存储器 磁盘、载磁体
       磁芯存储器   硬磁材料、环状元件
       光盘存储器   激光、磁光材料
     按存取方式分类
       存取时间与物理地址无光（随机访问）
         随机存储器 在程序的执行过程中可读可写
         只读存储器 在程序的执行过程中只读  
       存取时间与物理地址有关（串行访问）
         顺序存取存储器 磁带
         直接存取存储器 磁盘
     按在计算机中作用分类
       主存储器
         ram
             静态RAM
             动态RAM 
         rom 
             MROM
             PROM
             EPROM
             EEPROM
       flash memory
       高速缓冲存储器（cache）
       辅助存储器  磁盘、磁带、光盘         
     存储器的层次结构
       存储器三个主要特性的关系
         速度 容量 价格
        寄存器、缓存、主存、磁盘、光盘、磁带
           速度       容量
        缓存-主存   主存-辅存
#### 主存的基本组成        
#### 主存中存储单元地址的分配
     设地址线24根 按字节寻址2^24=16MB
     若字长位16位 按字寻址8MW
     若字长位32位 按字寻址4MW
#### 主存的技术指标
      存储容量 主存 存放二进制代码的总位数
      存储速度
         存取时间  存储器的 访问时间  读出时间 写入时间
         存取周期  连续两次独立的存储器操作  
      存储器的带宽 位/秒 
#### 半导体存储芯片的基本结构 
      地址线（单向）数据线（双向） 芯片容量
       10            4             1K*4位
       14            1             16K*1位   
      片选线 CS CE
      读/写控制线 WE（低电平写 高电平读）
      OE（允许读）WE（允许写）
#### 半导体存储芯片的译码驱动方式
     线选法
       比较密集
     重合法 
#### 静态RAM
     保存0和1的原理是什么？
     基本单元电路的构成是什么？
     对单元电路如何读出和写入？
     典型芯片的结构是什么样子的？
     静态RAM芯片的如何进行读出和写入的操作？ 

#### 动态RAM和静态RAM的比较
                           DRAM               SRAM              
     存储原理               电容               触发器 
     集成度                 高                  低
     芯片引脚               少                  多
     功耗                   小                  大 
     价格                   低                  高
     速度                   慢                  快
     刷新                   有                  无



