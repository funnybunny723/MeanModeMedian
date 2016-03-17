# MeanModeMedian
//Finds the mean, mode and median in an array of Integers

public static void main(String[] args){
  int[] array = {};
  System.out.println("The array is: ");
  for(int e: array){
    System.out.print(e);
  }
  System.out.println("The mean is " + getMean(array));
}

public double getMean(int[] array){
  double mean = 0;
  for(int i = 0; i < array.length; i++){
    mean += array[i];
  }
  return mean/array.length;
}

public int getMedian(int[] array){
  int[] ordered = new int[array.length];
  for(int i = 1; i < array.length; i++){
		int temp = array[i];
		for(int j = i-1 ;j >=0 && temp.compareTo(array[j]) <0; j--){
			array[j+1] = array[j];
		}array[j+1] = temp;
	}ordered = array;
	return array[array.length/2];
}
