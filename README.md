# Learning_doc
---
# 1. Install NginX
1. Go to NginX website [downloadlink](https://nginx.org/en/download.html)
2. Download windows zip file.
3. Extract the zipped file into a folder. For this tutorial we'll use desktop.
4. Validate that nginx.exe is present in `C:\Users\YOUR_USERNAME\OneDrive\Desktop\NginX\nginx-1.27.3`

# 2. Configure NginX with website 
1. Copy your HTML code into the HTML folder of the NginX directory `C:\Users\YOUR_USERNAME\OneDrive\Desktop\NginX\nginx-1.27.3\html`
2. Confirm if `index.html` is present in above folder.

# 3. Start NginX
1. Execute `nginx.exe` file kept inside `C:\Users\YOUR_USERNAME\OneDrive\Desktop\NginX\nginx-1.27.3`
2. Validate by opening [http://localhost](http://localhost) on browser.
3. In case nginx is not running, or a website is not visible make sure port 80 is available for use. Stop any other services if it's using port 80, and restart NginX.

# 4. Set up Domain name in local DNS
To open your website with a custom domain name you would need to have entry in local DNS for that domain pointed to your machine. Every machine has local host IP 127.0.0.1, which should be linked to your domain.
1. Add following content in your `/etc/host` file.

```
127.0.0.1 mydomain.example
```
2. In case /etc/host is not writeable, you have to open file using administrator permission.
Follow the following steps to do so 
    a. Run command prompt as administrator 
    b. Run following commands
    ```
    cd C:\Windows\System32\drivers\etc 
    notepad hosts 
    ```
    c. Enter the content given above and save the file.
3. Open your domain using [http://mydomain.example](http://mydomain.example)
