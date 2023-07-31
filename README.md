
# Stripe Payment

The "Stripe Payment" project demonstrates the seamless integration of the Stripe payment functionality into a Flask web application. Stripe is a widely used online payment processing platform that enables businesses and individuals to securely accept online payments.

With Stripe, users can initiate a checkout session and make subscription payments for products and services. The application provides an intuitive "Checkout" button that redirects users to the Stripe checkout page, where they can enter their payment details securely.

Stripe supports various payment methods, including credit and debit cards, digital wallets, and bank transfers. It handles the complexities of payment processing and ensures that transactions are secure and compliant with industry standards.

The project provides basic templates (checkout.html, success.html, and cancel.html) that users can customize to match their application's design. The "Payment Successful" page (success.html) and "Payment Failed" page (cancel.html) provide users with clear confirmation of their payment status.

This project aims to serve as a starting point for developers looking to implement subscription-based payment systems with Stripe in their Flask applications. It also presents opportunities for future enhancements, such as user authentication, subscription plan management, and automated testing.


## Installation

**1.Clone the repository or download the source code-** https://github.com/abhisheksingh-17/Stripe-Payment.git

**2.Create and activate a virtual environment (optional, but recommended):**

```bash
  python3 -m venv venv

  source venv\Scripts\activate
```
**3.Install the required dependencies:**    
```bash
  pip install -r requirements.txt
```
**4.Set up your Stripe API key:**

Replace "my api key" in the app.py file with your actual Stripe API key. You can obtain the API key from your Stripe dashboard-https://dashboard.stripe.com/test/apikeys
## Deployment

**1.Run the Flask development server:**
```bash
  python app.py
```
**2.Access the application in your web browser:**

Open http://localhost:5000/checkout.html in your web browser to see the home page.

**3.Checkout and make a subscription payment:**

Click the "Checkout" button on the home page to initiate a checkout session. You will be redirected to the Stripe checkout page to enter payment details.

**4.Success and Cancel Pages:**

After completing the payment, you will be redirected to the success page (success.html) if the payment is successful or the cancel page (cancel.html) if the payment is canceled.

## Technologies Used

The "Stripe Payment Integration with Flask" project utilizes the following technologies:

**1.Flask:** Flask is a lightweight web framework for Python, used to build the backend server and handle HTTP requests.

**2.Stripe API:** The Stripe API provides the payment processing functionality, enabling secure and seamless online payments.

**3.HTML & CSS:** The frontend of the application is built using HTML for the structure and CSS for styling.

**4.Font Awesome:** Font Awesome icons are used to enhance the visual elements of the application.

**5.Python:** The project's backend logic is written in Python, handling the Stripe integration and other server-side operations.

**6.Virtual Environment:** A virtual environment is used to manage project dependencies and ensure isolation from other Python projects.

**7.Git:** Git is used for version control and to track changes to the project's codebase.

**8.GitHub:** GitHub serves as the code repository and collaboration platform for the project.
## Code Explanation

**1.app.py**

The app.py file is the main Flask application file that handles the web application's backend logic and routes.

The Flask app is initialized using Flask(__name__), and the static and template folders are specified for the application.

The Stripe API key is set using stripe.api_key = "my api key". Replace "my api key" with your actual Stripe API key obtained from the Stripe dashboard.

The /create-checkout-session route is defined to handle the creation of a new Stripe checkout session when the user clicks the "Checkout" button.

In the create_checkout_session() function, a new Stripe checkout session is created using the stripe.checkout.Session.create() method. The line_items parameter specifies the product price and quantity for the checkout session. The mode is set to "subscription" to enable subscription-based payments.

Upon successful creation of the checkout session, the user is redirected to the Stripe checkout page to complete the payment process.

**2.Templates (checkout.html, success.html, cancel.html)**

The provided templates are simple HTML files that define the frontend layout and content for the application.

**checkout.html:** This template contains a form with a single "Checkout" button. When users click the button, it initiates the /create-checkout-session POST request to start the Stripe checkout process.

**success.html:** This template displays a "Payment Successful" message and informs the user that their subscription has been successfully established. It uses Font Awesome icons for visual elements.

**cancel.html:** This template displays a "Payment Failed" message and encourages users to revisit the website to complete their purchase if their payment was canceled. It also utilizes Font Awesome icons for visual elements.

**3.Styling (CSS)**

The CSS styles for the templates are embedded within the <style> tags in each template file.

The CSS defines the layout and appearance of the application's elements, including background images, button styles, font sizes, and positioning.

The templates use Font Awesome icons via the link to the Font Awesome kit (https://kit.fontawesome.com/92d70a2fd8.js)
## Screenshots


**Home Page-**
![](https://github.com/abhisheksingh-17/Stripe-Payment/blob/main/Results/1.png?raw=true)


**Checkout Page-**
![](https://github.com/abhisheksingh-17/Stripe-Payment/blob/main/Results/2.png?raw=true)

![](https://github.com/abhisheksingh-17/Stripe-Payment/blob/main/Results/4.png?raw=true)


**Payment Successful Page-**
![](https://github.com/abhisheksingh-17/Stripe-Payment/blob/main/Results/6.png?raw=true)


**Payment Failed Page-**
![](https://github.com/abhisheksingh-17/Stripe-Payment/blob/main/Results/7.png?raw=true)


**Payment Dashboard-**
![](https://github.com/abhisheksingh-17/Stripe-Payment/blob/main/Results/8.png?raw=true)
## Acknowledgements
I would like to express my sincere gratitude to the following individuals and resources for their valuable contributions and support during the development of this project:

**1.Stripe:** I am thankful to Stripe for providing an excellent payment processing platform and comprehensive documentation that made integrating payments into this project straightforward.  
https://stripe.com/docs/api

**2.Font Awesome:** The provided templates utilize Font Awesome icons, adding visual elements to the application and enhancing the user experience.
https://fontawesome.com

**3.Open Source Community:** I extend my thanks to the open-source community for their contributions to the Flask framework and related libraries, making this project possible.
## Future Scope
The "Stripe Payment Integration with Flask" project provides a solid foundation for a subscription-based payment system. Here are some potential areas for future enhancement and expansion:

**1.User Authentication-**
Currently, the application allows any user to initiate a checkout session. Implementing user authentication and registration will enable personalized subscriptions and better user management.

**2.Subscription Plan Management-**
Introduce an admin dashboard to manage subscription plans, allowing administrators to create, update, and remove subscription options.

**3.Payment History and Invoices-**
Include a payment history feature that allows users to view past payments and access/download invoices for their records.

**4.Webhooks and Event Handling-**
Implement Stripe webhooks to handle events like payment failures, subscription cancellations, and other crucial events to provide users with timely notifications.

**5.Secure Deployment-**
In a production environment, ensure secure deployment with HTTPS, protect sensitive data, and follow best practices for securing web applications.

**6.User Account Management-**
Create user profiles where users can manage their account details, update payment methods, and view their subscription status.

**7.Subscription Upgrade/Downgrade-**
Allow users to upgrade or downgrade their subscription plans easily from within their account.

**8.Support for Multiple Payment Gateways-**
In addition to Stripe, consider adding support for other payment gateways to provide users with more payment options.

**9.Internationalization and Localization-**
Extend support for multiple languages and currencies to make the application more accessible to a global audience.

**10.Automated Testing-**
Implement automated testing to ensure the application's robustness and prevent regressions.