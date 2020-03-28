# E-mail Settings

By default, LaraEstimate can send e-mails with Estimates Links to the customer, through the **Share Modal**. 

But to send these e-mails, you need to set the smtp settings or change the e-mail driver in the project settings.

To set a SMTP driver, open the **.env** file that you have created when installed the system and change the following lines with your preferred SMTP service settings:

```
MAIL_DRIVER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
```

We recommend that you create a [Mailtrap](https://mailtrap.io/) account to test your e-mails during development. In production, you can use your preferred SMTP service.