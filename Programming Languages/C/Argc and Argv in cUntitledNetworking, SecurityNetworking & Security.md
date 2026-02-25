## 1️⃣ What They Are

In C, the `main` function can take parameters to **receive command-line arguments**:

int main(int argc, char *argv[])

- **`argc`** → _argument count_
    
    - An `int` representing **how many arguments** were passed to the program
        
    - Always ≥ 1 because the program name itself counts as the first argument
        
- **`argv`** → _argument vector_
    
    - An array of **strings (`char*`)**, each representing an argument
        
    - `argv[0]` → program name
        
    - `argv[1]` → first command-line argument
        
    - `argv[argc]` → `NULL` (end of array)
        

---

## 2️⃣ Example Usage

Suppose we run:

	./program hello world

![[{7003214F-F421-472F-B177-CE517FB35D9D}.png]]

## 3️⃣ Key Notes

- `argc` counts **all arguments**, including program name
    
- `argv` is **array of pointers to strings**
    
- `argv[argc]` is always `NULL` (useful for loops)
    
- You can also declare `argv` as:
    

char **argv

This is equivalent to `char *argv[]`.

---

## 4️⃣ Typical Uses

- Reading **user input from command line**
    
- Passing **file names** or **options** to programs
    

Example: read a file name from command line:
![[{8C63A4BC-A5BC-48D2-A4B0-5376B70D6F51}.png]]Run:

./program myfile.txt

---

## 5️⃣ Common Mistakes

1. Forgetting that `argv[0]` is the **program name**
    
2. Assuming `argc` = number of user-provided arguments (it includes program name)
    
3. Not checking `argc` before accessing `argv[i]` → can cause segmentation fault