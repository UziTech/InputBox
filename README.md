InputBox
========

C# Input dialog for accepting information.

Usage
=====

```C#
string username = "user";//Get last username from registry or file

InputBoxItem[] items = new InputBoxItem[] {
    new InputBoxItem("Username", username),
    new InputBoxItem("Password", true)
};

InputBox input = InputBox.Show("Login", items, InputBoxButtons.OKCancel);
if (input.Result == InputBoxResult.OK)
{
    doLogin(input.Items["Username"].Text, input.Items["Password"].Text);
}
```
![](http://uzitech.github.io/images/inputbox1.png)
