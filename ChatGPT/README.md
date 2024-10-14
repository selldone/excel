
# ChatGPT Prompt To Convert Any Excel To Selldone Import Products Format File

Please attach your file in the chatGPT and past the following prompt to get the file converted to Selldone import format.

```text
I need assistance in modifying my product data to match the Selldone product import format for importing products into my Selldone shop.

What I Have:

I have product data with the following columns:


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

    Exclude Unnecessary Columns!


    Provide Structure of Values:
        Ensure that each column contains data in the correct format and structure as required by Selldone.
        Modify the values if necessary to conform to Selldone's requirements.


    Strucure of standard selldone Excel file for products:
    
| **Column Name**            | **Description**                                                                                                                                               | **Required** | **Relations/Notes**                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------|
| **Product ID**             | The unique identifier of the product in Selldone.                                                                                                             | Optional     | Used to update an existing product. If empty, a new product will be created.                                     |
| **Variant ID**             | The unique identifier of the product variant.                                                                                                                 | Optional     | Used to update an existing variant. Applicable when **Type** is 'VARIANT'.                                       |
| **Title**                  | The name of the product.                                                                                                                                      | **Required** |                                                                                                                  |
| **Title En**               | The English name of the product.                                                                                                                              | Optional     | The standard name or technical name of the product in English.                                                   |
| **Type**                   | The type of the product. It can be `PHYSICAL`, `VIRTUAL`, `FILE`, `SERVICE`, `SUBSCRIPTION`. Use 'VARIANT' for variants; otherwise, use a valid product type. | **Required** | 'VARIANT' indicates the row is a variant of the last product listed.                                             |
| **Price**                  | The price of the product as a floating-point number, e.g., `10.99`.                                                                                           | **Required** | Customer Price = `Price` + `Commission` - `Discount`                                                             |
| **Currency**               | The currency code of the price, e.g., 'USD', 'EUR', 'GBP'.                                                                                                    | **Required** |                                                                                                                  |
| **Commission**             | The commission amount or percentage for the product.                                                                                                          | Optional     | Defaults to `0` if not provided.                                                                                 |
| **Discount**               | The discount amount or percentage applied to the product.                                                                                                     | Optional     | Defaults to `0` if not provided.                                                                                 |
| **Discount Start Date**    | The start date of the discount period.                                                                                                                        | Optional     | Format: `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`.                                                                   |
| **Discount End Date**      | The end date of the discount period.                                                                                                                          | Optional     | Format: `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`.                                                                   |
| **Status**                 | The availability status of the product, e.g., 'Open', 'Close'.                                                                                                | **Required** | 'Open' means available for sale; 'Close' means not available.                                                    |
| **Quantity**               | The available stock quantity.                                                                                                                                 | Optional     | Defaults to `0` if not provided.                                                                                 |
| **SKU**                    | The Stock Keeping Unit identifier. A unique code used to track inventory.                                                                                     | Optional     |                                                                                                                  |
| **MPN**                    | The Manufacturer Part Number.                                                                                                                                 | Optional     |                                                                                                                  |
| **GTIN**                   | The Global Trade Item Number.                                                                                                                                 | Optional     |                                                                                                                  |
| **GPC**                    | The Global Product Classification code.                                                                                                                       | Optional     |                                                                                                                  |
| **Condition**              | The condition of the product, e.g., 'New', 'Used', 'Refurbished'.                                                                                             | Optional     |                                                                                                                  |
| **Brand**                  | The brand or manufacturer of the product.                                                                                                                     | Optional     |                                                                                                                  |
| **Warranty**               | Warranty information, e.g., '1 Year Manufacturer Warranty'.                                                                                                   | Optional     |                                                                                                                  |
| **Spec**                   | Specifications of the product in JSON format.                                                                                                                 | Optional     | Must be valid JSON (e.g., `{"Color":"Red","Size":"M"}`).                                                         |
| **Spec Order**             | The display order of specifications in a JSON array.                                                                                                          | Optional     | Must be a valid array of `Spec` keys (e.g., `["Color","Size"]`).                                                 |
| **Pros**                   | Advantages of the product in JSON format.                                                                                                                     | Optional     | Must be a valid JSON array (e.g., `["Lightweight","Durable"]`).                                                  |
| **Cons**                   | Disadvantages of the product in JSON format.                                                                                                                  | Optional     | Must be a valid JSON array (e.g., `["Limited color options"]`).                                                  |
| **Image**                  | The main image URL of the product.                                                                                                                            | **Required** |                                                                                                                  |
| **Outputs**                | Output specifications in JSON format.                                                                                                                         | Optional     | Must be valid JSON.                                                                                              |
| **Inputs**                 | Input specifications in JSON format.                                                                                                                          | Optional     | Must be valid JSON.                                                                                              |
| **Content Title**          | Title of the product description content.                                                                                                                     | Optional     |                                                                                                                  |
| **Content Body (Html)**    | HTML content describing the product in detail.                                                                                                                | Optional     |                                                                                                                  |
| **Content Description**    | A brief description of the product content.                                                                                                                   | Optional     |                                                                                                                  |
| **Content Image**          | URL of an image used in the content.                                                                                                                          | Optional     |                                                                                                                  |
| **Content FAQ**            | Frequently Asked Questions in JSON format.                                                                                                                    | Optional     | Must be a valid JSON array.                                                                                      |
| **Content Structure Data** | Structured data for SEO in JSON-LD format.                                                                                                                    | Optional     | Must be valid JSON-LD.                                                                                           |
| **Category**               | The product category or categories.                                                                                                                           | Optional     | Should match existing categories in your Selldone account; otherwise, it will create the category automatically. |
| **Lead Time**              | The number of days before the product is shipped (production or handling time).                                                                               | Optional     | Defaults to `-1` if not provided. `-1` indicates no lead time.                                                   |
| **Extra**                  | Additional product details in JSON format, such as dimensions or weight.                                                                                      | Optional     | Must be valid JSON (e.g., `{"weight":50,"width":100,"length":200,"height":40}`).                                 |
| **Image Contain**          | Indicates if the image should be contained within its container.                                                                                              | Optional     | Accepts `TRUE` or `FALSE`. Defaults to `FALSE`.                                                                  |
| **Return Warranty**        | The return warranty period in days.                                                                                                                           | Optional     | Defaults to `0` if not provided.                                                                                 |
| **Original**               | Indicates if the product is original or a replica.                                                                                                            | Optional     | Accepts `TRUE` or `FALSE`. Defaults to `TRUE`.                                                                   |
| **Slug**                   | The URL-friendly version of the product name.                                                                                                                 | Optional     | If empty, it will be auto-generated from the **Title**.                                                          |
| **Images**                 | Additional image URLs for the product, separated by commas.                                                                                                   | Optional     |                                                                                                                  |
| **V_Color**                | Variant attribute: color.                                                                                                                                     | Optional     | Applicable when **Type** is 'VARIANT'.                                                                           |
| **V_Style**                | Variant attribute: style.                                                                                                                                     | Optional     | Applicable when **Type** is 'VARIANT'.                                                                           |
| **V_Volume**               | Variant attribute: volume.                                                                                                                                    | Optional     | Applicable when **Type** is 'VARIANT'.                                                                           |
| **V_Weight**               | Variant attribute: weight.                                                                                                                                    | Optional     | Applicable when **Type** is 'VARIANT'.                                                                           |
| **V_Pack**                 | Variant attribute: pack size or packaging.                                                                                                                    | Optional     | Applicable when **Type** is 'VARIANT'.                                                                           |
| **V_Type**                 | Variant attribute: type or model.                                                                                                                             | Optional     | Applicable when **Type** is 'VARIANT'.                                                                           |
| **Limit Min**              | The minimum quantity allowed per order.                                                                                                                       | Optional     | Defaults to `0` (no minimum limit).                                                                              |
| **Limit Max**              | The maximum quantity allowed per order.                                                                                                                       | Optional     | Defaults to `0` (no maximum limit). Must be greater than or equal to **Limit Min** if provided.                  |
| **Qty 1**                  | Minimum quantity for tiered pricing level 1.                                                                                                                  | Optional     | Used in conjunction with **Price 1** for bulk pricing.                                                           |
| **Price 1**                | Price for tiered pricing level 1.                                                                                                                             | Optional     |                                                                                                                  |
| **Qty 2**                  | Minimum quantity for tiered pricing level 2.                                                                                                                  | Optional     |                                                                                                                  |
| **Price 2**                | Price for tiered pricing level 2.                                                                                                                             | Optional     |                                                                                                                  |
| **Qty 3**                  | Minimum quantity for tiered pricing level 3.                                                                                                                  | Optional     |                                                                                                                  |
| **Price 3**                | Price for tiered pricing level 3.                                                                                                                             | Optional     |                                                                                                                  |
| **Qty 4**                  | Minimum quantity for tiered pricing level 4.                                                                                                                  | Optional     |                                                                                                                  |
| **Price 4**                | Price for tiered pricing level 4.                                                                                                                             | Optional     |                                                                                                                  |
| **Qty 5**                  | Minimum quantity for tiered pricing level 5.                                                                                                                  | Optional     |                                                                                                                  |
| **Price 5**                | Price for tiered pricing level 5.                                                                                                                             | Optional     |                                                                                                                  |
| **Qty 6**                  | Minimum quantity for tiered pricing level 6.                                                                                                                  | Optional     |                                                                                                                  |
| **Price 6**                | Price for tiered pricing level 6.                                                                                                                             | Optional     |                                                                                                                  |
| **Qty 7**                  | Minimum quantity for tiered pricing level 7.                                                                                                                  | Optional     |                                                                                                                  |
| **Price 7**                | Price for tiered pricing level 7.                                                                                                                             | Optional     |                                                                                                                  |
| **Qty 8**                  | Minimum quantity for tiered pricing level 8.                                                                                                                  | Optional     |                                                                                                                  |
| **Price 8**                | Price for tiered pricing level 8.                                                                                                                             | Optional     |                                                                                                                  |
| **Qty 9**                  | Minimum quantity for tiered pricing level 9.                                                                                                                  | Optional     |                                                                                                                  |
| **Price 9**                | Price for tiered pricing level 9.                                                                                                                             | Optional     |                                                                                                                  |
| **Qty 10**                 | Minimum quantity for tiered pricing level 10.                                                                                                                 | Optional     |                                                                                                                  |
| **Price 10**               | Price for tiered pricing level 10.                                                                                                                            | Optional     |                                                                                                                  |
| **Price Label**            | A label or description for the price, e.g., 'per unit', 'per kg'.                                                                                             | Optional     |                                                                                                                  |
| **Unit**                   | The unit of measurement for the product, e.g., 'kg', 'liters', 'pcs'.                                                                                         | Optional     |                                                                                                                  |
| **Price Input**            | Indicates the type of price input, e.g., 'DEFAULT', 'CUSTOM'.                                                                                                 | Optional     | Use predefined constants or values accepted by Selldone.                                                         |
| **Valuation ID**           | The ID of the valuation method associated with the product.                                                                                                   | Optional     | Must correspond to a valid valuation ID in your Selldone account.                                                |


Notes and Guidelines
    First Row: Represents a product with detailed information.
    Second Row: Represents a variant of the product above.
    Fields like Spec, Spec Order, Pros, Cons, Extra, and Content Body (Html) contain JSON or HTML data. Ensure that these are properly formatted in your Excel file.
    The Images field contains multiple image URLs separated by commas.
    Boolean Fields like Image Contain and Original should be either TRUE or FALSE.
    Date Fields should be in the format YYYY-MM-DD HH:MM:SS.
    JSON Fields: Columns like Spec, Pros, Cons, Outputs, Inputs, Content FAQ, and Content Structure Data must contain valid JSON strings.
    Date Formats: Use the YYYY-MM-DD format for all date fields to ensure proper parsing.
    Boolean Fields: For fields like Image Contain and Original, use true or false.
    Numeric Fields: Ensure numeric fields like Price, Commission, Discount, Quantity, Return Warranty, Limit Min, and Limit Max contain valid numbers.
    Variant Rows: When Type is 'VARIANT', the row represents a variant of the last product defined in the spreadsheet. All variant attributes (V_Color, V_Style, etc.) are applicable in this case.
    Tiered Pricing: To offer bulk pricing, use Qty X and Price X columns. For example, if Qty 1 is 10 and Price 1 is 9.99, customers buying 10 or more units get the product at $9.99 each.
    Images: Multiple image URLs in the Images column should be separated by commas without spaces.
    Categories and Brands: Ensure that the values provided for Category and Brand match exactly with those defined in your Selldone account to prevent mismatches.
    Updating Products: If you provide a Product ID (and Variant ID for variants), the system will attempt to update the existing product or variant. If these are left empty, new entries will be created.
    Limits: If Limit Max is provided, it must be greater than Limit Min. If Limit Max is 0, it signifies no maximum limit.


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