Perfect — you’ve successfully **created a named tunnel** (`myapp-tunnel`). Now you can configure it to run continuously and optionally associate it with your No-IP domain if you want, or just use a stable Cloudflare URL. Here’s what to do next:

---

### **Step 1: Create a config file**

Create a `config.yml` in:
`C:\Users\aa591\.cloudflared\`

Example content if you want the tunnel to point to your local app (`localhost:8080`):

![[Pasted image 20250818144122.png]]
- If you don’t want to use your No-IP domain, just leave the `hostname` line out. The tunnel will generate a stable `trycloudflare.com` URL.

---

### **Step 2: Run the tunnel**

`cloudflared tunnel run myapp-tunnel`

- If you included `hostname`, it will try to resolve through your No-IP domain.
- If you left it out, you’ll get a **stable Cloudflare URL**.

---

### **Step 3 (optional): Install as a Windows service**

To make the tunnel **run permanently in the background** (so it survives reboots):
`cloudflared service install`

- After this, the tunnel will start automatically whenever your PC boots.
- You can still stop it manually if needed:

`cloudflared service uninstall`