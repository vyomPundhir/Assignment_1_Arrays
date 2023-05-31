Q1.
```javascript
function Sum(nums, target) {
  const mapnum = new Map();

  for (let i = 0; i < nums.length; i++) {
    const comp = target - nums[i];
    if (mapnum.has(comp)) {
      return [numMap.get(comp), i];
    }
    mapnum.set(nums[i], i);
  }

  return [];
}
const nums = [2, 7, 11, 15];
const target = 9;

const index = Sum(nums, target);
console.log(`Output: [${index[0]}, ${index[1]}]`);
```
Q2.
```javascript
function removeElement(nums, val) {
  let k = 0; // Number of elements not equal to val

  for (let i = 0; i < nums.length; i++) {
    if (nums[i] !== val) {
      nums[k] = nums[i];
      k++;
    }
  }

  return k;
}

const nums = [3, 2, 2, 3];
const val = 3;

const remain = removeElement(nums, val);
console.log(`Output: ${remain}, nums = [${nums.slice(0, remain).join(', ')}, _, _]`);
```
Q3.
```javascript
function search(nums, target) {
  let left = 0;
  let right = nums.length - 1;

  while (left <= right) {
    const mid = Math.floor((left + right) / 2);

    if (nums[mid] === target) {
      return mid;
    } else if (nums[mid] < target) {
      left = mid + 1;
    } else {
      right = mid - 1;
    }
  }
  return left;
}

const nums = [1, 3, 5, 6];
const target = 5;

const index = search(nums, target);
console.log(`Output: ${index}`);

```
Q4.
```javascript
function plusOne(digits) {
  const n = digits.length;

  for (let i = n - 1; i >= 0; i--) {
    if (digits[i] < 9) {
      digits[i]++;
      return digits;
    } else {
      digits[i] = 0;
    }
  }

  digits.unshift(1);
  return digits;
}

const digits = [1, 2, 3];
const result = plusOne(digits);
console.log("Output:", result);

```