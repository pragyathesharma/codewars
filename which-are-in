import java.util.*;
public class WhichAreIn { 
	
	public static String[] inArray(String[] array1, String[] array2) {
      ArrayList<String> list = new ArrayList<String>();
      for(String word : array2)
      {
        for(String sub : array1)
        {
          if(word.contains(sub) && !list.contains(sub))
            list.add(sub);
        }
      }    
      Collections.sort(list);
      return list.toArray(new String[list.size()]);
	}
}
