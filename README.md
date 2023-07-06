**
 2  * 需求分析：从键盘输入5名学员某门课程的笔试成绩，并求出五门成绩的总成绩和平均成绩
 3  * @author chenyanlong
 4  * 日期：2017/10/14
 5  */
 6 package com.hp.test05;
 7 
 8 import java.util.Scanner;
 9 
10 public class HS_Array1 {
11 
12     public static void main(String[] args) {
13         // TODO Auto-generated method stub
14         System.out.println("请输入5个学生的笔试成绩：");
15         
16         double sum=0;
17         double avg;
18         int[] scores = new int[6];
19         Scanner input=new Scanner(System.in);
20         //输入5个成绩
21         for(int i=0;i<5;i++){
22             
23             scores[i]=input.nextInt();
24         }
25         //求和
26         for(int j=0;j<5;j++){
27             sum=sum+scores[j];
28         }
29         System.out.println("总成绩:"+sum);
30         //平均分
31         avg=sum/5;
32         System.out.println("平均分:"+avg);           
33     }
34 }
复制代码
复制代码
 1 /**
 2  * 需求分析： 从键盘输入5名学员某门课程的笔试成绩，
 3  * 并求出五门成绩的最高分、最低分和平均分
 4  * @author chenyanlong
 5  * 日期：2017/10/14
 6  */
 7 package com.hp.test05;
 8 
 9 import java.util.Scanner;
10 
11 public class HS_Array2 {
12 
13     public static void main(String[] args) {
14         
15         int[] scores=new int[5];
16         int sum=0;
17       
18         double avg;
19         System.out.println("请输入5个成绩");
20         
21         Scanner input=new Scanner(System.in);
22         for(int i=0;i<scores.length;i++){           
23             scores[i]=input.nextInt();
24         }
25         //总成绩，最高分，最低分
26         int max=scores[0];
27         int min=scores[0];
28         for(int j=0;j<scores.length;j++){
29             //总成绩
30             sum +=scores[j];
31             //最低分
32             if(scores[j]<min){
33                 min=scores[j];
34             }
35             //最低分
36             if(scores[j]>max){
37                 max=scores[j];
38             }
39         }
40         avg=sum/scores.length;
41         System.out.println("总成绩:"+sum);
42         System.out.println("最高分："+max);
43         System.out.println("最低分："+min);
44         System.out.println("平均分："+avg);
45             
46     }
47 }
复制代码
复制代码
 1 /**
 2  * 需求分析： 用二维数组存放三个班学生的成绩，并计算三个班学生的总成绩    
 3  * @author chenyanlong
 4  * 日期：2017/10/14
 5  */
 6 package com.hp.test05;
 7 
 8 import java.util.Arrays;
 9 import java.util.Scanner;
10 
11 public class HS_Array3 {
12 
13     public static void main(String[] args) {
14         
15         int[][] array=new int[][]{{2,1},{2,1,3},{2,1}};
16         for(int i=0;i<array.length;i++){
17             String str=(i+1)+"班";
18             Arrays.sort(array[i]);
19             System.out.println(str+"排序以后");
20             for(int j=0;j<array[i].length;j++){
21                 System.out.println(array[i][j]);
22             }
23         }
24     }
25 }


