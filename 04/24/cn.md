那个夏天我一边舔舐伤口，一边继续着demo里的工作。
巴特勒·拉姆泼逊（Butler Lampson）、彼得·多伊奇（Peter Deutsh）和我想出了一个方案来模拟[HLL机器语言](http://baike.baidu.com/item/hll#3)。
那时我推崇B5000的方案，但巴特勒不想给字节解码，他还指出既然8比特有256种编号的可能性，那么我们理当做的就是为“指令空间（instruction space）”里不同的部分赋予不同的意义。
最终，我们会创造出一种“穷人的[哈夫曼编码](http://baike.baidu.com/item/%E5%93%88%E5%A4%AB%E6%9B%BC%E7%BC%96%E7%A0%81)（poor man's Huffman code）”，它的身上兼具了灵活与简洁两种特性。
后来，这个方案应用在了帕克中心所有的模拟器上。

