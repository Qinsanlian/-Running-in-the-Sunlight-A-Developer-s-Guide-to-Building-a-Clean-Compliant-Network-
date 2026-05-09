# -Running-in-the-Sunlight-A-Developer-s-Guide-to-Building-a-Clean-Compliant-Network-
**Author: Qin Kai**  
**Version: v2.0**  
**Last updated: May 9, 2026**

---

### A few words before we begin: about tools in the “grey area”

Before you get into the actual steps, you may have used—or at least heard of—some tools that live in a grey zone, such as Cloudflare WARP, Fast-GitHub, the Watt Toolkit, and others.

I am not going to dismiss them out of hand. At an earlier point in time, they served as trail markers for many developers. Their existence and their evolution proved one thing: you don’t need to rely on complicated, shady “magic” to make your development environment work better. They helped shift the mindset away from “I must use forbidden means to reach overseas dev resources.” That was meaningful in its time.

But there is another side to see: these tools are often built by individuals or very small teams. What they lack is not technical skill—it is *legal standing*. They do not have a regulated entity behind them to vouch for the user and share liability. It’s a bit like a highly skilled doctor who holds no medical licence. The exact same technical solution, if operated by a properly licensed company, would be entirely different in its legality. That is the fundamental dilemma of personal compliance.

So our attitude towards these tools is: **appreciate them, and then gently let them go**.

*   **Do not depend on them long-term**, because their foundation is built on “working around” rather than “working within” the rules. That leaves you in a state of constant uncertainty.
*   **Do not belittle them**, because their historical role as pathfinders is real.
*   **Ultimately, step into the sunlight.** Our goal is to build a long-term solution that lets you feel at ease—a fully compliant one. That is the foundation on which real creative work happens.

---

### 1. First step: ask your school if there is already a “school bus”

Before you start building your own “vehicle”, there is one option that is the easiest, the most compliant, and the cheapest: **ask your school.**

Contact your university’s network center or IT office. You can ask something like:

> “Hello, I’m a student in the XX department. For my daily development and study, I need stable access to GitHub and various technical documentation. I’d like to find out if the school provides a VPN service. If so, what is the application process like?”

Among all the options, this is the **most compliant, the most worry-free, and the least maintenance-heavy**. A school VPN is backed by the legal credentials of an educational institution. Using it to access academic resources is just as compliant as using the campus network to visit the university library.

If the answer is “not yet available”, or if your application is not approved, please don’t feel discouraged. It doesn’t mean anything has gone wrong. It just means we need to walk a short stretch of road ourselves. And so, in the following pages, I will walk you through building your own clean, sunlit channel, for about the cost of two cups of bubble tea a month.

**Who this is written for:**
*   Developers who need stable access to GitHub and technical docs
*   Learners who want to watch YouTube tech tutorials smoothly
*   You—who want to solve this problem in a fully compliant way

**A core principle: do not create needs that do not exist.**
A mature developer knows how to add things, and also knows how to subtract. We solve problems only within the bounds of the rules. You’re not a ship hiding in the sewer; you’re a sail under the open sun.

---

### 2. Why I’m writing this, and the system we are dealing with

#### 2.1 Someone who almost took the wrong path

My name is Qin Kai. I’m a diploma student. A few years ago, I was also fascinated by studying all sorts of complex protocols and “disguise” techniques. That kind of technical obsession almost pulled me onto the completely wrong road. Fortunately, I was pulled back at the crucial moment. Afterwards, I spent a long time reflecting, reading through laws and regulations, and finally chose a totally different path: **running in the sunlight—meeting legitimate needs with compliant tools.**

With my own hands I built this very kind of channel: based on the SOCKS5 protocol, running inside an encrypted SSH tunnel, governed by a strict whitelist, and used *only* for study and development. The result proved itself: not only did it outperform every grey-market solution I had ever tried in speed and stability, it gave me something even more important—a genuine peace of mind.

**The most important point: this channel is for your own use. Please do not share it with others.** Doing so would push you dangerously close to the edge. **Rights and obligations always come as a pair.**

I write this to tell every young person who has had the same confusion as me: **we don’t need to fight against anything. Compliance, it turns out, is the fastest way.** Instead of spending all your energy trying to sneak around a security checkpoint, walk through it with your head held high. It’s safer, more stable, and far more efficient.

#### 2.2 Understanding it: a precision highway traffic management system

Many people picture the network censorship system as a “wall” they need to climb over. That metaphor puts us in the wrong position from the very beginning.

I would rather liken it to a **world-class, fully automated highway traffic management system.**

It deploys checkpoints across the backbone network. These checkpoints can recognise the make, appearance, and behaviour pattern of every “vehicle” (data packet). It is not a passive barrier; it is a highly precise and efficient automated enforcement network.

If the “cargo” inside your car (the data packet payload) bears clearly prohibited signatures, it will cut off your lane (your network connection) in real time. I have experienced this firsthand: because of one misoperation, my entire home network was severed for two full minutes. In that moment, I understood with stark clarity that all the little tricks an individual might master have no value of resistance against it.

**So, I choose to hold it in proper respect—and to drive in the lane it allows.**
When your “car” looks clean, behaves transparently, and is heading to a legitimate destination—you are just a student going to the GitHub “library” to do some research—it will not disturb you. It may even, in a practical sense, protect your swift passage. When you do your part right, the entire external environment, including this system, will make way for you.

---

### 3. A tool that lost control: the story of Clash

Many of you have probably used or heard of Clash. It worked like a clever “data-packet dispatcher”: it could steer different types of network traffic into different channels, based on rules.

However, when it began to be widely used to bypass network management rules, things spiralled out of control. In the end, its core developer, unable to bear the enormous legal and privacy risks any longer, chose to delete all the public code and vanished. This triggered an avalanche—hundreds of downstream projects that depended on it collapsed overnight.

The lesson this teaches us is very clear: **no matter how clever a technology is, if its foundation is built on “circumventing the rules”, its collapse is only a matter of time.** For developers, it means permanent project loss and legal jeopardy. For users, it means the sudden death of a tool you relied on, and the security vacuum that follows. **The prosperity of a grey zone is brittle. Only a solution that stands in the sunlight can give you long-term, stable companionship.**

---

### 4. Why SOCKS5? A reflection on “fingerprints”

#### 4.1 Your network “fingerprint”

In the network world, every data packet carries the unique “fingerprint” of its protocol. This fingerprint is not determined by the encrypted content you send, but by the way you establish the connection, the size distribution of packets, timing patterns, and other behavioral characteristics. Encryption protects your “cargo”, but it cannot hide your “car model”.

The current censorship system is, at its heart, a risk-assessment system based on these fingerprints. It doesn’t care too much about the colour of your car, but it can precisely identify its model and your driving characteristics.

*   **What is the problem with obfuscation protocols?**
    The core idea behind obfuscation protocols is to **forge a fingerprint**—for example, to make your traffic look exactly like ordinary web browsing. But think for a moment: isn’t the act of “disguising” itself a highly suspicious feature at a security checkpoint? Who is more trustworthy: someone who must use a falsified identity, or someone who presents themselves plainly and honestly? **Do not position yourself as a person who needs to hide their tracks. That positioning itself will push you step by step deeper into the grey zone.**

*   **Our choice: a naturally clean fingerprint**
    The **SOCKS5 over SSH** approach has a fingerprint that is simply itself—a standard SSH encrypted connection. What is that like? It’s like a yellow utility vehicle with “Electrical Emergency Repair” printed on its side. It drives on the road, and millions of sysadmins all over the world use the exact same thing every single day for remote server administration. Its traffic pattern is so common, so normal, that in the risk model of the censorship system it comes close to background noise—it is “benign.”

**Rather than painstakingly forging a fake identity, it’s better to be born with a clean, widely recognised one. That is the entire logic behind our choice of SOCKS5.**

#### 4.2 A clear comparison

| Dimension | **Sunlight Channel (SOCKS5 + SSH)** | **Grey scheme (Shadowsocks/Trojan, etc.)** |
| :--- | :--- | :--- |
| **Traffic Fingerprint** | **Genuine and clean**: standard remote admin traffic. | **Deliberately forged**: disguised as ordinary web traffic. |
| **Risk Assessment** | **Normal**: the system sees you as an admin maintaining a server. | **Suspicious**: why would a normal person forge their fingerprint? |
| **Long-term Risk** | **Extremely low**, unless the SSH protocol itself is banned. | **High**; once the fingerprint database updates, the disguise fails instantly. |
| **Maintenance Cost** | **Very low**; a single command, stable in the long run. | **High**; you must constantly chase new disguise methods. |
| **Compliance** | **Transparent**; can withstand any compliance audit. | **Grey**; the legal risk is entirely on the user. |

We have no strong need for hiding. We are just a person who wants to read books at the GitHub “library”. When there is no such need, do not pile on unnecessary pretense. **You are not a rat in a sewer; you are the sun at eight or nine in the morning.**

---

### 5. A checklist before we set off

| What you need | What it’s for | Approximate cost |
| :--- | :--- | :--- |
| **An overseas VPS** | The overseas “relay station” for your data traffic | A few dozen yuan per month |
| **Your own domain name (optional but recommended)** | A nice, memorable signboard for your relay station | A few dozen yuan per year |
| **Your computer** | Your everyday development environment | You already have it |
| **An SSH client** | Built into your computer; on mobile, Termius is recommended | Free |
| **A proxy client** | On desktop: Clash Verge Rev; on mobile: SocksDroid | Free |
| **Patience and respect for the boundaries** | The most important preparation of all | Priceless |

---

### 6. Choosing the site for your “relay station”: purchasing a server

#### 6.1 Some reliable options

Here are a few providers I’ve used myself or that have been verified through long-term, trustworthy sources. **There are no commercial promotions here.**

| Provider | Characteristics | Recommended regions |
| :--- | :--- | :--- |
| **Tencent Cloud Lighthouse** | From a major, compliant company; often has student discounts | Hong Kong, Singapore |
| **RackNerd** | Very budget-friendly; a good fit for students with a tight budget | USA (latency will be higher) |

> **A note on payment**: If you have a foreign currency card such as VISA or MasterCard, purchasing overseas services will be smoother. This is just a reference to broaden your payment options; please assess payment security for yourself.

#### 6.2 Region choice: balancing distance and experience

*   **Hong Kong**: Physically closest; latency around 30–50 ms. The top pick for daily development—the smoothest experience.
*   **Singapore / Japan**: Excellent fallback options in the Asia-Pacific region; latency around 80–150 ms.
*   **USA**: Lowest cost, but highest latency (>180 ms). You’ll feel a slight “sluggishness”; best used as a backup node.

#### 6.3 A sufficient configuration

**Recommended starting point: 1 vCPU / 2 GB RAM / 60 GB SSD / 1 TB monthly traffic.** This is more than enough to run one SSH tunnel smoothly.

#### 6.4 A sincere reminder

An overseas server is **by no means a place beyond the reach of law**. Everything you do is subject to the laws of your country. This guide only shows you how to set up a channel for compliant development work. **Please do not use it to do anything that breaks the rules.** If at some point you feel you are being “targeted”, first examine whether any of your own actions have crossed the line.

---

### 7. Giving your “relay station” a name: buying a domain (optional, but recommended)

A domain maps a hard-to-remember IP address (`123.45.67.89`) into a name you can easily say and recall (`my-dev-space.top`).

**One small suggestion: spend those few dozen yuan on a paid domain.** Suffixes like `.com`, `.top` cost about the same as a couple of milk teas for the first year. You can get them on platforms like Namecheap, or through cloud providers.

Why not use free domains like `.tk`? Because they have a long history of abuse; their trust level is extremely low, and many places will flag them as “dangerous”. More importantly, you only have the right to use them, not to own them. The provider can take them back at any time. A few dozen yuan buys you stable ownership and long-term peace of mind. That trade-off is very, very worth it.

---

### 8. First thing after moving in: securing your “relay station”

A brand new server exposed to the public internet is scanned every minute by automated programs all over the world. We need to harden its security immediately. We recommend `Ubuntu 22.04` or `Debian 12`. Perform the following operations as the `root` user.

#### 8.1 Update the system
First, tidy the house and install the latest patches.
```bash
apt update && apt upgrade -y
```

#### 8.2 Create a user account that belongs to you
Don’t stay on the `root` account, the one with supreme power. It’s too dangerous. We create a normal user and give it `sudo` rights so it can do administrative tasks.
```bash
# Replace 'qinkai' with a name you like
adduser qinkai
usermod -aG sudo qinkai
```

#### 8.3 Use a “key” instead of a password for login
Password logins can be leaked and are vulnerable to brute force. We use an SSH key pair—you hold the private key, the server holds the public key; only when the two mate can you authenticate.

1.  **On your own computer’s terminal**, generate a key pair:
    ```powershell
    # The -C flag lets you add your email as a label
    ssh-keygen -t ed25519 -C "your_email@example.com"
    ```
    Just press Enter through all the prompts. This will create two files: the private key `id_ed25519` and the public key `id_ed25519.pub`.

2.  **“Install” the public key onto your server**:
    ```powershell
    # Replace <VPS_IP> with your server's IP
    type $env:USERPROFILE\.ssh\id_ed25519.pub | ssh root@<VPS_IP> "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"
    ```

3.  **Test it**: **Don’t close the current window.** Open a new terminal window and try logging in with the key:
    ```powershell
    ssh -i $env:USERPROFILE\.ssh\id_ed25519 root@<VPS_IP>
    ```
    If it logs you straight in without asking for a password, success!

#### 8.4 Disable password login and the high-risk entry point
Now we plug the two most dangerous holes: prevent `root` from logging in directly, and disable password authentication entirely.
Edit the SSH config file:
```bash
sudo nano /etc/ssh/sshd_config
```
Find and modify the following lines so they look exactly like this (if there’s a `#` at the start of the line, remove it):
```
PermitRootLogin no
PasswordAuthentication no
PubkeyAuthentication yes
```
Save and exit, then restart the SSH service:
```bash
sudo systemctl restart sshd
```
**Important: from now on, you can only log in with the normal user you just created (e.g. `qinkai`) plus your key file.**

#### 8.5 Install a “security door” on the server: a firewall
We use `UFW`, a simple firewall tool. But first, let’s change the default SSH port to avoid scanner noise.
```bash
# Edit the SSH config again
sudo nano /etc/ssh/sshd_config
# Find the line "#Port 22", change it to "Port 2222" (and remove the #)
```
Restart SSH: `sudo systemctl restart sshd`. **Note: your login port is now 2222.**

Now configure the firewall:
```bash
sudo ufw default deny incoming    # Deny all inbound traffic by default
sudo ufw default allow outgoing   # Allow all outbound traffic
sudo ufw allow 2222/tcp            # Open a small door only for port 2222
sudo ufw enable
sudo ufw status verbose            # Check; ensure only 2222 shows ALLOW
```

#### 8.6 Enable network acceleration and limit login attempts
These last optimisations make your server’s network smoother and safer.
```bash
# Enable BBR to optimise network performance
echo -e "net.core.default_qdisc=fq\nnet.ipv4.tcp_congestion_control=bbr\nnet.ipv4.tcp_fastopen = 3\nnet.ipv4.tcp_slow_start_after_idle = 0" | sudo tee /etc/sysctl.d/99-sunshine.conf
sudo sysctl -p /etc/sysctl.d/99-sunshine.conf

# Limit SSH connection attempts to thwart brute-force attacks
echo -e "MaxSessions 10\nMaxStartups 3:50:6\nLoginGraceTime 30s" | sudo tee -a /etc/ssh/sshd_config
sudo systemctl restart sshd
```

#### 8.7 DNS resolution and SSL certificate (optional)
If you bought a domain, go to its DNS management panel and add an A record pointing the domain to your server’s IP. **Note: do not enable any CDN or “cloud acceleration” features**, as this would contradict our principle of “protocol transparency.” Because the SSH tunnel itself is already encrypted, an SSL certificate is not a strict requirement. If you need one, you can use `acme.sh` to apply for a free certificate.

---

### 9. Lighting up your “Sunlight Channel”: building and verifying the tunnel

At last, the core step. You’ll find it’s much simpler than you imagined.

#### 9.1 Opening the channel

On your computer’s terminal, run the following command. I’ll explain what each part does:
```powershell
ssh -i "C:\Users\YourName\.ssh\id_ed25519" -N -D 1080 -p 2222 -o ServerAliveInterval=60 -o ServerAliveCountMax=3 -o ExitOnForwardFailure=yes qinkai@<Your_VPS_IP>
```
*   `-i "C:\...\id_ed25519"`: **This is your key**; tells the computer to use it for authentication.
*   `qinkai@<VPS_IP>`: **Log in as the normal user you created.**
*   `-p 2222`: **Knock on the door we set up for ourselves.**
*   `-N`: **Do not run any commands on the server**; we’re just borrowing a pathway.
*   `-D 1080`: **Open local port `1080` on your own machine as the entry point.** Everything that enters here will travel through the encrypted tunnel and exit from the server. This is the entrance to our SOCKS5 proxy.
*   `-o ServerAliveInterval=60` etc.: **Keep the connection alive** with heartbeat signals, so it doesn’t drop from inactivity.
*   `-o ExitOnForwardFailure=yes`: **If the tunnel fails to establish, exit immediately,** rather than leaving you wondering if it’s working.

**After you execute this, the terminal will pause and show no output. That’s normal. Do not close this window.**

#### 9.2 Feeling the first ray of “sunlight”

Open another terminal window. Try accessing GitHub through the channel you just built:
```powershell
curl.exe -v -x socks5h://127.0.0.1:1080 https://github.com
```
If a bunch of webpage code comes rushing back (something like `HTTP/2 200` and HTML content), congratulations! The tunnel is working.

#### 9.3 Letting your browser and apps use the tunnel intelligently: configuring Clash Verge Rev

We need a smart dispatcher—one that automatically sends traffic to GitHub through the tunnel, and lets domestic sites go directly.

1.  Download and install [Clash Verge Rev](https://github.com/clash-verge-rev/clash-verge-rev/releases).
2.  Open it, create a new profile, and paste the following content in its entirety:

```yaml
# Local proxy port
mixed-port: 7897
# Only allow local machine to use it; adds security
allow-lan: false
# Rule mode: most flexible
mode: Rule
log-level: info

# Define our just-built "Sunlight Channel"
proxies:
  - name: "Sunlight Channel"
    type: socks5
    server: 127.0.0.1
    port: 1080

# Create a proxy group that lets you manually choose between channel and direct
proxy-groups:
  - name: "Manual Select"
    type: select
    proxies:
      - "Sunlight Channel"
      - DIRECT

# The most crucial whitelist rules: only dev-related sites go through the channel; everything else goes direct
rules:
  - DOMAIN-SUFFIX,github.com,Manual Select
  - DOMAIN-SUFFIX,gitlab.com,Manual Select
  - DOMAIN-SUFFIX,google.com,Manual Select
  - DOMAIN-SUFFIX,stackoverflow.com,Manual Select
  - DOMAIN-SUFFIX,youtube.com,Manual Select
  - DOMAIN-SUFFIX,ytimg.com,Manual Select
  - MATCH,DIRECT
```
3.  **Save and “activate” this profile**, then turn on the `System Proxy` switch in the app’s main interface. Your browser is now managed by it.

⚠️ A Gentle but Firm Ethical Note on Clash Verge Rev

Clash Verge Rev is a powerful network routing tool. In this handbook, we only recommend using it as a client to connect to the SOCKS5 tunnel you built yourself—your own private, compliant lane under the sun.

We feel a deep responsibility to tell you this:

Never import nodes from unknown sources. The internet is full of "free nodes" and "airport subscription links". You have no idea who runs them or what they're really after. They can log everything you do online, steal your passwords and private data, or even use your device as a middleman for illegal activities. Please, don't take that risk.

Never share your personal tunnel. The SSH tunnel you set up following this guide is your resource—paid with your own money, protected by your own key, and carried on your own shoulders. If you share it with others, their risks become your risks, and that can quickly cross legal boundaries. Keep it yours.

Your allowlist is your last line of defense. Please keep the strict allowlist rules in your configuration file. They make sure your tunnel is only used to reach the development resources you really need—not that one sketchy site you got curious about, and definitely not what someone else might trick you into visiting.

The whole purpose of this handbook is to show you how to use compliant tools to walk a bright, open road. If you take this same tool and mix in nodes of unknown origin, you're not just betraying all the effort we've put into this—you might just push yourself back toward the edge. Tools don't have morals. You do.

#### 9.4 Using it on your mobile phone

1.  Install **Termius** and import your `id_ed25519` private key file.
2.  Add a Host: set the address to your server IP, port `2222`, username to your normal user, and authentication to `Key` (select your imported key).
3.  Save and connect. Then, under “Port Forwarding”, add a new rule: type `Dynamic`, local port `8443`.
4.  Install **SocksDroid**. Set the proxy address to `127.0.0.1`, port `8443`, then toggle the switch on. When you’re done, remember to disconnect in Termius.

#### 9.5 A few tips, and “what if…”

*   **The whitelist is your seatbelt.** It ensures that even if you carelessly visit a non-dev site, the traffic goes directly—not through the channel. This is crucial.
*   **The tunnel dropped?** Check if the terminal window is unresponsive. Sometimes ISPs interfere with non-standard ports. You can try changing the server’s SSH port to `443`.
*   **A website doesn’t open?** Check whether Clash’s `System Proxy` is turned on, or if the website is missing from the whitelist.
*   **Close it after use.** Just close the terminal window that shows no output, or press `Ctrl+C`. It’s a good habit.

---

### 10. Real-world test: how fast is the Sunlight Channel?

**Test environment**: my home broadband, Changzhou, Jiangsu. Server is an entry-level RackNerd box in Chicago.

| Scenario | Download speed | Upload speed | Latency |
| :--- | :--- | :--- | :--- |
| Direct access to GitHub, no channel | ~2 Mbps | ~1 Mbps | >300 ms |
| **Using the Sunlight Channel** | **~408 Mbps** | **~108 Mbps** | **~192 ms** |

This result far exceeded my expectations. It didn’t behave like some grey-market tools—a brief explosion of speed followed by massive connection drops. It was stable, clear, and reliable, like a true “express lane”.

---

### 11. Advanced topics: chain proxy, and “clean IPs”

If you have more complex needs—for example, needing an exit IP from a specific region—you can chain two servers together (your machine → Server A → Server B → target site). But for a beginner, this isn’t necessary right now.

We want to state one position clearly: **we will not explain, recommend, or teach how to get so-called “clean IPs” or “residential IPs.”** In the current landscape, this concept is deeply entangled with cybercrime and grey-market tool chains. For an individual developer, the cleanest, most audit-proof option is always the server IP you rent from a legitimate cloud provider. Behind that IP stands a legal entity that must obey the law.

We also do not introduce a CDN into this setup. A CDN hides your server’s real IP, which goes against our principle of “protocol transparency, genuine fingerprint.” **Please don’t wrap your traffic in third-party services you don’t truly understand.**

---

### 12. Final words: hold the boundary, to protect freer creation

Now, the channel in your hands is something you’ve built under the sunlight—with respect for the rules, sincerity towards the technology, and your own hands. It is clean.

Please keep a few small habits:

*   **Before using it, glance at the purpose:** Yep, this site is for reading technical documentation.
*   **While using it, tighten the boundary:** Let the whitelist rules protect you. Don’t probe the edges out of “curiosity”.
*   **After using it, turn it off:** Save resources, and reduce risk.
*   **Most importantly, ask yourself from time to time:** If I look at what I’m doing, can I feel at ease? That sense of ease is the very core of compliance.

We walk this path not because we are afraid, but because we have found: this is the straightest, fastest road to free creation. **Compliance, it turns out, is the fastest way.**

This is our “Sunlight Channel”.

---

### Appendix: a gift from the community—a whitelist of developer domains

You can add the following domains to your Clash whitelist rules as needed.

*   **🤖 AI models & coding**: `openai.com`, `chatgpt.com`, `claude.ai`, `deepseek.com`, `huggingface.co`, `openrouter.ai`, `cursor.sh`, `githubcopilot.com`, etc.
*   **🗂️ Code hosting**: `github.com`, `githubassets.com`, `gitlab.com`, `bitbucket.org`, etc.
*   **📦 Package registries**: `npmjs.com`, `pypi.org`, `crates.io`, `cdn.jsdelivr.net`, etc.
*   **☁️ Cloud & containers**: `aws.amazon.com`, `cloudflare.com`, `docker.com`, `hub.docker.com`, etc.
*   **📚 Technical docs & communities**: `developer.mozilla.org`, `nodejs.org`, `stackoverflow.com`, `medium.com`, etc.
*   **🎬 Tech videos**: `youtube.com`, `ytimg.com`, `vimeo.com`, etc.

*(For a more complete list, check the `category-dev` list maintained by the `v2fly/domain-list-community`—it’s one of the most comprehensive community-recognised collections.)*

---

### One important addition: don’t forget your student status

If you are a student, before you pay for anything, there’s a completely legitimate, high-value benefit you may have overlooked: the **[GitHub Student Developer Pack](https://education.github.com/pack)**.

Verify your student status using your school email (e.g., an `.edu` address), and you’ll get free access to a whole set of pro developer tools, such as:
*   **GitHub Pro** and **GitHub Copilot**: the AI assistant that helps you write code.
*   **A free .me domain from Namecheap**.
*   **Free credits for cloud services like DigitalOcean**.

These resources are backed by GitHub’s official student verification—fully compliant. Go and apply for this first; it can save you a good amount of money. Before you start building, please check what your student status can unlock for you. This fits perfectly with the philosophy of our guide: when ready-made, compliant resources exist, use them first.

