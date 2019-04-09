import java.util.*;

class Bouncy {
    
    static List<Integer> longestBouncyList(List<Integer> arr) {
    
        if(arr.size() == 0)
          return arr;
        ArrayList<List<Integer>> list = new ArrayList<>();
        ArrayList<Integer> temp=null;
        
        for(int i = 0; i < arr.size()-1; i++)
        {
          temp= new ArrayList<>();
          boolean up = true;
         
          if(arr.get(i) > arr.get(i+1))
            up = false;
          int j = i;
          while(j < arr.size()-1)
          {
           boolean added = false;
            if(up && arr.get(j) < arr.get(j+1))
              {
                temp.add(arr.get(j));
                up = false;
              }
            
            else if(!up && arr.get(j) > arr.get(j+1))
              {
                temp.add(arr.get(j));
                up = true;
              }
            
            else
            {
              //add i+1
              temp.add(arr.get(j));
              //temp.add(arr.get(j+1));
              list.add(temp);
              added = true;
              j=arr.size();
            }
            j++;
            if(j == arr.size()-1 && !added)
            {
              temp.add(arr.get(j));
              list.add(temp);
              added = true;
            }
          }
         
        }
        //System.out.println(list);
        int maxIndex = 0;
        for(int i = 0 ; i < list.size(); i++)
        {
          if(list.get(i).size() > list.get(maxIndex).size())
            maxIndex = i;
        }
        return list.get(maxIndex);
    }
}
