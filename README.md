# coderByte_MediumProblem
simpleMode
import java.util.*; 
import java.io.*;

class Main {

  public static int SimpleMode(int[] arr) {
    // code goes here
    int length =arr.length;
    //System.out.println(arr.length);
    int count2=0;
    int mode=0;
    for(int i =0; i<length; i++){

      int count =0;

      for(int j =i+1; j<length; j++){
         if(arr[i]==arr[j]){
           count++;
      }
      if(count>count2){
        mode = arr[i];
        count2=count;
      }
      }   
    }
    if(count2==0){
      return -1;
    }
      return mode;
  }

  public static void main (String[] args) {  
    // keep this function call here     
    Scanner s = new Scanner(System.in);
    System.out.print(SimpleMode(s.nextLine())); 
  }

}
