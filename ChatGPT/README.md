
# ChatGPT Prompt To Convert Any Excel To Selldone Import Products Format File

Please attach your file in the chatGPT and past the following prompt to get the file converted to Selldone import format.

```text
I need assistance in modifying my product data to match the Selldone product import format for importing products into my Selldone shop.

What I Have:

I have product data with the following columns:

    Current Column Headers:
        Product Name
        Price
        Stock
        SKU
        Description
        Image URL
        [Include any additional columns you have]

Sample Data:
Product Name	Price	Stock	SKU	Description	Image URL
Blue Office Chair	$49.99	100	BOF-CHAIR	Comfortable chair...	http://example.com/image1.jpg
Red Office Chair	$59.99	50	ROF-CHAIR	Stylish red chair...	http://example.com/image2.jpg

What I Need:

    Change Column Headers:

        Please help me rename my existing column headers to match Selldone's required columns.

        The required and optional columns for Selldone are as follows:

        Required Columns:
            Title
            Type
            Price
            Currency
            Status
            Image

        Optional Columns:
            Product ID
            Variant ID
            Title En
            Commission
            Discount
            Discount Start Date
            Discount End Date
            Quantity
            SKU
            MPN
            GTIN
            GPC
            Condition
            Brand
            Warranty
            Spec
            Spec Order
            Pros
            Cons
            Outputs
            Inputs
            Content Title
            Content Body (Html)
            Content Description
            Content Image
            Content FAQ
            Content Structure Data
            Category
            Lead Time
            Extra
            Image Contain
            Return Warranty
            Original
            Slug
            Images
            V_Color
            V_Style
            V_Volume
            V_Weight
            V_Pack
            V_Type
            Limit Min
            Limit Max
            Qty 1 to Qty 10
            Price 1 to Price 10
            Price Label
            Unit
            Price Input
            Valuation ID

        Please map my current columns to the appropriate Selldone columns. If any required Selldone columns are missing in my data, please suggest default values or let me know so I can provide the necessary information.

    Modify Data Values:
        Adjust data values as needed to match Selldone's expected formats and structures.
            Price: Ensure it is a numeric value without currency symbols.
            Currency: Use currency codes like 'USD', 'EUR'.
            Status: Set to 'Open' or 'Close' (I want all products to be 'Open').
            Type: Use 'PHYSICAL' for physical products.
            Boolean Fields: Use 'TRUE' or 'FALSE'.
            Date Fields: Use the format 'YYYY-MM-DD' or 'YYYY-MM-DD HH:MM
            '.
            JSON Fields: Ensure fields like Spec, Pros, Cons contain valid JSON strings.
        For example, in my data, the Price column includes a dollar sign (e.g., '$49.99'). Please remove the dollar sign to make it a numeric value.

    Exclude Unnecessary Columns:

        Exclude the following columns from the final data, as they cannot be imported into Selldone:
            Visits
            Rate
            Rates Count
            For Available
            For Auction
            Sells

    (I don't have these columns, but mentioning just in case.)

    Provide Structure of Values:
        Ensure that each column contains data in the correct format and structure as required by Selldone.
        Modify the values if necessary to conform to Selldone's requirements.

Example Transformation:

Given my current data:
Product Name	Price	Stock	SKU	Description	Image URL
Blue Office Chair	$49.99	100	BOF-CHAIR	Comfortable chair...	http://example.com/image1.jpg

I need it transformed to match Selldone's format:
Title	Type	Price	Currency	Status	Quantity	SKU	Content Description	Image
Blue Office Chair	PHYSICAL	49.99	USD	Open	100	BOF-CHAIR	Comfortable chair...	http://example.com/image1.jpg

Details:

    Title: Mapped from Product Name.
    Type: Set to 'PHYSICAL'.
    Price: Removed the dollar sign to make it numeric.
    Currency: Set to 'USD'.
    Status: Set to 'Open'.
    Quantity: Mapped from Stock.
    SKU: Remains the same.
    Content Description: Mapped from Description.
    Image: Mapped from Image URL.

Additional Information:

    I want to include any additional optional fields if possible, such as Category, Brand, etc.
    For fields that I don't have data for, please let me know if default values are needed.

Instructions:

    Please help me by providing the transformed data in a table format, showing how my current data maps to the Selldone format.
    Include any necessary adjustments to data values or formats.
    Provide guidance on any missing required fields or values.
    Ensure that the final data is ready for import into Selldone.

Note:

    Since I cannot attach files, please work with the data provided in this message.
    If you need more information or clarification, please ask.

Thank you for your assistance!

Example of Expected Output:

You can present the transformed data like this:
Title	Type	Price	Currency	Status	Quantity	SKU	Content Description	Image
Blue Office Chair	PHYSICAL	49.99	USD	Open	100	BOF-CHAIR	Comfortable chair...	http://example.com/image1.jpg
Red Office Chair	PHYSICAL	59.99	USD	Open	50	ROF-CHAIR	Stylish red chair...	http://example.com/image2.jpg

By using this prompt, ChatGPT can help you map your existing data to Selldone's required format, rename columns, adjust data values, and prepare your data for import into Selldone.
Shortened Version of the Prompt (if needed):

Subject: Help me modify my product data to match Selldone's product import format

Message:

    Current Columns and Sample Data:
    Product Name	Price	Stock	SKU	Description	Image URL
    Blue Office Chair	$49.99	100	BOF-CHAIR	Comfortable chair...	http://example.com/image1.jpg

    Required Selldone Columns:
        Title
        Type
        Price
        Currency
        Status
        Image

    Tasks:
        Rename columns to match Selldone's format.
        Modify data values as needed (e.g., remove '$' from Price).
        Set default values for missing required fields (e.g., Type: 'PHYSICAL', Status: 'Open', Currency: 'USD').
        Exclude unsupported columns (e.g., Visits, Rate).

    Example of Transformed Data:
    Title	Type	Price	Currency	Status	Quantity	SKU	Content Description	Image
    Blue Office Chair	PHYSICAL	49.99	USD	Open	100	BOF-CHAIR	Comfortable chair...	http://example.com/image1.jpg

    Note: Please work with the data provided. If you need more information, please ask.

Thank you!
```