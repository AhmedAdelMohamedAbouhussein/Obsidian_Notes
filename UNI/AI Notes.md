# Artificial Intelligence Notes

## **Chapter 1: Introduction to AI**

### **Definition**
> **AI = Science + Engineering** of creating intelligent machines.

---

### **Four Approaches to AI**
| Approach | Description |
|-----------|--------------|
| **Thinking Humanly (TH)** | Making machines think like humans by replicating cognitive processes. |
| **Acting Humanly (AH)** | Designing AI that behaves like a human. |
| **Thinking Rationally (TR)** | Using logic and reasoning to make the best decisions. |
| **Acting Rationally (AR)** | Focusing on actions that achieve the best outcomes. |

---

### **Turing Test**
- **Purpose:** Evaluate if a machine can exhibit human-like conversation.  
- **Note:** Passing the test **does not mean true intelligence** — a machine could simply mimic human language patterns.

---

### **Disciplines that AI is Built Upon**
| Discipline | Contribution |
|-------------|---------------|
| **Philosophy** | Explores ideas about reasoning, knowledge, and the mind. |
| **Mathematics** | Provides logic, probability, and computational concepts. |
| **Economics** | Focuses on decision theory and utility maximization for optimal choices. |
| **Neuroscience** | Studies how the brain works, inspiring neural networks. |
| **Psychology** | Examines human thinking and behavior. |
| **Computer Engineering** | Builds fast and efficient hardware to run AI algorithms. |
| **Control Theory / Cybernetics** | Deals with systems that achieve goals through feedback and control. |

> 💡 *Tip: Review key events in AI history (optional).*

---

### **The Standard Model of AI**
- A **paradigm** where machines are designed to pursue fully specified, fixed objectives given by humans.  
- **Issue:** It assumes humans can define complete and correct objectives — which is often impossible.

---

### **Types of AI**
| Type                 | Description                                   |
| -------------------- | --------------------------------------------- |
| **Narrow AI**        | Designed for a single, specific task.         |
| **General AI (AGI)** | Can learn and reason across multiple domains. |
|                      |                                               |

---

### **Benefits of AI**
- Increased efficiency  
- Job automation  
- Personalized services  
- Scientific discovery

### **Risks of AI**
- Job displacement  
- Bias and discrimination  
- Privacy concerns  
- Spread of misinformation

---

### **Levels of AI**
| Level                                     | Description                                                 |
| ----------------------------------------- | ----------------------------------------------------------- |
| **Human-Level AI**                        | Machines that can learn and perform any task a human can.   |
| **Artificial General Intelligence (AGI)** | Possesses general cognitive abilities comparable to humans. |
| **Artificial Superintelligence (ASI)**    | Surpasses human intelligence in all domains.                |
|                                           |                                                             |

---

## **Chapter 2: Intelligent Agents**

### **Definition**
An **agent** is anything that:
- **Perceives** its environment through **sensors**
- **Acts** upon it through **actuators**

---

### **Key Concepts**
| Term                 | Definition                                            |
| -------------------- | ----------------------------------------------------- |
| **Percept**          | The agent’s perceptual input at a given instant.      |
| **Percept Sequence** | The complete history of what the agent has perceived. |
| **Agent**            | = **Architecture + Program**                          |
| **Agent Function**   | Maps percept histories to actions.                    |
|                      |                                                       |

---

### **Rational & Autonomous Agents**
- **Rational Agent:** Selects the action expected to maximize performance.  
- **Autonomous Agent:** Learns from experience and adapts behavior accordingly.

---

### **Performance Measure**
> Objective criteria that evaluate the success of an agent’s behavior.

---

### **PEAS Framework**
| Component | Meaning |
|------------|----------|
| **P** | Performance Measure |
| **E** | Environment |
| **A** | Actuators |
| **S** | Sensors |

---

### **Environment Types**
### **1. Accessible vs. Inaccessible**

- **Accessible:**  
    The agent can obtain **complete and accurate information** about the environment’s state.  
    **Example:** A chess game — all pieces and positions are visible.
    
- **Inaccessible:**  
    The agent has **limited or partial information** about the environment.  
    **Example:** A self-driving car — it can’t know exactly what other drivers will do.
    

> 💡 _Accessible = full info; Inaccessible = partial info._

---

### **2. Deterministic vs. Nondeterministic**

- **Deterministic:**  
    The **next state** of the environment is **completely determined** by the current state and the agent’s action.  
    **Example:** Chess — given a move, the board’s next state is predictable.
    
- **Nondeterministic (Stochastic):**  
    The **next state** is **uncertain** or affected by **randomness**.  
    **Example:** Taxi driving — traffic or pedestrian behavior introduces uncertainty.
    

> 💡 _Deterministic = predictable outcomes; Nondeterministic = unpredictable._

---

### **3. Episodic vs. Nonepisodic (Sequential)**

- **Episodic:**  
    Each task or episode is **independent** — the agent’s next action does **not depend on previous ones**.  
    **Example:** Image classification — each image is processed separately.
    
- **Nonepisodic (Sequential):**  
    Current decisions **affect future states or rewards**.  
    **Example:** Playing chess — every move impacts later outcomes.
    

> 💡 _Episodic = one-shot decisions; Sequential = decisions build on each other._

---

### **4. Hostile vs. Friendly**

- **Hostile:**  
    The environment **acts against the agent** or has **competing agents**.  
    **Example:** Multiplayer games — opponents try to defeat you.
    
- **Friendly:**  
    The environment or other agents **cooperate** or do not interfere.  
    **Example:** Cooperative robots working together on an assembly line.
    

> 💡 _Hostile = adversarial; Friendly = cooperative._

---

### **5. Static vs. Dynamic**

- **Static:**  
    The environment **does not change** while the agent is deciding.  
    **Example:** Chess — the board stays still while you plan your move.
    
- **Dynamic:**  
    The environment **can change** while the agent is thinking or acting.  
    **Example:** Driving a car — traffic and conditions change constantly.
    

> 💡 _Static = frozen world; Dynamic = constantly changing._

---

### **6. Discrete vs. Continuous**

- **Discrete:**  
    There are a **finite number of possible states, percepts, and actions.**  
    **Example:** Chess — limited, well-defined moves and board positions.
    
- **Continuous:**  
    There are **infinitely many possible states or actions**, changing smoothly over time.  
    **Example:** Taxi driving — steering angles, speed, and position vary continuously.
    

> 💡 _Discrete = countable steps; Continuous = infinite, smooth changes._

---

### ✅ **Summary Table**

|Characteristic|Type 1|Type 2|Example|
|---|---|---|---|
|**Accessibility**|Accessible|Inaccessible|Chess vs. Self-driving car|
|**Determinism**|Deterministic|Nondeterministic|Chess vs. Traffic|
|**Episodes**|Episodic|Nonepisodic|Image recognition vs. Chess|
|**Friendliness**|Friendly|Hostile|Cooperative robots vs. Battle games|
|**Dynamics**|Static|Dynamic|Chess vs. Driving|
|**Continuity**|Discrete|Continuous|Chess vs. Taxi driving|

---

### **Agent Types**
| Type              | Description                                             | Example                             |
| ----------------- | ------------------------------------------------------- | ----------------------------------- |
| **Simple Reflex** | Acts only on current percept; “if–then” rules.          | Simple vacuum cleaner               |
| **Model-Based**   | Uses internal model to track world state.               | Vacuum that remembers cleaned areas |
| **Goal-Based**    | Chooses actions to achieve specific goals via planning. | GPS finding the fastest route       |
| **Utility-Based** | Maximizes overall happiness or performance.             | AI choosing optimal trade-offs      |

---

### **Learning Agent**
> Improves its performance over time by learning from experience.

### **AI Ethics**
Designing responsible agents that act ethically and transparently.

---

## **Search Algorithms (Overview)**

### **Uninformed Search**
> Uses only information from the **problem definition**.

**Examples:**  
- BFS (Breadth-First Search)  
- DFS (Depth-First Search)  
- UCS (Uniform Cost Search)  
- DLS (Depth-Limited Search)  
- Iterative Deepening Search  

---

### **Informed Search**
> Uses **domain-specific knowledge** or heuristics to guide the search more efficiently.

**Examples:**  
- Greedy Search  
- A* Search  
- Beam Search  
- Recursive Best-First Search (RBFS)

---

### **Key Concepts**
- **Strategy:** Defined by the order in which nodes are expanded.  
- **Admissible Heuristic:** Never overestimates the cost to reach the goal.

---

### **Local Search Algorithms**
> Operate by moving from a start state to neighboring states **without tracking full paths**.

**Examples:**  
- **Hill Climbing**  
- **Simulated Annealing**  
- **Local Beam Search**

---

### **Game Search**
| Concept | Description |
|----------|--------------|
| **Minimax** | Strategy for two-player games assuming both play optimally. |
| **Alpha–Beta Pruning** | Optimization of minimax that ignores irrelevant branches. |

---

