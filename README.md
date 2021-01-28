# UISpec

•Homepage
*Header
  Button(New User -> creates _Form_)
  Option(Hide Disabled User -> manipulates _List_)
  Button(Save User -> saves _Form_)
*Body
  *List(User -> added by _Form_)
    Columns
      *ID (int)
      *User Name (string)
      *Email (string)
      *Enabled (boolean)
  *Form[New User <-]
    Fields
      *Username
      *Display Name
      *Phone
      *Email
      *User Roles
        -Dropdown(Placeholder = "Select user roles...")
          -Options
            *Guest
            *Admin
            *SuperAdmin
      *Enabled
        -Checkbox(Default = False)
   
    
         
  

  
  
  
