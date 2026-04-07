# Key Learnings + What To Think (Two Sum)

## Core Insight

**Store what you’ve seen, check what you need**

---

## What Should Run in Your Mind (Step-by-Step Thinking)

When you see this problem, your brain should go:

1. **“I need two numbers → pair problem”**
2. **“Brute force is O(n²), can I do better?”**
3. **“Yes, I can store previous values”**
4. **“For current number, what do I need?”**

   ```
   complement = target - num
   ```
5. **“Have I already seen this complement?”**

   * YES → return answer
   * NO → store current number

---

## Mental Algorithm (Memorize This Flow)

```
Create hashmap

For each index i:
    complement = target - nums[i]

    If complement exists in hashmap:
        return indices

    Else:
        store nums[i] with index
```

---

## Key Points

* Convert problem → **complement search**
* Use **HashMap for fast lookup**
* Always **check before insert**
* Store **value → index**
---

## Pattern Recognition

If you see:

* “Find two numbers”
* “Target sum”
* “Return indices”

Think immediately:
**HashMap + Complement**

---

## Common Mistakes

* Using brute force (O(n²))
* Wrong order (insert before check)
* Forgetting indices

---

## Interview Tip

Train your instinct:

> Whenever you need **pair + fast lookup → HashMap**

---

## One-Line Memory Trick

**Check if the required number already appeared before**
