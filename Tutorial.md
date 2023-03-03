A project import tutorial that Xiaobai can understand
If you want to download this project, run it through, and make some modifications on this basis, please refer to this tutorial.

Since this project uses cloud development, we will encounter various problems if we simply download the code and choose to import this project in the WeChat developer tools, especially the debugger will report that it cannot find relevant data. So in addition to importing related codes, we also need to adapt some data to the current cloud environment to make related functions run smoothly.

Each step in the tutorial has an animation demonstration, please wait patiently for loading or downloading before reading

Download this project and unzip it
do not repeat

Create a local project directory
My project folder here is named yourProjectFolder, just name it according to your own project

Image DESCR

Create a new project in WeChat developer tools
Fill in the project name according to the actual situation. Select the folder we created just now for the directory. Fill in your own appid. Make sure to check "Mini Program Cloud Development" and click New

Image DESCR

get your openid
openid is the unique identification code of each WeChat user in the WeChat applet

After clicking New, the development tool will automatically create an example of cloud development. Click "Click to get openid" in the emulator, then copy our openid in the debugger and save it.

You can create a new text file and save it temporarily like I did. If you know that win+v can view the clipboard, there is no need to create a new file

Image Descr

Get your cloud environment id
Click Cloud Development, click Settings in the Cloud Development Console, and copy the cloud environment id

Image Descr

Copy the downloaded project code to the project directory
After deleting the original files in the project directory, replace the project code in the

miniprogram folder
cloudfunctions folder
project.config.json
Copy to the project directory

Image Descr

Modify project configuration
Search for wx2604ce53df094ce9 in the developer tools search bar
Click on the search result to jump to the project configuration page
Modify the appid to our current appid and the project name to the current project name
save
Then search env-miamielm-5gliunnq19c0a342
Replace all results with the current cloud environment id
save

Image Descr

Upload and deploy all cloud functions
Expand the first folder (cloudfunctions) under the project directory

Right-click on each function and select Upload and Deploy: Cloud Install Dependencies (do not upload node_modules)

Image Descr

Modify sample data
Go to the "Sample Data" folder. Here I let VScode start from the current directory, so that I can use Vscode to find and replace in all files

Find oKXRg5euQbUoF74HQgN-FdJMwRSE and replace all results with our current openid

so that the data is considered to have been created by you

IMage Descr

Import the modified data into the cloud database
Open the cloud console
Choose cloud development
select database
Delete the data that comes with Mini Program Cloud Development
Create data tables with the same name as the sample data one by one
Import the sample data into the data table and modify the permissions of the data table to be readable and writable by everyone (you can modify the permissions of the data table later as needed, here to ensure that the program runs smoothly, it is deliberately set to be readable and writable by everyone)
Do the same for all data tables

Image Descr

So far, the cloud functions and database data used in the project have been successfully adapted to the current cloud environment. The applet can run at this time, but it will report a rendering error. This is because the image that needs to be loaded cannot be found in cloud storage. Now let's fix this

Modify the background image of the flea market and login page
Open the cloud development console and select storage
Upload the "system" folder
Copy the FileID of login.jpg, login2.jpg and fleaMarket.png

Image Descr

open database
Click on the ugShop form
Change the value of the logoUrl field to the FileID of the copied fleaMarket.png just now (win+V can bring up the clipboard)

Image Descr

Go back to the developer tool editor, press ctrl+p, enter selAppEnd, click selAppEnd.wxml to jump to the corresponding file
Change the value of the src attribute of the image component in the second line of the file to the FileID of the previously copied login.jpg, and then save it
Also enter login through ctrl+p, click login.wxml under miniprogram\ShopEnd\pages\localPages\login to jump to the corresponding file (note: the jump in the animation is inconsistent with this)
Also modify the src attribute value of the image component in the second line to be the FileID of login2.jpg

Image Descr

Set Homepage Carousel
If you are currently on the client side, click "My", scroll down and click "Logout Client"
Enter the merchant side
Click "New Business Registration"
Enter aadminlogin1017 to enter the management terminal
Click "Set Homepage Carousel"
Delete the original blank carousel image
Click "+" to upload the pictures under the "Pictures" folder to the corresponding product
Do the same for carousel image 2
Click "Save" at the bottom of the page

Image Descr

Set the store logo of valencia chain supermarket and chef chen Chinese restaurant
Open the cloud development console
Create new folders named "smBP9uFxmTxRv" and "smBxLqkKS9xxn"
Upload logoValencia.jpg under the "Pictures" folder in "smBxLqkKS9xxn" and copy the FileID
Upload chef_logo.jpg under the "Pictures" folder in "smBP9uFxmTxRv" and copy the FileID

Image Descr

open database
Open the "shop" dataset
Check the shopName of the first piece of data. If it is a valencia chain supermarket, change the value of the "logoUrl" field under the piece of data to the FileID of logoValencia.jpg
Similarly, change the value of the "logoUrl" field of another piece of data to the FileID of chef_logo.jpg

Image Descr

Set the product picture (take the wireless speaker as an example)
Click to enter the merchant side
Click "Sign in as store owner"
Select "Valencia supermarket chain"
Click on the "Store Management" tab
Click "Product Management"
Edit "Wireless Speaker"
Click delete on the product picture
Click "+"
Upload a picture of the small speaker in the "Pictures" folder

Image Descr

Due to the large number of commodities, it may be troublesome to operate one by one. You can also upload pictures to cloud storage in batches by writing code, get their FileIDs and assign them to the corresponding products in the database. But in comparison, uploading pictures manually may be more convenient

Finish
So far, except that the pictures of each product will report "rendering error", the whole program should be able to run normally. If this project is helpful to you, I hope to leave a star, thank you! !

![ninja](https://user-images.githubusercontent.com/72182017/222765111-57012d72-496f-4a40-bb2e-ae55f45f2c0a.jpg)

Or You can Sponsor This Project 


