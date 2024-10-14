# Wholesale with Tiered Prices Excel Template

**Effortlessly Import Your Shopify Products into Selldone with Advanced Tier Pricing**

This guide is designed to help you transform your Shopify export Excel file into the appropriate format for seamless
importing into Selldone. By aligning the Shopify export columns with Selldone's import requirements, you can easily
migrate your products and take advantage of Selldone's advanced tier pricing features.

## Features

- **Easy Migration**: Match Shopify's export file format with Selldone's import template.
- **Advanced Tier Pricing**: Utilize Selldone's tiered pricing based on ordered quantities.
- **Bulk Import**: Import products, categories, and images in bulk.

## How to Use This Template

1. **Export Your Products from Shopify**:
    - Log in to your Shopify admin panel.
    - Navigate to **Products** and click **Export**.
    - Choose to export **All products** in **CSV for Excel** format.

2. **Open the Exported File in Excel**:
    - Open the CSV file using Microsoft Excel or a compatible spreadsheet program.

3. **Map Shopify Columns to Selldone Columns**:
    - Use the column mapping table below to align your data.
    - Rename or add columns as necessary to match Selldone's requirements.

4. **Fill in Additional Fields**:
    - Add any missing Selldone-required columns that are not present in the Shopify export.
    - Input data for advanced tier pricing, limits, and other Selldone-specific features.

5. **Save and Import into Selldone**:
    - Save your Excel file.
    - Log in to your Selldone shop dashboard.
    - Navigate to **Products** and use the **Import** feature to upload your file.

## Column Mapping and Descriptions

The following table provides a detailed mapping between Shopify's export columns and Selldone's import columns, along
with descriptions and whether they are required.

| **Shopify Column**        | **Selldone Column**        | **Description**                                                                                              | **Required** |
|---------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------|--------------|
| **Published**             | **Status**                 | Product availability status. In Selldone, use **Open** for published products and **Close** for unpublished. | Yes          |
| **Variant SKU**           | **SKU**                    | Stock Keeping Unit identifier.                                                                               | Yes          |
| **Title**                 | **Title**                  | Product title.                                                                                               | Yes          |
| **Variant Inventory Qty** | **Quantity**               | Total product quantity available.                                                                            | Yes          |
| **Type**                  | **Type**                   | Product type. Use **PHYSICAL** for physical products.                                                        | Yes          |
| **Variant Price**         | **Price**                  | Base product price.                                                                                          | Yes          |
| **Currency Code**         | **Currency**               | Currency of the price (e.g., **USD**, **EUR**).                                                              | Yes          |
| **Body (HTML)**           | **Content Description**    | Product description.                                                                                         | Yes          |
| **Image Src**             | **Image**                  | Main product image URL.                                                                                      | Yes          |
| **Additional Images**     | **Images**                 | Additional product images URLs, separated by commas.                                                         | Optional     |
| *(Custom Field)*          | **Extra**                  | Extra product details in JSON format (e.g., dimensions).                                                     | Optional     |
| *(Custom Field)*          | **Lead Time**              | Product shipping lead time.                                                                                  | Optional     |
| *(Custom Field)*          | **Limit Min**              | Minimum order quantity limit per purchase.                                                                   | Optional     |
| *(Custom Field)*          | **Limit Max**              | Maximum order quantity limit per purchase.                                                                   | Optional     |
| *(Custom Field)*          | **Price 1** to **Price 6** | Tiered prices for different quantity ranges.                                                                 | Optional     |
| *(Custom Field)*          | **Qty 1** to **Qty 6**     | Quantity thresholds for tiered pricing.                                                                      | Optional     |
| **Product Category**      | **Category**               | Product category. Should match categories in Selldone or be created accordingly.                             | Yes          |
| *(Custom Field)*          | **Image Contain**          | Image contain flag (**TRUE** or **FALSE**).                                                                  | Optional     |

**Note**: Fields marked as *(Custom Field)* are not standard in Shopify exports and need to be added manually.

## Detailed Column Descriptions

- **Status**: Set to **Open** to publish the product in Selldone or **Close** to keep it unpublished.
- **SKU**: Unique identifier for inventory tracking.
- **Title**: Name of the product.
- **Quantity**: Number of units available for sale.
- **Type**: Set to **PHYSICAL** for tangible goods.
- **Price**: Base selling price of the product.
- **Currency**: Currency code matching the price (e.g., **USD**).
- **Content Description**: Detailed description, supports HTML formatting.
- **Image**: URL to the main image of the product.
- **Images**: Additional images, separated by commas.
- **Extra**: Use JSON format to include extra details like dimensions (`{"length":10,"width":5,"height":2}`).
- **Lead Time**: Time taken for the product to be delivered once shipped.
- **Limit Min** and **Limit Max**: Set minimum and maximum purchase quantities.
- **Price 1** to **Price 6** and **Qty 1** to **Qty 6**: Define tiered pricing based on quantity thresholds.
- **Category**: Assign the product to a category for better organization.
- **Image Contain**: Set to **TRUE** if the image should be contained within its container; **FALSE** otherwise.

## Setting Up Advanced Tier Pricing

Selldone allows you to offer tiered pricing to your customers based on the quantity they purchase. This is especially
useful for wholesalers.

### Example

| **Qty 1** | **Price 1** | **Qty 2** | **Price 2** | **Qty 3** | **Price 3** |
|-----------|-------------|-----------|-------------|-----------|-------------|
| 10        | 9.00        | 50        | 8.50        | 100       | 8.00        |

In this example:

- **Price 1**: Customers buying at least **10** units get each for **$9.00**.
- **Price 2**: Customers buying at least **50** units get each for **$8.50**.
- **Price 3**: Customers buying **100** or more units get each for **$8.00**.

### How to Add Tiered Pricing

1. **Add Columns**: In your Excel file, add columns for **Price 1** to **Price 6** and **Qty 1** to **Qty 6**.
2. **Input Data**: Enter the quantity thresholds and corresponding prices.
3. **Ensure Alignment**: Each **Price X** should have a corresponding **Qty X**.

## Transforming Your Shopify Export File

To match your Shopify export file to Selldone's import format:

- **Rename Columns**: Change column headers to match Selldone's expected column names.
- **Add Missing Columns**: Insert any additional columns required by Selldone that are not present in Shopify's export.
- **Populate Data**: Fill in the required information, ensuring all mandatory fields are completed.
- **Format Data Correctly**:
    - **JSON Fields**: Ensure JSON data in the **Extra** column is properly formatted.
    - **Boolean Fields**: Use **TRUE** or **FALSE** for fields like **Image Contain**.
    - **Numeric Fields**: Ensure prices and quantities are numerical values.

## Sample Data Row

| **Status** | **SKU**  | **Title**      | **Quantity** | **Type** | **Price** | **Currency** | **Content Description**  | **Image**                           | **Images**                                                                 | **Limit Min** | **Limit Max** | **Qty 1** | **Price 1** | **Qty 2** | **Price 2** | **Category** | **Image Contain** |
|------------|----------|----------------|--------------|----------|-----------|--------------|--------------------------|-------------------------------------|----------------------------------------------------------------------------|---------------|---------------|-----------|-------------|-----------|-------------|--------------|-------------------|
| Open       | PROD-001 | Sample Product | 500          | PHYSICAL | 10.00     | USD          | High-quality sample item | http://example.com/images/prod1.jpg | http://example.com/images/prod1a.jpg, http://example.com/images/prod1b.jpg | 1             | 1000          | 10        | 9.50        | 50        | 9.00        | Electronics  | TRUE              |

**Explanation**:

- **Status**: Product is published.
- **SKU**: Unique identifier.
- **Quantity**: 500 units in stock.
- **Limit Min**: Minimum order of 1 unit.
- **Limit Max**: Maximum order of 1000 units.
- **Tiered Pricing**: Discounts start at 10 units.

## Final Steps

1. **Validate Your Data**: Ensure all required fields are filled and data formats are correct.
2. **Save the File**: Save your Excel file in a format compatible with Selldone (e.g., `.xlsx`).
3. **Import into Selldone**:
    - Log in to your Selldone dashboard.
    - Navigate to **Products** and select **Import**.
    - Upload your Excel file.
4. **Review and Confirm**:
    - After importing, review the products in your Selldone store.
    - Check that all data, including tiered pricing, has been imported correctly.

## Benefits of Using Selldone's Advanced Tier Pricing

- **Increased Sales**: Encourage larger orders by offering discounts on bulk purchases.
- **Flexibility**: Easily adjust pricing tiers to match market demands.
- **Efficiency**: Streamline your wholesale operations with automated pricing adjustments.

---

By following this guide, you can seamlessly migrate your Shopify products into Selldone and take full advantage of
advanced tier pricing. This will enhance your wholesale capabilities and provide a better shopping experience for your
customers.

---

**About Selldone**

[Selldone](https://selldone.com) is an easy-to-use eCommerce platform that empowers merchants to create and manage their
online stores with ease. With a user-friendly interface and powerful features like advanced tier pricing, Selldone makes
online selling a breeze. [Get started today!](https://selldone.com)