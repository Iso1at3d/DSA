# File: learning.md

## Problem Overview

Tumhe ek array of strings diya gaya hai. Tumhe sabhi strings ka longest common prefix find karna hai.

Agar koi common prefix nahi hai, to empty string return karo.

## Core Idea

Is problem ko dekhte hi yeh sochna chahiye:

"Sabhi strings me starting se compare karna hai jab tak mismatch na mile"

## Key Observations

* Prefix hamesha string ke start se hota hai
* Jaise hi kisi bhi string me mismatch mile, wahi stop karna hai
* Shortest string se zyada prefix ho hi nahi sakta

## Approach (Step-by-step soch)

1. Pehli string ko reference maan lo
2. Uske har character ko check karo
3. Har index ke liye:

   * Sabhi strings me same character hai ya nahi check karo
4. Agar mismatch mile ya string khatam ho jaye → break
5. Jo valid part hai wahi answer hai

## Example (Important for memory)

Input:
strs = ["flower","flow","flight"]

Step-by-step:

f → sab me common
l → sab me common
o → third string me 'i' hai → mismatch

Final Answer: "fl"

## Easy Memory Trick

"Har string ko ek line me likh ke vertical compare karo"

Jaise:

flower
flow
flight

Column-wise check karo jab tak match ho

## Pattern Recognition

* String comparison
* Prefix problems
* Character-by-character traversal

## Pattern Used

Horizontal Scanning (Prefix Shrinking)

## Why This Works

* Hum first string ko initial prefix maan lete hain
* Phir har next string ke saath check karte hain ki kya wo prefix match kar raha hai
* Agar match nahi karta, to prefix ko chhota kar dete hain
* Yeh process tab tak chalta hai jab tak valid common prefix mil na jaye

Isliye yeh efficient hai kyunki unnecessary comparisons avoid ho jaate hain

## When To Use This Pattern Again

* Jab multiple strings ka common starting part find karna ho
* Jab prefix gradually shrink kar sakte ho based on condition
* Jab direct comparison easy ho (no complex structure needed)
* Interview me jab "common prefix", "shared start", ya "matching beginning" type ka question aaye

## Common Mistakes

* Sirf first 2 strings compare karke answer assume kar lena
* Shortest string ka dhyan na rakhna
* Early break na karna (time waste)

## Complexity Analysis

* Time Complexity: O(n * m)
* Space Complexity: O(1)

## Interview Tip

* Start me bolo: "We will compare characters column-wise across all strings"
* Edge case bolo: empty string present ho sakta hai
* Batana ki shortest string se zyada prefix possible nahi
* Clean loop structure use karo
* End me ek quick dry run kar do

Simple rule:
"Compare from start, stop at first mismatch"

