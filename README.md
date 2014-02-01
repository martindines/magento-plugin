©2011-2014 BITPAY, INC.

Permission is hereby granted to any person obtaining a copy of this software
and associated documentation for use and/or modification in association with
the bitpay.com service.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

Bitcoin payment module using the bitpay.com service.

Installation
------------
Copy these files into your Magento directory.

Configuration
-------------
NOTE: SSL is required for use of the BitPay plugin for Magento

1. Create an API key at bitpay.com by clicking My Account > API Access Keys > Add New API Key.
2. In Admin panel under "System > Configuration > Sales > Payment Methods > Bitcoins":
<ol type="a">
 <li>Verify that the module is enabled. 
 <li>Enter your API key.  
 <li>Select a transaction speed.  The **high** speed will send a confirmation as soon as a transaction is received in the bitcoin network (usually a few seconds).  A **medium** speed setting will typically take 10 minutes.  The **low** speed setting usually takes around 1 hour.  See the bitpay.com merchant documentation for a full description of the transaction speed settings. 
 <li>Verify that the currencies option includes your store's currencies.  If it doesn't, check bitpay.com to see if they support your desired currency.  If so, you may simply add the currency to the list using this setting.  If not, you will not be able to use that currency. 
 <li>(optional) Adjust the "Fullscreen Invoice" setting.  "No" means that payment instructions are embedded in the checkout page.  "Yes" means that the buyer will be redirected to bitpay.com to pay their order. 
</ol>	

Usage
-----
When a shopper chooses the Bitcoin payment method, they will be presented with an order summary as the next step (prices are shown in whatever currency they've selected for shopping).  If the fullscreen option is disabled, they can pay for their order using the address shown on the screen.  Otherwise they will place their order and be redirected to bitpay.com to pay.

The order status in the admin panel will be "Processing" if payment has been confirmed. 

Note: This extension does not provide a means of automatically pulling a current BTC exchange rate for presenting BTC prices to shoppers.

Change Log
----------
v1.1.0
- Now gives the option to show an iframe on the checkout page instead of redirecting to bitpay.com.

v1.0.0
- Now supports API keys instead of SSL files.  Tested against 1.7.0.2.

v0.1.0
- Initial version, tested against Magento 1.6.0.0
