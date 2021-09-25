### **Turing Test Quiz: Count Elements using PHP**
Given an integer array arr, count how many elements x there are, such that x+1 is also in arr. if there're duplicates in arr, count them separately.

**Example 1:**

```php  
Input: arr = [1,2,3]
```

**Output: 2**

**Explanation:**

There are 2 such elements: 1 and 2 because 2 and 3 are also in the array.

**Example 2:**

```php 
Input:arr = [1,1,3,3,5,5,7,7]
```

**Output: 0**
 
**Explanation:**

There's no such number because 2,4,6,8 is not present in the array.

```php
class Solution{
	function countElement($arr){
		$arr_size = count($arr);
		$count = 0;
		for ($i=0; $i < $arr_size; $i++) { 
			$chk_exist = $arr[$i] + 1;
			if(in_array($chk_exist, $arr)){
				$count +=1;
			}
		}
		return $count;
	}
}
$array = ['1','1','3','3','5','5','7','7'];
$solution = new Solution();
$output = $solution->countElement($array);
echo $output;
```

</pre>