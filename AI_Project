
package ai_project;

import java.util.Scanner;

/**
 *
 * @author Seif
 */
public class AI_Project {
        static int[] X = new int[]{3,3,3,4,4,5,5,7,7,8};
        static int []Y = new int[]{4,6,8,5,7,1,5,3,5,5};
        static int []cluster1X =  new int[10];
        static int []cluster1Y =  new int[10];
        static int []cluster2X =  new int[10];
        static int []cluster2Y =  new int[10];
        static int iterations=1;
        
    public  static void main(String[] args) {
       // m1(3,4) m2(8,5)
       double x1=3 , x2=8 , y1=4 , y2=5;
       
       Scanner scan = new Scanner(System.in);
       System.out.println("enter 1 for euclidian distance or 2 for manhattan: ");
       String method = scan.next();
       int MethodNumber = Integer.parseInt(method);
       
       if(MethodNumber == 1){
           Euclidian(x1 , x2 , y1 , y2);  
       } 
       else if (MethodNumber ==2){
           
           Manhattan(x1 , x2 , y1 , y2); 
       }
          
       }
        
     public  static void Euclidian(double x1 ,double x2 , double y1 , double y2)
     {
         
         double AnswerM1 , AnswerM2;
           double sumX = 0;
           double sumY = 0;
           double sumX2 = 0;
           double sumY2 = 0;
           int count1 =0;
           int count2=0;
           double avgX=0.0;
           double avgY=0.0;
           double avgX2=0.0;
           double avgY2=0.0;
          for (int i=0;i<10;i++){
           AnswerM1 = Math.sqrt(Math.pow(X[i]-x1 , 2) + Math.pow(Y[i]-y1,2));
           AnswerM2 = Math.sqrt(Math.pow(X[i]-x2 , 2) + Math.pow(Y[i]-y2,2));
           
           if (AnswerM1<AnswerM2)
           {    
               cluster1X[count1] = X[i];
               cluster1Y[count1] = Y[i];
               count1++;
           }
           else{
               
               cluster2X[count2] = X[i];
               cluster2Y[count2] = Y[i];
               count2++;
           }
          }
           for (int i=0 ; i<count1;i++){
               sumX+= cluster1X[i];
           }
           for (int i=0 ; i<count1;i++){
               sumY+= cluster1Y[i];
           }
           
           for (int i=0 ; i<count2;i++){
               sumX2+= cluster2X[i];
           }
           for (int i=0 ; i<count2;i++){
               sumY2+= cluster2Y[i];
           }
           Double Dcount2 = new Double(count2);
           avgX2 = sumX2/Dcount2;
           avgY2 = sumY2/Dcount2;
           
           
           Double Dcount1 = new Double(count1);
           avgX = sumX/Dcount1;
           avgY = sumY/Dcount1;
           
          if (avgX != x1 || avgY != y1 || avgX2 != x2 || avgY2 != y2)
          {
              System.out.println("Iteration : "+iterations+" ");
              System.out.println(" ");
              System.out.println("cluster 1: ");
              for(int i=0;i<count1;i++)
           {
               System.out.println(cluster1X[i] +" "+cluster1Y[i]+" ");
               
           }
              System.out.println(" ");
           System.out.println("cluster 2: ");
           for(int i=0;i<count2;i++)
           {
               System.out.println(cluster2X[i] +" "+cluster2Y[i]+" ");
               
           }
           System.out.println("New M's");
            System.out.println(avgX+" "+avgY+" "+avgX2+" "+avgY2+" ");
            System.out.println(" ");
              iterations++;
              
            Euclidian(avgX , avgX2 , avgY , avgY2);
          }

     }
     public  static void Manhattan(double x1 ,double x2 , double y1 , double y2)
     {
         int iterations=1;
         double AnswerM1 , AnswerM2;
           double sumX = 0;
           double sumY = 0;
           double sumX2 = 0;
           double sumY2 = 0;
           int count1 =0;
           int count2=0;
           double avgX=0.0;
           double avgY=0.0;
           double avgX2=0.0;
           double avgY2=0.0;
          for (int i=0;i<10;i++){
           AnswerM1=Math.abs(X[i]-x1)+Math.abs(Y[i]-y1);
           AnswerM2=Math.abs(X[i]-x2)+Math.abs(Y[i]-y2);
           if (AnswerM1<AnswerM2)
           {    
               cluster1X[count1] = X[i];
               cluster1Y[count1] = Y[i];
               count1++;
           }
           else{
               
               cluster2X[count2] = X[i];
               cluster2Y[count2] = Y[i];
               count2++;
           }
          }
           for (int i=0 ; i<count1;i++){
               sumX+= cluster1X[i];
           }
           for (int i=0 ; i<count1;i++){
               sumY+= cluster1Y[i];
           }
           
           for (int i=0 ; i<count2;i++){
               sumX2+= cluster2X[i];
           }
           for (int i=0 ; i<count2;i++){
               sumY2+= cluster2Y[i];
           }
           Double Dcount2 = new Double(count2);
           avgX2 = sumX2/Dcount2;
           avgY2 = sumY2/Dcount2;
           
           
           Double Dcount1 = new Double(count1);
           avgX = sumX/Dcount1;
           avgY = sumY/Dcount1;
           
          if (avgX != x1 || avgY != y1 || avgX2 != x2 || avgY2 != y2)
          {
              System.out.println("Iteration : "+iterations+" ");
              System.out.println(" ");
              System.out.println("cluster 1: ");
              for(int i=0;i<count1;i++)
           {
               System.out.println(cluster1X[i] +" "+cluster1Y[i]+" ");
               
           }
              System.out.println(" ");
           System.out.println("cluster 2: ");
           for(int i=0;i<count2;i++)
           {
               System.out.println(cluster2X[i] +" "+cluster2Y[i]+" ");
               
           }
           System.out.println("New M's");
            System.out.println(avgX+" "+avgY+" "+avgX2+" "+avgY2+" ");
            System.out.println(" ");
              iterations++;
              
            Manhattan(avgX , avgX2 , avgY , avgY2);
          }
     }
}
