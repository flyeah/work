# 数据结构

数据结构(data structure)是带有结构特性的数据元素的集合，它研究的是数据的逻辑结构和数据的物理结构以及它们之间的相互关系，并对这种结构定义相适应的运算，设计出相应的算法，并确保经过这些运算以后所得到的新结构仍保持原来的结构类型。简而言之，数据结构是相互之间存在一种或多种特定关系的数据元素的集合，即带“结构”的数据元素的集合。“结构”就是指数据元素之间存在的关系，分为逻辑结构和存储结构。 [2]   

数据的逻辑结构和物理结构是数据结构的两个密切相关的方面，同一逻辑结构可以对应不同的存储结构。算法的设计取决于数据的逻辑结构，而算法的实现依赖于指定的存储结构。 [2]   

数据结构的研究内容是构造复杂软件系统的基础，它的核心技术是分解与抽象。通过分解可以划分出数据的3个层次；再通过抽象，舍弃数据元素的具体内容，就得到逻辑结构。类似地，通过分解将处理要求划分成各种功能，再通过抽象舍弃实现细节，就得到运算的定义。上述两个方面的结合可以将问题变换为数据结构。这是一个从具体（即具体问题）到抽象（即数据结构）的过程。然后，通过增加对实现细节的考虑进一步得到存储结构和实现运算，从而完成设计任务。这是一个从抽象（即数据结构）到具体（即具体实现）的过程。 [3]  

## 研究对象

数据的逻辑结构  
指反映数据元素之间的逻辑关系的数据结构，其中的逻辑关系是指数据元素之间的前后间关系，而与他们在计算机中的存储位置无关。逻辑结构包括： [1]   
1.集合：数据结构中的元素之间除了“同属一个集合” 的相互关系外，别无其他关系； [1]   
2.线性结构：数据结构中的元素存在一对一的相互关系； [1]   
3.树形结构：数据结构中的元素存在一对多的相互关系； [1]   
4.图形结构：数据结构中的元素存在多对多的相互关系。 [1]   

数据的物理结构  

指数据的逻辑结构在计算机存储空间的存放形式。 [1]   
数据的物理结构是数据结构在计算机中的表示（又称映像），它包括数据元素的机内表示和关系的机内表示。由于具体实现的方法有顺序、链接、索引、散列等多种，所以，一种数据结构可表示成一种或多种存储结构。 [1] 
数据元素的机内表示（映像方法）： 用二进制位（bit）的位串表示数据元素。通常称这种位串为节点（node）。当数据元素有若干个数据项组成时，位串中与个数据项对应的子位串称为数据域（data field）。因此，节点是数据元素的机内表示（或机内映像）。 [1] 
关系的机内表示（映像方法）：数据元素之间的关系的机内表示可以分为顺序映像和非顺序映像，常用两种存储结构：顺序存储结构和链式存储结构。顺序映像借助元素在存储器中的相对位置来表示数据元素之间的逻辑关系。非顺序映像借助指示元素存储位置的指针（pointer）来表示数据元素之间的逻辑关系。 [1] 

数据存储结构  

数据的逻辑结构在计算机存储空间中的存放形式称为数据的物理结构(也称为存储结构)。一般来说，一种数据结构的逻辑结构根据需要可以表示成多种存储结构，常用的存储结构有顺序存储、链式存储、索引存储和哈希存储等。 [4]   
数据的顺序存储结构的特点是：借助元素在存储器中的相对位置来表示数据元素之间的逻辑关系；非顺序存储的特点是：借助指示元素存储地址的指针表示数据元素之间的逻辑关系  

## 常用的数据结构

  数组(Array)  
  
  数组是一种聚合数据类型，它是将具有相同类型的若干变量有序地组织在一起的集合。数组可以说是最基本的数据结构，在各种编程语言中都有对应。一个数组可以分解为多个数组元素，按照数据元素的类型，数组可以分为整型数组、字符型数组、浮点型数组、指针数组和结构数组等。数组还可以有一维、二维以及多维等表现形式。 [5]   
  
  栈( Stack)  
  
  栈是一种特殊的线性表，它只能在一个表的一个固定端进行数据结点的插入和删除操作。栈按照后进先出的原则来存储数据，也就是说，先插入的数据将被压入栈底，最后插入的数据在栈顶，读出数据时，从栈顶开始逐个读出。栈在汇编语言程序中，经常用于重要数据的现场保护。栈中没有数据时，称为空栈。 [5]   
  
  队列(Queue)  
  
  队列和栈类似，也是一种特殊的线性表。和栈不同的是，队列只允许在表的一端进行插入操作，而在另一端进行删除操作。一般来说，进行插入操作的一端称为队尾，进行删除操作的一端称为队头。队列中没有元素时，称为空队列。 [5]   
  
  链表( Linked List)  
  
  链表是一种数据元素按照链式存储结构进行存储的数据结构，这种存储结构具有在物理上存在非连续的特点。链表由一系列数据结点构成，每个数据结点包括数据域和指针域两部分。其中，指针域保存了数据结构中下一个元素存放的地址。链表结构中数据元素的逻辑顺序是通过链表中的指针链接次序来实现的。 [5]   
  
  树( Tree)  
  
  树是典型的非线性结构，它是包括，2个结点的有穷集合K。在树结构中，有且仅有一个根结点，该结点没有前驱结点。在树结构中的其他结点都有且仅有一个前驱结点，而且可以有两个后继结点，m≥0。 [5]   
  
  图(Graph)  
  
  图是另一种非线性数据结构。在图结构中，数据结点一般称为顶点，而边是顶点的有序偶对。如果两个顶点之间存在一条边，那么就表示这两个顶点具有相邻关系。 [5]   
  
  堆(Heap)  
  
  堆是一种特殊的树形数据结构，一般讨论的堆都是二叉堆。堆的特点是根结点的值是所有结点中最小的或者最大的，并且根结点的两个子树也是一个堆结构。 [5]   
  
  散列表(Hash)  
  
  散列表源自于散列函数(Hash function)，其思想是如果在结构中存在关键字和T相等的记录，那么必定在F(T)的存储位置可以找到该记录，这样就可以不用进行比较操作而直接取得所查记录。 [5]   
  
  ## 二叉树
  二叉树、平衡二叉树、前序遍历、后序遍历
  
  
