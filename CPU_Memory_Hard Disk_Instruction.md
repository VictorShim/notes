#CPU,内存,硬盘,指令以及他们的关系
##CPU
1. cpu的工作就是运行指令
2. cpu的指令保存在缓存(cache)或内存中(缓存位于CPU中，速度远比内存快，由于程序的局部性原理所以缓存的命中率较高，可以有效提高处理速度)
3. cpu的第一条指令在内存的最顶端处

##内存
1. 内存用于存放指令供CPU使用
2. 内存相对CPU缓存慢了许多，但是相对硬盘快了许多
3. 内存是易失性存储，断电后数据消失

##硬盘
1. 硬盘容量大，速度慢，价格便宜
2. 硬盘是非易失性存储，断电后数据仍保存在硬盘中

##指令
1. 在传统架构上，指令包括一个操作码--它指定了要进行什么样的操作
操作数--它可能指定了参与操作的寄存器，内存地址或者立即数。操作数可能还包括寻址方式。

##总结
* 计算机中有多种存放数据和指令代码的单元，比如在CPU内的寄存器（register）、高速缓存(cache)、内存（memory）、硬盘等。寄存器访问速度最快但成本昂贵；高速缓存（cache） 一般也在CPU内部，比寄存器慢2~10倍，容量也有限，量级大约几百KB到几十MB不等；再接下来就是内存了，内存位于CPU外，比寄存器慢10倍以上，但容量大，目前一般以几GB到几百GB不等；硬盘容量更大，但一般比寄存器要慢1000倍以上，不过掉电后其存储的数据不会丢失**( PS:INTEL最新的Optane非易失性内存的速度已经接近DRAM内存，容量可达上百GB，详情可参考[INTEL官方网站介绍](http://www.intel.cn/content/www/cn/zh/architecture-and-technology/optane-memory.html)。)**
* 由于寄存器、cache、内存、硬盘在读写速度和容量上的巨大差异，所以需要操作系统来协调数据的访问，把经常访问的数据放在内存中，把不常用的数据放到硬盘上，这样可以达到使用效率更高的同时访问速度相对更快。