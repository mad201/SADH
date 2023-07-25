def is_potential_scam(email_content):
    scam_keywords = [
        "urgent",
        "win",
        "lottery",
        "inheritance",
        "bank account",
        "Nigerian prince",
        "dear friend",
        "password",
        "verify",
        "login",
    ]
    
    email_content_lower = email_content.lower()
    
    for keyword in scam_keywords:
        if keyword in email_content_lower:
            return True
    
    return False

def main():
    print("Scam and Hack Detector")
    print("----------------------")
    
    email_content = input("Enter the email content: ")
    
    if is_potential_scam(email_content):
        print("Warning: This email may be a potential scam.")
    else:
        print("This email seems legitimate.")
    
if __name__ == "__main__":
    main()

