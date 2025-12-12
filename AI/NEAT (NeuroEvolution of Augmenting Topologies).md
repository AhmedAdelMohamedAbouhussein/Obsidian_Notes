
**1. Introduction:**  
NEAT is an evolutionary algorithm designed to automatically evolve artificial neural networks (ANNs). Unlike traditional neural network training (e.g., backpropagation), NEAT evolves both the **weights** of connections **and the network structure** (topology) over generations. This allows networks to start simple and become more complex only when necessary. NEAT was introduced by **Kenneth O. Stanley** in 2002.

---

**2. Key Concepts of NEAT:**

**a) Evolving Topology and Weights:**

- Traditional neural networks require the designer to fix the number of layers and neurons.
    
- NEAT starts with a **minimal network** (usually input nodes connected directly to output nodes) and **gradually adds new neurons and connections** as evolution progresses.
    
- This gradual complexity allows NEAT to find efficient solutions without overcomplicating the network at the start.
    

**b) Genes and Genomes:**

- In NEAT, a neural network is represented as a **genome**, consisting of **genes**:
    
    - **Node genes** → represent neurons (input, hidden, output).
        
    - **Connection genes** → represent links between neurons, with weights and enabled/disabled status.
        
- Each genome encodes all the information required to build its neural network.
    

**c) Speciation:**

- To protect innovative networks from being immediately discarded, NEAT divides the population into **species** based on similarity.
    
- Networks within the same species compete primarily with each other, not with the entire population.
    
- This prevents premature convergence and encourages diversity in solutions.
    

**d) Crossover (Recombination):**

- NEAT can **combine two parent networks** to produce an offspring.
    
- During crossover, matching genes are aligned using **innovation numbers** (unique IDs assigned to new genes when mutations occur).
    
- This ensures meaningful merging of network structures.
    

**e) Mutation:**  
NEAT applies mutations in two main ways:

1. **Weight Mutation:** Slightly changes the weight of existing connections.
    
2. **Structural Mutation:**
    
    - **Add Connection:** Connects two previously unconnected neurons.
        
    - **Add Node:** Splits an existing connection to add a new neuron.
        

- Structural mutations allow the network to grow in complexity over time.
    

**f) Fitness Evaluation:**

- Each network is tested on the task it is meant to solve (e.g., controlling a robot, playing a game).
    
- Networks that perform better have a **higher fitness score** and are more likely to reproduce.
    
- Over generations, the population evolves networks that are better adapted to the task.
    

---

**3. Advantages of NEAT:**

- **Automatically evolves network structure** → no need to manually design hidden layers.
    
- **Protects innovation** via speciation → avoids losing potentially useful structures.
    
- **Efficient growth** → networks start simple and only become complex when needed.
    
- Can solve problems traditional backpropagation struggles with, like reinforcement learning tasks or dynamic environments.
    

---

**4. Applications:**

- Game AI (e.g., evolving agents in video games).
    
- Robotics (e.g., controlling robots for walking or balancing).
    
- Optimization and control problems.
    
- Simulations requiring adaptive, evolving behavior.
    

---

**5. Summary of the NEAT Process:**

1. **Initialize:** Start with a minimal population of simple neural networks.
    
2. **Evaluate:** Test each network on the task and assign fitness scores.
    
3. **Speciate:** Group similar networks into species.
    
4. **Select & Reproduce:** Use fitness-based selection, applying crossover and mutation to produce offspring.
    
5. **Mutate:** Apply weight and structural mutations to offspring.
    
6. **Repeat:** Continue over generations until a solution meets the performance goal.