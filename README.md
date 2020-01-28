# SodaVendingService

SodaVendingService is a web based tool for vending machines to facilitate the purchasing and distribution of sodas through a digital interface.

The source code is written in C#, using Visual Studio .NET Core with an MVC Framework and Razor pages. The most relevant files and their hierarchy are as follows:

    - Models
        -IndexViewModel.cs
        -Promotion.cs
        -Soda.cs
        -SodaTransaction.cs
        -VendingSession.cs
        -VendingStates.cs
        -IndexViewModel.cs
    - Views
        -Index.cshtml
    - Controller
        -HomeController.cshtml
    - WWWroot
        -inventory.json
        -transactions.json
        -promotions.json

        
# Adding Sodas to the Vending List

To add a new product to the vending list, adjust inventory.json to include the new soda and place the corresponding image representing it in the wwwroot/pictures folder. It will automatically populate it in the view.

# Managing Promotions

Promotions are triggered based on values set in the promotions.json file. There is a sample JSON object preloaded, with a 50% chance to trigger per soda purchase.

# Updating Inventory

inventory.json updates on the activation of the SoldSoda state. It is decremented every time a sold is purchased and is updated with each transaction.

# Recording Transactions

transaction.json updates on the activation of the SoldSoda state. It records the sodaId of a soda and the DateTime in which it was sold. 


