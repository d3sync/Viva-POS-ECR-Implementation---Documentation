# Viva-POS-ECR-Implementation---Documentation
Documentation for Viva POS RC Application - Implementation of Viva API for countertop POS.

Currently on version #2.1.0.39#

Application allows the user to connect through a Windows(Win7 with .NET Framework 4.5.2 and higher) computer to a countertop terminal that implements Viva API as documented in their portal here => https://developer.vivawallet.com/apis-for-point-of-sale/card-terminals-devices/vivawallet-api-cl/

The main key points and the purposes of this application are:
* Minimize required time to execute a transaction
* Reduce the risk of human error during those transactions
* Be secure and transparent
* Be intuitive as to what the end user should expect.

The application aims for simplicity. 
The less you do the better.

We achieve this by using the A and Z for all things programming nothing short than Ctrl+C and Ctrl+V of course!

##How it works?

It's simple the application supports the connection for 2 countertop POS terminals for the A company and B company
The user has to simple choose the one he desires to connect to either by clicking the button in the UI or by using
Global Shortkeys Ctrl+F1 or Ctrl+F2 (Global Shortkeys are shortkeys that can be used even when the application is 
lurking in the background ). The next step is to go to the companies ERP/CRM system and simply copy the Order Code
and also the price of the order. 
This is done consecutive that means you don't have to go back and forth between the two applications. 

Here is where the magic lies. 

My application monitors the clipboard and by using Regex I am
filtering the input and fill in the required information in the app. As soon as this is done we send the SaleRequest
to the terminal.

The customer inserts or waves the terminal with his magic wand(contactless card or inserts with chip)

After the success of the transaction the user receives the STAN number of the transaction in his clipboard ready to be pasted
in the ERP/CRM system without breaking a sweat or bleeding through the eyes trying to read and manually input the required info by "hand"

The application does offer a few more tricks like logging successful transactions and logging everything for some peace and quiet. As-well as the ability to cancel a transaction and refund.


-------------
One key ingredient misses from this recipe to meet perfection. The ability to make a sale request with installments. A feature that has not yet been implemented by the Viva API.

Any questions or inqueries can be sent to d3apps [@tt] idle.gr
