## 1️⃣ Definition

A **Flame Graph** is a **visual tool** used to analyze **program performance**.

- Shows **how much time is spent in each function** during execution
    
- Typically used for **CPU profiling**, but can also show **memory usage** or other metrics
    
- Each **rectangle** represents a function call
    
- **Width** = **time spent** in that function (including children)
    
- **Y-axis** = **stack depth** (call hierarchy)
    

Flame graphs are popular because they make it easy to **see hotspots in code** at a glance.

---

## 2️⃣ Why Use Flame Graphs

- Detect **performance bottlenecks**
    
- Identify **functions that consume most CPU**
    
- Optimize **high-cost call paths**
    
- Visualize **stack traces over time**
    

---

## 3️⃣ How Flame Graphs Work

1. Run a **profiler** to collect **stack traces** over time (e.g., `perf`, `async-profiler`, `Xcode Instruments`)
    
2. Aggregate **stack traces** into **samples**
    
3. Draw **rectangles for each function**:
    
    - Width ∝ **total time spent in that function**
        
    - Stacked vertically to show **caller → callee relationships**
        
4. Interactive flame graphs often allow **clicking a rectangle** to zoom or see details

4️⃣ Anatomy of a Flame Graph
![[{E7F548D9-7A04-49AD-9969-28B89E89A11C}.png]]


- **Top of stack (Y-axis)** → currently executing function
    
- **Bottom of stack** → entry point (e.g., `main()`)
    
- **Width** → total time spent in function + children
    

---

## 5️⃣ Example Workflow (Linux)

1. Install **perf** for profiling:
    

sudo apt install linux-tools-common linux-tools-generic

2. Run program with profiling:
    

perf record -F 99 -g ./my_program

- `-F 99` → sample 99 times per second
    
- `-g` → capture call graph
    

3. Generate **flame graph** (using Brendan Gregg’s scripts):
    

perf script | ./stackcollapse-perf.pl > out.folded  
./flamegraph.pl out.folded > flamegraph.svg

- Open `flamegraph.svg` in browser → interactive flame graph
    

---

## 6️⃣ Tools / Libraries

|Platform / Language|Tool / Library|
|---|---|
|Linux / C / C++|`perf`, `FlameGraph` scripts|
|Java|`async-profiler`, `YourKit`, `JFR`|
|JavaScript / Node|`0x`, `clinic flame`|
|Python|`py-spy`, `FlameGraph`|
|macOS|`Instruments`, `dtrace`, `perf`|

---

## 7️⃣ Advantages

- **Visualizes hotspots** clearly
    
- **Shows call hierarchy**
    
- **Easy to interpret** compared to raw stack traces
    
- Works with **CPU, memory, or I/O profiling**
    

---

## 8️⃣ Limitations

- **Requires sampling/profiling** → small overhead
    
- Only shows **aggregated time**, not every single call
    
- **Large codebases** may create cluttered graphs
    
- Interactive visualization often needed for **large flame graphs**
    

---

## 9️⃣ Key Exam / Interview Points

- Flame graph = **visual CPU/memory profiling tool**
    
- **Width of rectangle** = total time spent in that function (incl. children)
    
- **Height** = call stack depth
    
- **Top** = currently executing function
    
- Helps identify **performance bottlenecks** quickly
    
- Tools: `perf` (Linux), `async-profiler` (Java), `0x` (Node.js), `py-spy` (Python)