# Wholesale with Tiered Prices Excel Template

This Excel template is designed for Selldone shop merchants to easily import bulk products and categories with tiered
pricing based on the ordered quantity. The template also supports importing images for each product.

## Features

- Import bulk products with multiple pricing tiers
- Set minimum and maximum order limits per cart
- Import product images

## Columns

| Column              | Description                                                                                                 | Selldone |
|---------------------|-------------------------------------------------------------------------------------------------------------|----------|
| Publish             | Product publish status (1 for published, 0 for unpublished) [✂ Provided by the seller not used in selldone] | ❌        |
| Status              | Product availability status (Open or Close)                                                                 | ✅        |
| SKU                 | Stock keeping unit identifier                                                                               | ✅        |
| Title               | Product title                                                                                               | ✅        |
| Ctn L               | Carton length [✂ Provided by the seller not used in selldone]                                               | ❌        |
| Ctn W               | Carton width  [✂ Provided by the seller not used in selldone]                                               | ❌        |
| Ctn H               | Carton height [✂ Provided by the seller not used in selldone]                                               | ❌        |
| Ctn Qty             | Carton quantity [✂ Provided by the seller not used in selldone]                                             | ❌        |
| Quantity            | Total product quantity                                                                                      | ✅        |
| Ctn Weight          | Carton weight [✂ Provided by the seller not used in selldone]                                               | ❌        |
| Extra               | Extra product details (JSON format)                                                                         | ✅        |
| Production Time     | Product production lead time                                                                                | ✅        |
| Lead Time           | Product shipping lead time                                                                                  | ✅        |
| Type                | Product type (PHYSICAL)                                                                                     | ✅        |
| Currency            | Product currency (e.g. USD)                                                                                 | ✅        |
| Price               | Base product price                                                                                          | ✅        |
| Limit Min           | Minimum order quantity limit                                                                                | ✅        |
| Limit Max           | Maximum order quantity limit                                                                                | ✅        |
| Price 1-6           | Tiered prices for different quantity ranges                                                                 | ✅        |
| Qty 1-6             | Quantity ranges for tiered pricing                                                                          | ✅        |
| Category            | Product category                                                                                            | ✅        |
| Content Description | Product description                                                                                         | ✅        |
| Image               | Main product image URL                                                                                      | ✅        |
| Picture 2-10        | Additional product images URLs  [✂ Provided by the seller not used in selldone]                             | ❌        |
| Images              | Additional product images URLs (comma-separated)                                                            | ✅        |
| Image Contain       | Image contain flag (TRUE or FALSE)                                                                          | ✅        |


In this guide, we demonstrate how to effortlessly transform your existing Excel file into the appropriate format for seamless importing into Selldone.

---

[Selldone](https://selldone.com) is an easy-to-use eCommerce platform, empowering merchants to create and manage their
online stores. With a user-friendly interface and powerful features, Selldone makes online selling a
breeze. [Get started today!](https://selldone.com)
