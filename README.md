# Divide-Conquer
/************************************************************************************************************
 *
 *  Pace University
 *  Fall 2016
 *  Algorithms and Theory of Computing
 *
 *  Course: CS 608 CRN 73103
 *  Author: Rakesh Parappa
 *  Collaborators: NONE
 *  References: None
 *
 *  Assignment: Assignment #1
 *  Problem: Maximum Subarray Problem using Divide and Conquer
 *  Description: The Maximum Subarray Problem is the task of finding the contiguous
 *	subarray, within an array of numbers, that has the largest sum. Divide & Conquer method finds 
 *	the largest sum of the contiguous subarray in O(nlogn) running time.
 *
 *  Input: Random variables selected from -10 to 10
 *  Output: The largest sum of the contiguous subarray of an array.
 *
 *  Visible data fields:
 *  int i, n, maxsum, low, high;
 *	int[] A = new int[n];
 *
 *
 *  Visible methods:
 *  public static void main(String[] args)
 *  public static int maxsubarray(int[] A, int low, int high)
 *  public static int maxcrossarray(int[] A, int low, int mid, int high)
 *  private static int comp(int a, int b, int c)
 *
 *   Remarks
 *   -------
 * 2. Running time is measured in Milliseconds
 *  _______________________________________________________________________ 
 *  |						|  n= 100  | n=500  | n=10^3 | n=5000 | n=10^4 |
 *  |_______________________|__________|________|________|________|________|	 
 *	|Brute Force			|  9.0     | 138    | 796	 |89521	  |	797299 |	
 *	|_______________________|__________|________|________|________|________|
 *	_________________________________________________________________________________ 
 *  |						|  n= 100  | n=500  | n=10^3 | n=5000 | n=10^4 | n=5*10^4|
 *  |_______________________|__________|________|________|________|________|_________|	 
 *	|Brute Force Improved	|  2.0     | 16.0   | 18.0	 | 91.0	  |	280.0  | 4651	 |
 *	|_______________________|__________|________|________|________|________|_________|
 *  ___________________________________________________________________________________________________
 *  |						|   n= 100 | n=500  | n=10^3 | n=5000 | n=10^4 | n=5*10^4| n=10^5 | n=10^6 |
 *  |_______________________|__________|________|________|________|________|_________|________|________|	 
 *	|Divide & Conquer		|  0.0     |  1.0	|  2.0	 |	4.0   |	5.0    | 16.0    | 31.0   | 138.0  |
 *	|_______________________|__________|________|________|________|________|_________|________|________|
 *  ___________________________________________________________________________________________________
 *  |						|   n= 100 | n=500  | n=10^3 | n=5000 | n=10^4 | n=5*10^4| n=10^5 | n=10^6 |
 *  |_______________________|__________|________|________|________|________|_________|________|________|	 
 *	|Dynamic Program		|  0.0     |  0.0	|  0.0	 |	1.0   |	1.0    | 3.0     | 11.0   | 16.0   |
 *	|_______________________|__________|________|________|________|________|_________|________|________|
 *
 *
 *  3.* As per the above measured running time if we draw a graph with input size on x-axis and time on y-axis, the growth rate of Brute
 *    	Force version is highest and Divide & Conquer method is the fastest for all values of n among the three algorithms. 
 *    *	But when you compare the results with Kadane's dynamic programming algorithm, it is evident that it is not only faster but also
 *    	linear at n=100 to n=1000 and also at n=5000 to 10^4, which indicates that its growth rate is even slower than Divide and Conquer.
 *    * As per the asymptotic growth rate order (C < logn < n < nlogn < n^2 < n^3 < e^n) polynomial has higher growth rate when compared to
 *      Linearithmic  or linear functions.
 *    * Hence we come to the conclusion that the Divide & Conquer method is the efficient method among the first three but and but Dynamic 
 *    	program of Kadane's is the best of all the four algorithms and the Big-O of each version satisfies with the growth rate such that 
 *      O(n) < O(nlogn) < O(n^2) < O(n^3).
 *******************************************************************************************************************************************/
