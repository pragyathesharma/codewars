import java.util.*;
class DoubleLinear {
    
  public static int dblLinear (int n) {
      if(n==0) 
        return 1;
      TreeSet<Integer> set = new TreeSet<>();
      set.add(1);
      for (int i = 0; i < n; i++){
        int x = set.first();
        set.add(x*2+1);
        set.add(x*3+1);
        set.remove(x);
      }
      return set.first();
  }
}
