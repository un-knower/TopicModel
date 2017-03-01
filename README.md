LDA在Stream数据环境下遇到的两个主要的挑战：
---------
+ Stream数据的特点带来的挑战
    
    实时性，在线更新，动态增长的词表
    
+ 海量Data带来的挑战 （没有亮点）
    
    在Stream环境下短时间内有可能产生海量的数据，单机的程序往往无法快速实时地更新模型和作出即时的响应
+ LDA拥有大规模的参数矩阵(V\*K) -- stream参数服务器
  
    前面的两个挑战，迫使我们必须在分布式流式环境下实现LDA算法模型。然而LDA算法模型带有大规模的参数矩阵。这给动态实时更新过程中的参数同步带来新的挑战。因为，这么大规模的参数矩阵的同步更新会造成巨大的网络延迟，将会造成系统的性能瓶颈。