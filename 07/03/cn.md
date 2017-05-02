有一种方式来思考软件发展：大部分软件设计都是为了想办法进行后期绑定（late-bind），然后说服制造商将这些想法融入硬件中去。
早期硬件有联网的程序和参数，随机存取内存能够对其进行后期绑定。
过去，计算机循环（looping）与标引（indexing）都由存储中的地址修改（address modification）完成。
数年来软件设计师们已经找出了各种各样的方法来对计算位置进行后期绑定——这就衍生出了[变址寄存器（base register）](http://baike.baidu.com/item/%E5%8F%98%E5%9D%80%E5%AF%84%E5%AD%98%E5%99%A8)/界限暂存器（bound register）、段落迁移（segement relocation）、页面[MMU](http://baike.baidu.com/item/MMU)、迁移程序（migratory process）等。
由于“效率低下”，分时（time-sharing）系统也停滞了多年——然而制造商并不会将MMU置入机器，因此大学需要自食其力！
递归将参数后期绑定在这些过程中，但在CPU中放入哪怕是最基本的堆栈机制也花费了数年时间。
大部分机器也还不具备动态配置（dynamic allocation）与[垃圾回收（garbage collection）](http://baike.baidu.com/item/GC/66426)等功能。
总体说来，目前大多数硬件设计只是在过去粗制滥造的基础上进行了重新优化。
