# signup


class SignUpPage {
    var username: String?
    var password: String?
    var confirmPassword: String?

 
    func validateForm() -> Bool {
       
        if username?.isEmpty == true {
            print("Username field is empty")
            return false
        }

      
        if password?.isEmpty == true {
            print("Password field is empty")
            return false
        }

        
        if confirmPassword?.isEmpty == true {
            print("Confirm password field is empty")
            return false
        }

        
        if password != confirmPassword {
            print("Passwords do not match")
            return false
        }

       
        return true
    }
}


let signUpPage = SignUpPage()


signUpPage.username = "JohnDoe"
signUpPage.password = "password123"
signUpPage.confirmPassword = "password123"


if signUpPage.validateForm() {
    print("Form is valid")
} else {
    print("Form is not valid")
}
