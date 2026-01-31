### Meaning

A **CDN** is a network of **distributed servers** that deliver **web content (images, videos, scripts, etc.) to users** from a server **closest to their location**.

- Reduces latency and improves load times.

---

## 1. How CDN Works

1. Origin server hosts the content.
    
2. CDN caches copies of content in **edge servers** around the world.
    
3. When a user requests content:
    
    - Request goes to the **nearest edge server**
        
    - If content is cached → delivered immediately (**cache hit**)
        
    - If not → fetched from origin server (**cache miss**)
        

---

## 2. Benefits

- **Faster content delivery** (lower latency)
    
- **Reduced load** on origin server
    
- **High availability**: multiple servers = less downtime
    
- **Scalability**: can handle sudden spikes in traffic
    

---

## 3. Common Use Cases

- Websites serving images, videos, CSS, JS files
    
- Streaming services (Netflix, YouTube)
    
- Software downloads
    
- API responses
    

---

## 4. Examples of CDN Providers

- Cloudflare
    
- Akamai
    
- Amazon CloudFront
    
- Fastly
    

---

## 5. Memory Hook

- Think: **“Copy your website to servers everywhere → users get it fast”**
    
- CDN = “global cache for your website”
    

---

## 6. One-Line Exam Answer

> A CDN (Content Delivery Network) is a network of distributed servers that deliver web content from the nearest server to users, improving speed, availability, and scalability.