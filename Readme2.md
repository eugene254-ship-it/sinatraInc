Why is this Project essential:
![images](https://user-images.githubusercontent.com/72182017/222767451-2b10cd9c-befb-4aad-a8d2-038fdcd0449d.jpg)

Sponsor this Project
Overview Overview
In 2020, the outbreak of the new crown virus has greatly reduced the travel frequency of consumers, and the offline business of merchants has suffered heavy losses. As a result, many merchants shifted their business focus to online, mitigating the impact of the virus through contactless delivery. During this special period, merchants and consumers are increasingly demanding online food delivery software.

In the year of 2020, the outbreak of COVID-19 has significantly decreased people's intention of hanging out, which was a disaster to offline business. Therefore, myriad shops have switched their focus of business from offline to online to mitigate the impact of COVID- 19 by contactless delivery. During this unusual period of time, the importance of delivery apps kept growing.

Based on this, the "Little Crocodile Running Errands" project was established in July 2020, aiming to build a platform to provide online ordering and offline delivery errand services for Chinese people in the Miami area of the United States during the epidemic.

Based on that, the project, Little Crocodile Delivery, was created in the July of 2020 in order to build a platform and provide online ordering, offline delivery service to the Chinese people in Miami, US.

This project is developed based on the native MINA framework of the WeChat applet, and the front-end and back-end connections are realized through the cloud development function provided by the WeChat developer tool. For background database design, please refer to the sample data

This project is developed based on the original MINA framework of WeChat Mini-Program. The connection of front end and back end is made by Cloud Development provided by WeXin DevTool. Please refer to sample data for the design of database

The project realizes three user terminals: customer terminal (C terminal), merchant terminal (B terminal), and management terminal (A terminal). The three terminals are all integrated in a small program, and the user can switch within the small program. All Mini Program users can enter the customer side unconditionally, and only the store owner or clerk who has registered the store in the background can enter the merchant side. The management terminal needs to enter the exclusive password by the registered administrator in a special way to be able to enter

This project has implemented three user sides—— Customer Side (C-side), Business Side (B-side) and Administration Side (A-side). They are all integrated within the same mini program, where users can switch from one side to another. Every user can enter C-side without any condition. But only shop owners and shop assistants who have associated with a registered shop in database are able to enter B-side. The administration side is only accessible to registered administrators with their own password.

If you need to develop based on this project, please refer to the project import tutorial

If you would like to develop your own program based on this project, please refer to Tutorial for importing this project

The main modules and their main functions of the three terminals are listed as follows:

The main modules and features of the three sides are listed as follows:

Customer side Customer Side
Delivery Service Module Delivery Service Module

shopping cart
Place an order Placing Orders
Flea Market Module Flea Market Module

Upload Merchandise Upload Merchandise
Merchant side Shop Side
Order Management Module Order Management Module

Order Taking
Processing Order Handling
Delivery Order Delivery
Cancel Order Cancellation
Shop Management Module Shop Management Module

Merchandise Management Merchandise Management
Shop Assistant Management Shop Assistant Management
Fee Setting Fee Setting
Operation Setting Operation Setting
Administration Side
Administration-of-customer-side Module

Ads at Home Page
Management of Flea Market
Merchant side management Administration-of-shop-side Module

Shop Registration Shop Registration
Shop Ranking Shop Ranking
Customer Service Module Customer Service Module

View order Access Order Information
Demo of Main Business Process
Customer side Customer Side
The customer side includes two business lines: delivery service and flea market

The C-side has two main businesses: delivery service and flea market

Procedure of delivery service:
Browse products->Add products to shopping cart->Checkout->Select delivery address->Place an order->Wait for delivery.

find a product-> add to basket->checkout->select address->order placing->wait for delivery

delivery_service

Procedure of Flea-market Business
Click "Publish Product" -> fill in product information -> upload -> wait for review -> pass the review and put the product on the shelf -> wait for the buyer to contact

click "upload"->provide product info->upload->wait for reviewing->approve->wait for buyer

If the product does not pass the review, the customer can modify the product information and submit it for review again until the review is passed

If the product does not get approved, the customer may revise the product info, wait for the reviewing again and repeat this process until it gets approved.

upload_second_hand_goods

Business Side
Business on the merchant side includes order management and store management

B-side includes the management of order and shop

Order Management Order Management
Receive a new order -> receive an order -> distribution -> delivery

Customers can cancel the order at any time before the merchant accepts the order
After the merchant accepts the order, only the merchant can cancel the order. If the customer wants to cancel the order, he needs to contact the merchant by phone
order receiving->order taking->order picking->delivery

Customers can cancel an order at any time before it is taken.
If the order is taken, only the B-side has access to cancel it. Customers would have to make a phone call for cancellation.

Shop Management Shop Management
The store owner's management of the store is mainly divided into product management, clerk management and business settings.

Shop management of shop owners includes management of merchandise, shop assistant and operation setting

Commodity management is to add, delete, modify, query and sort commodity information. no demo here

Shop owners' management of merchandise is the addition, deletion, modification, query, and sorting of merchandise information, which will not be displayed here.

In the same way, the shopkeeper's management of the shop assistants can also be summarized as "adding, deleting, modifying and checking". Among them, "modify" refers to modifying the clerk's remarks and permissions.

Similarly, shop owners' management for shop assistants is also summarized as addition, deletion, modification and query

Clerk permissions include

Process the order (receive the order - complete the distribution - complete the delivery)
Modify product information (product name, price, minimum purchase quantity, etc.)
Modify store information (store announcement, whether to open the door, etc.)
Shop assistants' access includes

order handling (order taking-order picking-order delivery)
modify merchandise info (name, price, minimum quantity etc.)
modify shop info (announcement, open or close etc.)
The process of adding a new clerk is: store management tab page -> clerk management -> click "+Add clerk" to get the invitation code -> send the invitation code to the clerk -> the clerk clicks "become a clerk" on the merchant login interface -> enter Invitation code -> shop assistant registered successfully

The procedure of adding a shop assistant is: go to shop management tab->assistant management->click "+add assistant"->obtain invitation code->send to the assistant->the assistant clicks "become an assistant" at the login page of B-side->input invitation code->assistant registration successful

The following demonstrates the process of the store owner adding a new clerk and the operations that can be performed on the clerk.

The demo below displays the procedure of adding a new assistant and what you can do to him.

add_assistant

Administration Side
The business of the management end includes the management of the customer end and the management of the business end.

A-side can manage C-side and B-side

The management side can set the carousel advertisement on the homepage of the customer side, including advertisement sorting, slogan, etc. When users click on the ad, they will automatically jump to the product details page corresponding to the ad.

A-side can set the ad at the home page of C-side. The setting includes ad sorting and ad slogan. When customers click the ad, they will automatically jump to the page with detailed info of the corresponding product.

The management of the flea market on the management side is to review the commodities uploaded by users. Once an item has been reviewed, it can be placed on the flea market to be visible to all customers. If the product cannot pass the review, the administrator must state the reason before rejecting the release of the product.

Management of flea market on A-side is the reviewing of the products uploaded by C-side. Products can enter the flea market and be accessed by every customer when it is approved on C-side.

The management of the merchant side from the management side is mainly for the registration of the store and the ranking of the store under the "recommended store" on the homepage of the customer side

Management of B-side on C-side involves shop registration and the rank of a shop under the "shop recommendation" module on C-side.

The registration process of the store is similar to the process of adding shop assistants on the merchant side. The management terminal generates the store registration code and sends it to the store owner. The store owner clicks "New Merchant Registration" on the merchant login page and enters the registration code to complete the registration

The procedure to register a shop is similar with adding a new assistant. The C-side generates shop registration code and send it to a shop owner. The owner will then go to the login page of B-side, click "open a shop" , input the code and finish the registration.

The management side can modify the ranking value of the merchant. The higher the ranking value, the higher the ranking

A-side can modify the ranking value of a shop. The higher the ranking value, the higher the shop ranks.

The following demonstrates the process of reviewing the product uploaded by the user on the management side

The demo below displays the procedure of how C-side review the product uploaded by C-side.
