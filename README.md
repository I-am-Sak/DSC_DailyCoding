# DSC_DailyCoding
Press fork in the upper right corner.
Write your answer and save it using your confortable language.
Or else you can also upload your solution in the folder.
1]//Solution_in_java//
public class GFG { 

    static void arrayConcatenate(int arr[], int b[],  
                                             int k) 
    { 
        // Array b will be formed by concatenation 
        // array a exactly k times 
        int j = 0; 
        while (k > 0) { 
  
            for (int i = 0; i < arr.length; i++) { 
                b[j++] = arr[i]; 
            } 
            k--; 
        } 
    } 
      static int maxSubArrSum(int a[]) 
    { 
        int size = a.length; 
        int max_so_far = Integer.MIN_VALUE, 
            max_ending_here = 0; 
  
        for (int i = 0; i < size; i++) { 
            max_ending_here = max_ending_here + a[i]; 
            if (max_so_far < max_ending_here) 
                max_so_far = max_ending_here; 
            if (max_ending_here < 0) 
                max_ending_here = 0; 
        } 
        return max_so_far; 
    } 
    static long maxSubKSum(int arr[], int k) 
    { 
        int arrSum = 0; 
        long maxSubArrSum = 0; 
  
        int b[] = new int[(2 * arr.length)]; 
  
        arrayConcatenate(arr, b, 2); 

        for (int i = 0; i < arr.length; i++) 
            arrSum += arr[i]; 
        if (arrSum < 0) 
            maxSubArrSum = maxSubArrSum(b); 

        else
            maxSubArrSum = maxSubArrSum(b) + 
         (k - 2) * arrSum; 
  
        return maxSubArrSum; 
    }  
    public static void main(String[] args) 
    { 
        int arr[] = { 1, -2, 1 }; 
        int k = 5; 
        System.out.println(maxSubKSum(arr, k)); 
    } 
}    


2]//Solution_in_java//
            
            
