# PPC/NC isPrime
We will be blasted 50 numbers to reply whether it is prime or not, so this is for automated solving, here was my Python script for connecting and receiving/sending data. 
```
from time import sleep
import socket

sock = socket.socket()
sock.connect(("86.57.166.23", 9000))

def add(num): #function for stripping strings to three digit number then reply
	x = int(num[num.index("/50")+3:].strip())
	answer = ""
	for i in range(2, int(x/2)+1): #prime number confirmer
		if (x % i) == 0:
			answer = "NO"
			break
		else:
			answer = "YES"
	return answer

while True:
	sleep(1)
	data = sock.recv(1024).decode('utf-8')
	if "grodno{" in data: #check for flag
		print(data)
		break
	else:
		reply = add(data)
		print (reply)
		sock.send((str(reply) + '\r\n').encode())
sock.close()

```
Flag was grodno{3128c0pr!m3_numb3r_!s_d!v!s!b13_0n1y_by_1_4nd_by_!+s31f4f8801}
