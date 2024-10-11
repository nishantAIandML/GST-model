Welcome to the **GST Prediction Model** project! This project is designed to calculate the Goods and Services Tax (GST) on various food items based on the latest 2023 GST rates in India. Using the Groq API to handle the language model responses, the program processes the item descriptions to return the correct GST rates, HSN codes, and the total cost with GST.

**Technologies Used**

The project leverages a variety of technologies and libraries to accomplish its goal:

1. **Python**: The base language for the project.


2. **GroqAPI**: Used to integrate a language model for processing and retrieving GST rates and HSN codes based on product descriptions.


3. **Pandas**: For data manipulation and DataFrame operations.


4. **Custom Functions**: To clean, transform, and process the results from the Groq API.

**Features and Parameters**

1. **GST Rate Calculation:**

Based on the product description, the model uses the Groq API to fetch the GST rate applicable for the item.

The code then calculates the price with GST based on the entered price without GST.


2. **HSN Code Lookup:**

The model can also generate HSN codes for the products based on their description using the Groq API.



3. **Input Parameters:**

_Description of Food:_ Enter the description of the food item for which you want to calculate GST.

_Quantity:_ Number of units (kilograms/litres) of the product.

_Rate without GST:_ Price of the product per kilogram or litre, excluding GST.


4. **DataFrame Output:**

The result is shown as a pandas DataFrame that includes:

_Description of Food_

HSN Code (if available)

Quantity

Rate without GST

Rate with GST

GST Percentage

Total cost without GST

Total cost with GST


**API Details**

_Groq API_

We use the Groq API to get GST rates and HSN codes based on product descriptions. To use the API, you need to set your GROQ_API_KEY:

from groq import Groq
client = Groq(api_key="YOUR_GROQ_API_KEY")

_Chat Completions_

The Groq API chat completion is used in the get_gst() function to query the GST rate based on food descriptions. The model processes the user request and returns the appropriate response in percentage format.

_Example usage:_

chat_completion = client.chat.completions.create(
    messages=[{"role": "user", "content": "Juice. Give GST rate"}],
    model="llama3-8b-8192",
)


**Future Enhancements**

We will add more product categories and descriptions for improved accuracy.

We will expand the functionality to handle more complex inputs and different tax categories beyond food items.

Also we can integrate currency conversions or input rates in multiple units. 


**Developed By-**
Nishant
Rahul Kumar
Sanskar Usretay

