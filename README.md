# Recon
#### Recon Flow
#### Thu thập doamin,subdomain (tools amass): amass enum -d (hostname)
#### nmap  (hostname hoặc ip) 
#### port range (-p1-65535)
#### Scan speed -T0 -T1 ... -T5
#### Tìm version -sv
#### OS -O
#### Có thể dùng shodan (phải nạp card)
# Từ Nslookup ta biết được gì 
#### Có thể thấy được Ip của domain đấy (có thể chung dải mạng) nslook up (hostname)
# Ports/Service những dịch vụ đang chạy trên server
#### namp,rustscan,metabigor 
#### nmap -p- (hostname)
# Nếu service là web thì phải pentest
#### Technology stack, Dỉrectories Scan, Paramester Scan
# Technology stack
#### wappalyzer 
# Directories Scan
#### ffuf -w common.txt -u http://hostname/FUZZ -fc 302
#### -h gắn thêm 1 header nào đấy vào request 
#### -fc filter kh muốn thấy cái gì đấy (vd: 403)
#### -ac tự động loại bỏ mấy cái k liên quan dùng trong trường hợp scan nhiều host
#### -e thêm những extentions sau chứ FUZZ (vd ban đầu wordlists là test sau khi  thêm .txt,.php)
# Paramester Scan
#### arjun -u (hostname)
# Tip and tricks
#### Nếu bị lỗi ở 1 chỗ rất có khả năng bị ở những chỗ còn lại 
#### có SSH burte force login, check version
#### Tìm đùng hostname trỏ đến IP nào thì dùng curl -ik (IP_HERE) -H "HOST: domain_HERE"
