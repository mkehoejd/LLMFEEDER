# LLM Feeder

This helps old wordpress sites get crawled by LLM's so their sites are compliant with the future of, "search".  This lightweight WordPress plugin exposes WooCommerce product data in structured JSON format via a REST API endpoint. It’s designed to support product discovery by Large Language Models (LLMs), AI-powered search tools, and external marketplaces.

---

## 🔍 What It Does

- Creates a REST API endpoint:  
  `/wp-json/llm-feed/v1/products/`

- Outputs WooCommerce product data including:
  - Product ID
  - Title
  - Description (plain text)
  - Price
  - SKU
  - Permalink
  - Schema.org-compatible metadata (brand, availability, type)

---

## 💡 Why It Matters

This plugin helps make your product catalog accessible to:
- AI search assistants (ChatGPT, Perplexity, Claude, etc.)
- LLM-based shopping agents
- SEO crawlers and structured data tools
- Google Merchant feeds (with future extensions)

The output is optimized for consumption by both machines and search APIs.

---

## 🛠 Installation

1. Upload the plugin to `/wp-content/plugins/llm-feeder/`
2. Activate it via WordPress Admin → Plugins
3. Visit:  
   `https://yourdomain.com/wp-json/llm-feed/v1/products/`  
   to verify the JSON output

---

## ✅ Requirements

- WordPress 5.0+
- WooCommerce 3.0+
- REST API enabled (default)

---

## 🧪 Example Output

```json
[
  {
    "id": 123,
    "title": "1950s Gibson Parlor Guitar",
    "description": "Warm, punchy tone with vintage patina...",
    "price": "2495.00",
    "sku": "GIB-1950-PRL",
    "url": "https://yourdomain.com/product/1950s-gibson-parlor/",
    "@type": "Product",
    "brand": "Greg Boyd Music",
    "availability": "https://schema.org/InStock",
    "currency": "USD"
  }
]
