<h1>Divide & Conquer(DC)<br></h1>
May 16 2020<br><br>
         DC is about splitting big problem into small problems and solving them recursively.
The small problems must also be like big problem. 
Say for example, DC can be applied to a sort funtion where the input set is split into multiple small chunks of sort elements and can be resolved recursively.<br><br>
DC is not about splitting a big module whose functions are different, say for eg diving a monolith into small chunks.
<br>
<h3>Binary Search</h3><br>
l = low will be the first element<br>
h = high will be the last element<br>
Middle value = Math.floor((l+h)/2)


```
private int binarySearch(int[] nums,int low,int high,int target){        
        int mid = (low+high)/2;
        if(high<low){
            return -1;
        }else if(nums[mid]==target){
            return mid;
        }else if(nums[mid]<target){
            return binarySearch(nums,mid+1,high,target);
        }else{
            return binarySearch(nums,low,mid-1,target);
        }
    }
```
<br>

The time complexity is O(log n)
<br>
Binary search can be solved using a while loop by altering the value of l,h<br>
The time complexity for it is also O(log n)<br>
