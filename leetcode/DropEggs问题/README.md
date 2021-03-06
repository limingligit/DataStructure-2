###### 问题描述  
有两个鸡蛋，一栋楼，设楼的高度是height，在某一层以下，仍鸡蛋的时候，鸡蛋不会碎，但是从该层开始一直到height，仍鸡蛋的话，鸡蛋会碎，如何使用这两枚鸡蛋测试出这个临界层是哪层，要求仍鸡蛋的次数尽量少。  

---

###### 思路  

如果从一层开始逐层的测试，仍的次数，在最坏的情况下是height。  
为了减少仍的次数，可以让第一个鸡蛋增加一定的<strong>跳跃性</strong>。比如对于100层的楼，第一个鸡蛋从第10，20，30，...，90，100仍下去，假设鸡蛋在70层没碎，但是在80层碎了，这说明这个临界层就在：[71, 80]，然后用第二个鸡蛋从71一直试到80。  
在这种，增加了<strong>跳跃性</strong>的情况下，仍的次数最多是 (height / jump + jump)。