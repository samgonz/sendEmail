# sendEmail
code to send a welcome email in python

"""
Change the below text to edit the message and subject.
"""
user = input("Enter Your Name >>: ")
email = input("Enter Your Email >>: ")
message = (f"Thank you {user} for signing up to recieve emails.")
subject = (f"Welcome email for {user}.")

"""
This is the complete message that will be sent to the email provided.
"""
complete_message = 'Subject: {}\n\n{}'.format(subject, message)

"""
This is the SMTP information to be able to send the email to the email provided.
"""
s = smtplib.SMTP('smtp.gmail.com', 587)
s.starttls()

"""
Edit the below login info
Change email to your email. 

Change password to the email of your choice.

Suggestion if using gmail, create an app password
See below webpage on how to use and create an app password.
https://support.google.com/accounts/answer/185833?hl=en
"""
s.login("email@email.com", "password")
s.sendmail('&&&&&&&&&&&', email, complete_message)

print("Email Sent!") 
