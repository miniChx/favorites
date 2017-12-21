理解Math.random()随机数范围


Math.random() //系统默认随机数范围 0.0 ~ 0.9 之间的double值

 

/*
*注意错误使用方法
*当需要一个int型的随机数那么就(int)Math.random()这只能得到一个数  就是 0 
*/

 

// 需要int型的 0 ~ x (x为任意大于0的整数)范围的随机数
// 需要0到某个数n的范围 就是Math.random()*(n+1)           
// 0 ~ 5 之间 就是乘以6
(int)(Math.random() * 6);    //注意：不能写成(int)Math.random() * 5  这样将永远得到0
// 0 ~ 3 之间 就是乘以4
(int)(Math.random() * 4);

 

// 需要int型的 1 ~ x(x为任意大于1的整数)范围的随机数
// 需要1到某个数n的范围 就是Math.random()*n + 1 
// 1 ~ 5 之间 就是乘以5加1
(int)(Math.random() * 5 + 1);    //注意：不能写成(int)Math.random() * 5 + 1 这样将永远得到1
// 1 ~ 3 之间 就是乘以3加1
(int)(Math.random() * 3 + 1);

//如果在需要别的范围的就需要用if来筛选了
while(true){
  int num = (int)(Math.random() * 6 + 1);   //  1 ~ 6 之间
  if(num > 2){                          //筛选出 3 ~ 6 之间的数
    System.out.println(num);
  }
}
