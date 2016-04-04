# MeanModeMedian
//Finds the mean, mode and median in an array of Integers
public class MeanModeMedian{

	public static void main(String[] args){
	  int[] array = {};
	  System.out.println("The array is: ");
	  for(int e: array){
	    System.out.print(e);
	  }
	  System.out.println("The mean is " + getMean(array));
	}
	
	public int[] orderArray(int[] array){
       	 int[] ordered = new int[array.length];
	  for(int i = 1; i < array.length; i++){
		int temp = array[i];
		for(int j = i-1 ;j >=0 && temp < array[j]; j--){
			array[j+1] = array[j];
		}array[j+1] = temp;
	}ordered = array;
	return ordered;
	}
	
	public double getMean(int[] array){
	  double mean = 0;
	  for(int i = 0; i < array.length; i++){
	    mean += array[i];
	  }
	  return mean/array.length;
	}
	
	public int getMedian(int[] array){
	int ordered = orderArray(array);
	  return ordered[array.length/2];
	}
	
	public int getMode(int[] array){
	  int popCount1 = 0;
	  int popCount2 = 0;
	  int popular1;
	  int popular2;
	  //first sort the array
	  int[] ordered = orderArray(array);
	  for (int i = 0; i < n.length; i++){
            pupular1 = n[i];
            count1 = 0;    //see edit

	        for (int j = i + 1; j < n.length; j++){
	            if (popular1 == n[j]) count1++;
	        }
	        if (count1 > count2){
	                popular2 = popular1;
	                count2 = count1;
	        } else if(count1 == count2){
	            popular2 = Math.min(popular2, popular1);
	        }
	    }
	  return popular2;
	  } 
	  
}
