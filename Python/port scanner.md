[[scripts]]

import socket

from datetime import datetime

  

target=input("Enter the target IP address: ")

ports=[80,443,8080,21,22,23,25,110,143]

  

now = datetime.now()

  

f=open("c:\\users\\rswan\\documents\\python\\scanlog.txt","a")

for port in ports:

    s=socket.socket(socket.AF_INET, socket.SOCK_STREAM)

    s.settimeout(1)

    result=s.connect_ex((target,port))

    if result==0:

        print(f"Port {port} is open")

        f.write(f"Port {port} is open\n")

    else:

        print(f"Port {port} is closed")

        f.write(f"Port {port} is closed\n")

  

    s.close()

  

x = time.time()

print("Timestamp: ", x  )

print(now)

f.write("Timestamp: " + str(x) + "\n")

f.write(str(now) + "\n" "\n")

f.close()