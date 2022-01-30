# Intersection-of-two-arrays
leetcode problem easy
class Solution {
    public int[] intersection(int[] nums1, int[] nums2) {
       
        Set<Integer> set1=new HashSet();
        
        Set<Integer> intersection=new HashSet();
        
        for(int num:nums1)
        {
            set1.add(num); //added all elements of nums1
        }
        for(int num:nums2)
        {
            if(set1.contains(num))
            {
                intersection.add(num); //added intersected array 
            }
        }
        int i=0;
        int[] result=new int[intersection.size()];
        for(int num:intersection)
        {
            result[i++]=num; ///i is incremented just after leaving box []
        }
        
        return result;
        
    }
        
        
    
}
