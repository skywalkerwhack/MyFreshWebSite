---
date: '2025-08-26T21:00:42+08:00'
#draft: true
title: '常用的vps脚本'
---

## Scripts
### SSH key validation
```
for pubkey_file in /etc/ssh/*.pub; do ssh-keygen -lf ${pubkey_file} -E sha256;  done
```
### Prefer ipv4
```
sed -i 's/#precedence ::ffff:0:0\/96  100/precedence ::ffff:0:0\/96  100/' /etc/gai.conf
```
### Server Performance Testing
* **NodeSeek Toolkit**
```bash
bash <(curl -sL https://sh.nodeseek.com)
```
* ** ECS (Go Version)**
```
export noninteractive=true && curl -L https://raw.githubusercontent.com/oneclickvirt/ecs/master/goecs.sh -o goecs.sh && chmod +x goecs.sh && bash goecs.sh env && bash goecs.sh install && goecs
```
### Proxy Setup
* **Command Line Installer (Sing-box by 233boy)**
```bash
bash <(wget -qO- -o- https://github.com/233boy/sing-box/raw/main/install.sh)
```
* **singbox on alpine linux**
```
bash <(wget -qO- https://raw.githubusercontent.com/fscarmen/sing-box/main/sing-box.sh)
```
* **Graphical Clients**
> Note: Some GUI-based VPN clients claiming to use Sing-box may prioritize user acquisition over code quality. Many include advertisements and unstable features. Use with caution.
> ~~[Nekoray GUI Client](https://github.com/MatsuriDayo/nekoray)~~ *(Deprecated/Not recommended)*

---
## Online Diagnostic & Utility Sites 
### Server Connectivity
* [tcp.ping.pe](https://tcp.ping.pe)
* [ping0.cc](https://ping0.cc/)
* [port.ping.pe](https://port.ping.pe)

### DNS Leak Detection
* [ipleak.net](https://ipleak.net/)
* [whoer.net DNS Test](https://whoer.net/dns-leak-test)
* [dnsleaktest.com](https://www.dnsleaktest.com/)

### IP & Geolocation Info
* [ip.sb](https://ip.sb)
* [ip-api.com](http://ip-api.com/)
* [ipinfo.io](https://ipinfo.io)
### WebRTC Leak Testing
* [browserleaks.com/webrtc](https://browserleaks.com/webrtc
---
## Community & Knowledge Base
### Discussion Forums
* [V2EX - Censorship Subforum](https://www.v2ex.com/go/censorship)

### GitHub Resources
* [Awesome VPN Tools](https://github.com/awesome-vpn/awesome-vpn/tree/master)
---
$\text{The END}$
