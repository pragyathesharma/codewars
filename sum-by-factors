import java.util.*;
public class SumOfDivided {
  public static String sumOfDivided(int[] n) {
    TreeSet<Integer> set = new TreeSet<Integer>();
    for(int i = 0; i < n.length; i++)
    {
      int temp = Math.abs(n[i]);
      int divisor = 2;
      while(temp > 1)
      {
        if(temp%divisor==0)
        {
          set.add(divisor);
          temp/=divisor;
        }
        else divisor++;
      }
    }
    
    String answer = "";
    
    for(Integer num : set)
    {
      int sum = 0;
      answer+="(";
      for(int i = 0; i < n.length; i++)
      {
        if(n[i]%num==0)
          sum+=n[i];
      }
      answer+=num+" "+sum+")";
    }
    
    return answer;
  }
}
