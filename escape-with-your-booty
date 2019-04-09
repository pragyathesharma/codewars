import java.util.*;
public class Course 
{
  
    public static boolean checkCourse(char[][] map) 
    {
        int pirateRow = map.length-1;
        int pirateCol = 0;
        HashMap<Integer, ArrayList<Integer>> hMap = new HashMap<Integer, ArrayList<Integer>>();
        for (int i = 0; i < map[0].length; i++)
        {
          for (int j = 0; j < map.length; j++)
          {
            if (map[j][i] == 'N')
            {
              int key = i;
              if (!hMap.containsKey(key))
                hMap.put(key, new ArrayList<Integer>());
              int direction = 0;
              if (j == map.length-1)
                direction = 1;
              hMap.get(key).add(j);
              hMap.get(key).add(direction);
            }
            else if(map[j][i]=='X')
            {
                  pirateRow=j;
                  pirateCol=i;
            }
            
          }
        }
        
        do 
        {
          map[pirateRow][pirateCol] = '0';
          pirateCol++;
          map[pirateRow][pirateCol] = 'X';
          
          Iterator<Integer> it = hMap.keySet().iterator();
          while (it.hasNext())
          {
            int column = it.next();
            int row = hMap.get(column).get(0);
            map[row][column] = '0';
            int direction = hMap.get(column).get(1);
            if (direction == 0)
            {
              row++;
              if (row == map.length-1)
                direction = 1;  
            } 
            else 
            {
              row--;
              if (row == 0)
                direction = 0;
            }
            map[row][column] = 'N';
            ArrayList<Integer> nums = new ArrayList<Integer>();
            nums.add(row);
            nums.add(direction);
            hMap.put(column,nums);
          }
          
  
          for (int i = pirateCol-1; i <= pirateCol+1; i++)
          {
            for (int j = pirateRow-1; j <= pirateRow+1; j++)
            {
              if (j >= 0 && j < map.length && i >= 0 && i < map[0].length && map[j][i] == 'N')
                return false;
            }
          }
        } while (pirateCol < map[0].length-1);
        return true;
    }
}
