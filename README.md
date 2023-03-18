# OTP-Verification-Python
//OTP verification using Python.
import random
import smtplib

Otp = ''.join([str(random.randint(99999, 999999))])
s = smtplib.SMTP('smtp.gmail.com', 587)
s.starttls()
s.login("enosnaidu423@gmail.com", "ydnhmbqepejmnjrg")
Msg = 'Hello, Your OTP is'+str(Otp)
s.sendmail('enosnaidu423@gmail.com', 'ne3200@srmist.edu.in', Msg)
s.quit()

a = input("Enter Your OTP >>: ")
if a == Otp:
    print("Verified")
else:
    print("Please Check your OTP again")
