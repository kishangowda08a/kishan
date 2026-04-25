
Problem Statement
Consider a BJT Common Emitter amplifier using an NPN transistor with:
RC=4kΩR_C = 4k\OmegaRC=4kΩ
RB=200kΩR_B = 200k\OmegaRB=200kΩ
VCC=10VV_{CC} = 10VVCC=10V
β=100\beta = 100β=100
Input signal vinv_{in}vinis small
👉 Find:
Small-signal model
Voltage gain AvA_vAv

🔌 Original Circuit



6

⚙️ Step 1: DC Operating Point (Q-point)
We first find base current:
IB=VCC−VBERB=10−0.7200k=46.5&nbsp;μAI_B = \frac{V_{CC} - V_{BE}}{R_B}= \frac{10 - 0.7}{200k}= 46.5\ \mu AIB=RBVCC−VBE=200k10−0.7=46.5&nbsp;μA
Collector current:
IC=βIB=100×46.5μA=4.65&nbsp;mAI_C = \beta I_B = 100 \times 46.5\mu A = 4.65\ mAIC=βIB=100×46.5μA=4.65&nbsp;mA

🔄 Step 2: Small Signal Model
Replace transistor with hybrid-π model:
rπ=βgmr_\pi = \frac{\beta}{g_m}rπ=gmβ
gm=ICVTg_m = \frac{I_C}{V_T}gm=VTIC, where VT≈25mVV_T ≈ 25mVVT≈25mV
gm=4.65mA25mV=0.186&nbsp;Sg_m = \frac{4.65mA}{25mV} = 0.186\ Sgm=25mV4.65mA=0.186&nbsp;Srπ=1000.186≈537&nbsp;Ωr_\pi = \frc{100}{0.186} ≈ 537\ \Omegarπ=0.186100≈537&nbsp;Ω

🔍 Small Signal Equivalent Circuit



6

📉 Step 3: Voltage Gain Derivation
Output voltage:
vo=−icRCv_o = -i_c R_Cvo=−icRC
But:
ic=gmvπi_c = g_m v_\piic=gmvπ
So:
vo=−gmvπRCv_o = -g_m v_\pi R_Cvo=−gmvπRC
Since vπ≈vinv_\pi ≈ v_{in}vπ≈vin:
Av=vovin=−gmRCA_v = \frac{v_o}{v_{in}} = -g_m R_CAv=vinvo=−gmRC

🧮 Final Answer
Av=−0.186×4000=−744A_v = -0.186 \times 4000 = -744Av=−0.186×4000=−744

✅ Final Results
Transconductance: gm=0.186&nbsp;Sg_m = 0.186\ Sgm=0.186&nbsp;S
Input resistance: rπ≈537&nbsp;Ωr_\pi ≈ 537\ \Omegarπ≈537&nbsp;Ω
Voltage Gain:
Av=−744\boxed{A_v = -744}Av=−744

💡 Key Concepts (Important for Exams)
CE amplifier gives high gain + phase inversion
Negative sign → 180° phase shift
Gain depends mainly on:
gmg_mgm(depends on bias current)
RCR_CRC
https://notebook.zoho.in/app/index.&nbsp
;LGP&nbsp;html#/shared/22bt463a6e6412a8746aeb417dd81a2fe4df8
​


Two Sum (Classic DSA Problem)
📘 Problem Statement
Given an array of integers and a t DROP 1 arget value, return indices of the two numbers such that they add up to the target.

🧾 Example
Input: nums = [2, 7, 11, 15], target = 9
Output: [0, 1]
👉 Because 2 + 7 = 9

🖼️ Visual Understanding



7

🧠 Approach 1: Brute Force (Simple)
💡 Idea
Check every pair and see if they sum to target.
⏱️ Complexity
Time: O(n2)O(n^2)O(n2)
Space: O(1)O(1)O(1)
💻 Code (Python)

def twoSum(nums, target):
    n = len(nums)
    for i in range(n):
        for j in range(i + 1, n):
            if nums[i] + nums[j] == target:
                return [i, j]


⚡ Approach 2: Hash Map (Optimal)
💡 Idea
Instead of checking all pairs:
Store numbers in a dictionary (hash map)
For each number, check if target - current exists

🖼️ Hash Map Working



5

⏱️ Complexity
Time: O(n)O(n)O(n)
Space: O(n)O(n)O(n)

💻 Code (Python)

def twoSum(nums, target):
    seen = {}  # value -> index
    
    for i, num in enumerate(nums):
        complement = target - num
        
        if complement in seen:
            return [seen[complement], i]
        
        seen[num] = i


🔍 Step-by-Step Example
For nums = [2, 7, 11, 15], target = 9:
Step
Num
Complement
Hash Map
Result
1
2
7
{2:0}
❌
2
7
2
{2:0}
✅
👉 Found at indices [0, 1]

🎯 Key Takeaways
Use hashing to reduce time complexity
Always think:
👉 “Can I trade space for time?”
This is one of the most asked interview questions

🚀 Want more practice?
I can give you:
Variations (Two Sum II, Three Sum)
Java / C++ code
Interview tricks + edge cases
<iframe src="

Notebook
https://notebook.zohopublic.in/embed/notes/22bt4e450d391f1884a58941ba20ed9ac2b82
" scrolling="no" frameborder="0" allowfullscreen=true width="800" height="520" title="Embed code" ></iframe>

 
https://notebook.zohopublic.in/public/notes/22bt463a6e6412a8746aeb417dd81a2fe4df8


 <pre> ```cpp #include &lt;iostream&gt; using namespace std; int main() { cout &lt;&lt; "Hello World"; } ``` </pre>

