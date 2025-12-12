
**1. Introduction:**  
In NEAT, a **genome** is the **encoded representation of a neural network**. It contains all the information needed to build and evolve a network. Think of it as the “DNA” of a neural network—it determines its structure and behavior.

---

**2. Components of a Genome:**

1. **Node Genes:**
    
    - Represent the **neurons** in the network.
        
    - Each neuron has a type:
        
        - **Input Node:** Receives signals from the environment.
            
        - **Hidden Node:** Processes information.
            
        - **Output Node:** Produces the network’s final output.
            
    - Each node has a unique **ID** for tracking in evolution.
        
2. **Connection Genes:**
    
    - Represent **connections between neurons**.
        
    - Each connection has:
        
        - **In-node & Out-node:** The neurons it connects.
            
        - **Weight:** The strength of the connection (can be positive or negative).
            
        - **Enabled/Disabled Flag:** Whether this connection is active.
            
        - **Innovation Number:** A unique identifier for tracking historical origin of the gene (important for crossover).
            

---

**3. How a Genome Works:**

- The genome **does not compute anything** on its own.
    
- When it is “expressed” or “decoded,” the genome is used to **construct a neural network**.
    
- The resulting neural network can then **process inputs** and produce outputs.
    

---

**4. Role in NEAT Evolution:**

- **Mutation:** Genes in the genome can be mutated:
    
    - Add a new connection.
        
    - Add a new node.
        
    - Change the weight of a connection.
        
    - Enable or disable a connection.
        
- **Crossover:** Two genomes can combine to produce offspring genomes.
    
- **Speciation:** Genomes are compared to maintain diversity in the population.
    

**Key point:** The genome allows NEAT to evolve both **weights** (by mutating connection weights) and **topology** (by adding/removing nodes and connections) over generations.

---

**5. Summary:**

- A **genome is like the DNA of a neural network**.
    
- It encodes **neurons, connections, and their properties**.
    
- When expressed, it becomes a fully functioning neural network.
    
- NEAT evolves genomes to discover the best network structures and weights for a given task.
    

---

**One-line summary for revision:**  
**A genome is the encoded blueprint of a neural network that specifies its neurons, connections, and weights, allowing NEAT to evolve both structure and functionality.**