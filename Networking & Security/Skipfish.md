## 1️⃣ Definition

**Skipfish** is an **open-source web application security scanner** developed by **Google**.

- Used to **automatically scan web applications** for **security vulnerabilities**
    
- Performs **active reconnaissance** and generates **comprehensive security reports**
    
- Written in **C** for high performance
    

---

## 2️⃣ Key Features

|Feature|Description|
|---|---|
|Fast scanning|Multi-threaded scanning engine|
|Recursive crawling|Automatically explores website links|
|Vulnerability detection|Detects **XSS, SQL injection, CSRF, directory traversal**, etc.|
|Security report generation|Generates **HTML reports with detailed findings**|
|Low false positives|Optimized to reduce unnecessary alerts|
|Customizable|Allows tuning scan scope and rules|

---

## 3️⃣ How Skipfish Works

1. **Crawling**: Collects all URLs from the target website
    
2. **Dictionary-based fuzzing**: Uses a **built-in wordlist** to test parameters for vulnerabilities
    
3. **Request analysis**: Monitors HTTP responses for **error codes, anomalies, or potential exploits**
    
4. **Report generation**: Produces an **interactive HTML report** highlighting risks
    

---

## 4️⃣ Installation (Linux Example)

# Install dependencies  
sudo apt install build-essential libssl-dev  
  
# Download Skipfish  
wget https://github.com/spinkham/skipfish/archive/master.zip  
unzip master.zip  
cd skipfish-master  
  
# Build  
make

---

## 5️⃣ Basic Usage

./skipfish -o output_folder https://example.com

- `-o output_folder` → specifies output directory
    
- URL → target website
    

After completion, the folder contains:

- `index.html` → main security report
    
- `*.html` → detailed pages for each vulnerability
    

---

## 6️⃣ Common Options

|Option|Description|
|---|---|
|`-o <dir>`|Output directory for reports|
|`-W <wordlist>`|Custom wordlist for fuzzing parameters|
|`-S`|Skip SSL certificate checks|
|`-X <regex>`|Exclude URLs matching regex|
|`-I <regex>`|Include URLs matching regex|
|`-T <threads>`|Number of threads (default = 10)|
|`-m <depth>`|Maximum crawl depth|

---

## 7️⃣ Advantages

- **Fast and lightweight** compared to other scanners
    
- Generates **comprehensive reports**
    
- Supports **large-scale scanning**
    
- **Customizable scanning rules**
    

---

## 8️⃣ Limitations

- Requires **Linux or Cygwin on Windows**
    
- Not as feature-rich as professional scanners like Burp Suite or Nessus
    
- May **miss very advanced attacks** (needs manual verification)
    
- Aggressive scans may **trigger WAF or security defenses**
    

---

## 9️⃣ Use Cases

1. **Web application security testing**
    
2. **Automated vulnerability assessment**
    
3. **Reconnaissance before penetration testing**
    
4. **Continuous security scanning** for development pipelines
    

---

## 🔟 Key Exam / Interview Points

- **Skipfish = automated web app security scanner**
    
- **Fast, multi-threaded, open-source** (by Google)
    
- Uses **crawling + fuzzing** to detect vulnerabilities
    
- Outputs **HTML reports** highlighting risks
    
- Can be customized with **wordlists, threads, include/exclude rules**