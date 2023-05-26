# SMTP-Email-Verification
This code provides a simple way of verifying the mail using PYTHON
import math
import random
import smtplib

digits="0123456789"
OTP=""
for i in range(6):
    OTP+=digits[math.floor(random.random()*10)]
otp= OTP+ "is your OTP"
msg=otp
s= smtplib.SMTP('smtp.gmail.com',587)
s.starttls()
s.login("varshajayaseelan25@gmail.com","xtnv rpjy kayh tsol")

emailid = input("enter your email:")
s.sendmail('&&&&&&&&&&&',emailid,msg)
a = input("Enter your OTP >>:")
if a == OTP:
    print("verified")
else:
    print("please check your OTP again")

