
# 📘 BJT Common Emitter Amplifier

## 🔧 Problem Statement
Consider a BJT Common Emitter amplifier using an NPN transistor:

- \( R_C = 4k\Omega \)  
- \( R_B = 200k\Omega \)  
- \( V_{CC} = 10V \)  
- \( \beta = 100 \)  
- Input signal \( v_{in} \) is small  

👉 **Find:**
- Small-signal model  
- Voltage gain \( A_v \)

---

### Base Current

IB = (VCC - VBE) / RB  
IB = (10 - 0.7) / 200k  
IB = 46.5 µA  

### Collector Current

IC = β × IB  
IC = 100 × 46.5 µA  
IC = 4.65 mA

## ⚙️ Step 1: DC Operating Point (Q-point)

### Base Current
\[
I_B = \frac{V_{CC} - V_{BE}}{R_B} = \frac{10 - 0.7}{200k} = 46.5\ \mu A
\]

### Collector Current
\[
I_C = \beta I_B = 100 \times 46.5\mu A = 4.65\ mA
\]

---

## 🔄 Step 2: Small Signal Model

### Transconductance
\[
g_m = \frac{I_C}{V_T}, \quad V_T \approx 25mV
\]

\[
g_m = \frac{4.65mA}{25mV} = 0.186\ S
\]

### Input Resistance
\[
r_\pi = \frac{\beta}{g_m} = \frac{100}{0.186} \approx 537\ \Omega
\]

---

## 🔍 Small Signal Equivalent Circuit

![Small Signal Model](images/gitbook-ui.png)

---

## 📉 Step 3: Voltage Gain Derivation

\[
v_o = -i_c R_C
\]

\[
i_c = g_m v_\pi
\]

\[
v_o = -g_m v_\pi R_C
\]

Since \( v_\pi \approx v_{in} \):

\[
A_v = \frac{v_o}{v_{in}} = -g_m R_C
\]

---

## 🧮 Final Answer

\[
A_v = -0.186 \times 4000 = -744
\]

---

## ✅ Final Results

- Transconductance: \( g_m = 0.186\ S \)  
- Input resistance: \( r_\pi \approx 537\ \Omega \)  
- Voltage Gain:  
\[
\boxed{A_v = -744}
\]

---

## 💡 Key Concepts

- CE amplifier gives **high gain + phase inversion**
- Negative sign → **180° phase shift**
- Gain depends on:
  - \( g_m \) (bias current dependent)
  - \( R_C \)

---

# 💻 Two Sum (Classic DSA Problem)

## 📘 Problem Statement
Given an array of integers and a target value, return indices of the two numbers such that they add up to the target.

---

## 🧾 Example


![UI](images/gitbook-ui.png)


👉 Because \( 2 + 7 = 9 \)

---

## 🧠 Approach 1: Brute Force

### 💡 Idea
Check every pair.

### ⏱️ Complexity
- Time: \( O(n^2) \)  
- Space: \( O(1) \)

### 💻 Code (Python)

```python
def twoSum(nums, target):
    n = len(nums)
    for i in range(n):
        for j in range(i + 1, n):
            if nums[i] + nums[j] == target:
                return [i, j]


 <pre> ```cpp #include &lt;iostream&gt; using namespace std; int main() { cout &lt;&lt; "Hello World"; } ``` </pre>
def twoSum(nums, target):
    seen = {}  # value -> index
    
    for i, num in enumerate(nums):
        complement = target - num
        
        if complement in seen:
            return [seen[complement], i]
        
        seen[num] = i
