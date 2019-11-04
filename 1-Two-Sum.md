// Given a list of numbers and a number k, return whether any two numbers from the list add up to k.

// For example, given [10, 15, 3, 7] and k of 17, return true since 10 + 7 is 17.

// Bonus: Can you do this in one pass?

```
func twoSum(_ nums:[Int], _ k: Int ) -> Bool {
	let map = [Int: Int]()
	for i in 0..<nums.count {
		let diff = k - nums[i]
		//17 - 10 = 7
		if let complement = map[nums[i]] {
			//return [nums[complement], nums[i]]	
			return true
		}
		map[diff] = i
	}
	return false
}
```
