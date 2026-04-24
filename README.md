# flippaslippa.foo — WordPress + WooCommerce Online Store

## Project Overview

**flippaslippa.foo** is an educational e-commerce project built with **WordPress** and **WooCommerce**.

The project represents a small online store that sells **furry slippers**.

The main goal of this project was to deploy and configure a functional WooCommerce online store with a custom domain, HTTPS, Cloudflare protection, transactional email delivery, and automatic PDF invoice generation.

The project demonstrates a complete basic e-commerce setup, including server infrastructure, WordPress configuration, WooCommerce product management, domain connection, SSL configuration, Cloudflare caching, email setup, and invoice automation.

## Technology Stack

The project uses the following technologies and services:

- WordPress
- WooCommerce
- Ubuntu Server 24.04 version
- DigitalOcean Droplet
- Cloudflare DNS/CDN
- Caddy web server
- WP Mail SMTP
- PDF Invoices & Packing Slips for WooCommerce
- WP-CLI
- name.com domain registrar

---

# Step 1. Infrastructure

## DigitalOcean Droplet Setup

The website was deployed on a **DigitalOcean Droplet**.

The Droplet was created using a pre-installed WordPress template. This simplified the initial deployment process because WordPress was already installed on the server.

## Server Configuration

| Parameter | Value |
|---|---|
| Provider | DigitalOcean |
| Server type | Droplet |
| Region | Frankfurt |
| Plan | Basic |
| RAM | 1 GB |
| CPU | 1 vCPU |
| Server IP | `207.154.228.100` |
| Operating system | Ubuntu |
| Template | WordPress template installed on the Droplet |

The selected configuration is suitable for a small educational WooCommerce project with a limited number of products and low expected traffic.

<img width="766" height="466" alt="image" src="https://github.com/user-attachments/assets/ed3a7954-924a-406f-95f3-9a997bcb5417" />


# Step 2. Server Access and Initial WordPress Setup

## Server Access via SSH

The server was accessed through SSH using the root user.

The SSH connection command:

```bash
ssh root@207.154.228.100
```

After connecting to the server, the WordPress installation and web server configuration were checked.

## Initial WordPress Setup

The WordPress website was configured through the web interface.

The initial WordPress 6.9.2 setup included the following steps:

2. Selecting the website language.
3. Creating an administrator account.
4. Setting the website title.
5. Logging in to the WordPress admin dashboard.

The WordPress admin dashboard is available at:

```text
https://flippaslippa.foo/wp-admin
```

WordPress was used as the main content management system for creating pages, managing content, configuring plugins, and managing the WooCommerce store.

<img width="948" height="499" alt="image" src="https://github.com/user-attachments/assets/11d58e2b-a182-4d1e-9a2d-3ac863ba4de1" />


---

# Step 3. WooCommerce Installation and Product Catalog

## WooCommerce Setup

WooCommerce was used to add e-commerce functionality to the WordPress website.

WooCommerce allows the website to manage products, prices, product descriptions, product images, cart functionality, checkout functionality, order management, and customer notifications.

The WooCommerce setup included:

1. Store details configuration.
2. Country and currency configuration.
3. Product type selection.
4. Basic shipping configuration.
5. Basic payment configuration.
6. Product catalog creation.

## Product Catalog

The store catalog contains **6 furry slipper products**.

Each product includes:

- product name;
- product description;
- product images;
- product price;
- product tags.

The products are simple WooCommerce products. They are used to demonstrate the basic product management functionality of WooCommerce.

Product tags were added to improve product organization and make the catalog easier to manage.

<img width="655" height="496" alt="image" src="https://github.com/user-attachments/assets/07220024-8a4f-414f-a463-4796d0e10f7d" />

<img width="946" height="500" alt="image" src="https://github.com/user-attachments/assets/38a425c4-9ead-49a6-993a-2f36c6020c88" />


---

# Step 4. Website Design and Content

## Website Structure

The website was designed as a small online store with four main pages:

- **Home** — main landing page;
- **About** — information about the store;
- **Contacts** — contact information;
- **Shop** — WooCommerce product catalog.

These pages provide the basic structure required for a small e-commerce website.

## Home Page

The **Home** page was configured as the main page of the website.

It includes:

- store introduction;
- visual content;
- call-to-action buttons;
- navigation to the shop;
- basic information about the store.
- review section

The Home page also includes a product block, allowing users to quickly access available furry slippers directly from the main page.

<img width="943" height="477" alt="image" src="https://github.com/user-attachments/assets/f68ee6e7-2614-4d30-9397-198e14ef26e0" />


## Shop Page

The **Shop** page displays the WooCommerce product catalog.

The catalog contains 6 furry slipper products. Each product card includes product information such as image, title, price, and tags or categories.

The Shop page allows users to browse available products and open individual product pages.


## About Page

The **About** page explains the idea of the store and describes the business concept.

The store focuses on selling comfortable, soft, and visually attractive furry slippers at an accessible price.

This page helps visitors understand the purpose of the store and the type of products it offers.


## Contacts Page

The **Contacts** page contains customer contact information.

It may include:

- email address;
- contact form;
- business location;
- customer support information.

The Contacts page allows customers to contact the store if they have questions about products, orders, or delivery.


---

# Step 5. Email Configuration

## WP Mail SMTP

For reliable email delivery, the website uses the **WP Mail SMTP** plugin.

The plugin was installed and configured to improve the delivery of WordPress and WooCommerce transactional emails.

Transactional emails include:

- order confirmation emails;
- order status update emails;
- admin notifications;
- customer notifications.

Using SMTP is important because the default WordPress email function may be unreliable on VPS hosting. Without SMTP configuration, emails can fail to send or may be marked as spam by email providers.

WP Mail SMTP ensures that WooCommerce emails are sent through a proper mail service instead of relying only on the default PHP mail function.

<img width="947" height="484" alt="image" src="https://github.com/user-attachments/assets/4317f3a6-178d-4ffd-b86a-8edd4e047198" />

<img width="923" height="408" alt="image" src="https://github.com/user-attachments/assets/e028b570-47e6-4aa3-a2c3-8dfbad21998e" />


---

# Step 6. PDF Invoice Automation

## PDF Invoices & Packing Slips for WooCommerce

For automatic invoice generation, the following plugin was used:

```text
PDF Invoices & Packing Slips for WooCommerce
```

This plugin generates PDF invoices for WooCommerce orders.

The plugin was configured to generate and attach PDF invoices to WooCommerce order emails.

The PDF invoice contains the required order information:

- Order ID;
- order date;
- purchased products;
- product quantities;
- total amount;
- customer details;
- store details.

The invoice can be attached automatically to WooCommerce emails for order statuses such as:

- Processing order;
- Order on hold.

This improves the order confirmation process and provides customers with a formal document confirming their purchase.

<img width="943" height="500" alt="image" src="https://github.com/user-attachments/assets/08ceebd3-6e33-4b14-b674-d27bdaf785ca" />


<img width="921" height="497" alt="image" src="https://github.com/user-attachments/assets/14843ad1-651a-4d31-a653-563a64cac818" />


# Step 7. Domain Registration and Cloudflare Configuration

## Domain Registration

The domain used for the project is:

```text
flippaslippa.foo
```

The domain was originally purchased through **name.com**.

After the domain purchase, it was connected to Cloudflare for DNS management, caching, CDN functionality, and additional website protection.

## Connecting the Domain to Cloudflare

To connect the domain to Cloudflare, the domain was added to the Cloudflare dashboard.

After that, Cloudflare provided new nameservers. These nameservers were set at name.com, replacing the original nameservers.

After the nameserver update, DNS management was moved from name.com to Cloudflare.

Cloudflare is used for:

- DNS management;
- CDN caching;
- static asset caching;
- HTTPS support;
- basic website protection.

<img width="941" height="507" alt="image" src="https://github.com/user-attachments/assets/a7024e9f-8ff0-414a-abf1-d4046098bd3c" />


<img width="953" height="502" alt="image" src="https://github.com/user-attachments/assets/0cafc68b-5e36-42b4-bd26-fda631d9f12b" />


## Cloudflare DNS Records

In Cloudflare, an A record was created to point the domain to the DigitalOcean server.

| Type | Name | Content |
|---|---|---|
| A | `@` | `207.154.228.100` |

A `www` record can also be configured:

| Type | Name | Content |
|---|---|---|
| CNAME | `www` | `flippaslippa.foo` |

The A record connects the root domain to the DigitalOcean Droplet.

<img width="746" height="503" alt="image" src="https://github.com/user-attachments/assets/0c9e14ae-34f9-4193-8f9e-8f3bfe8d73e4" />


---

# Step 8. Cloudflare Caching Verification

## Verifying That Traffic Goes Through Cloudflare

Cloudflare usage can be verified through browser Developer Tools.

To check this:

1. Open the website in a browser.
2. Press `F12` to open Developer Tools.
3. Go to the **Network** tab.
4. Reload the page.
5. Open image, CSS, or JavaScript requests.
6. Check the response headers and caching information.

Static assets such as images, CSS files, and JavaScript files can be cached by Cloudflare. This proves that website traffic and static resources are passing through Cloudflare.

In the Network tab, cached assets may show headers related to Cloudflare, such as:

```text
cf-cache-status
server: cloudflare
cf-ray
```

This confirms that Cloudflare is handling requests for the website.

<img width="419" height="195" alt="image" src="https://github.com/user-attachments/assets/ec2797b3-a52a-4618-9920-378c7b316cb8" />


---

# Step 9. HTTPS Configuration with Caddy

## HTTPS Setup

HTTPS was configured on the server using **Caddy**.

Caddy automatically manages HTTPS certificates and simplifies SSL configuration. This allows the website to be served securely through HTTPS.

The final website URL is:

```text
https://flippaslippa.foo
```

Caddy was responsible for serving the WordPress website securely and managing the HTTPS certificate.

## Cloudflare SSL Mode

Cloudflare was also configured to work with the HTTPS-enabled origin server.

Recommended Cloudflare SSL setting:

```text
SSL/TLS mode: Full
```

This means that:

- visitors connect to Cloudflare using HTTPS;
- Cloudflare connects to the origin server using HTTPS;
- the website is served securely.

<img width="760" height="488" alt="image" src="https://github.com/user-attachments/assets/3c84068e-a600-4204-8c00-b39a0b70a7ab" />


---

# Step 10. WordPress Configuration Behind Cloudflare

## HTTPS Detection Behind Cloudflare

Because the website works behind Cloudflare, WordPress must correctly detect HTTPS requests.

Without this configuration, WordPress may incorrectly think that requests are coming through HTTP, even when visitors access the website through HTTPS.

This can cause issues such as:

- mixed content warnings;
- incorrect redirects;
- redirect loops;
- WooCommerce checkout issues;
- incorrect HTTPS detection inside WordPress.

To fix this, the following code was added to the `wp-config.php` file:

```php
// Cloudflare HTTPS fix
if (
    isset($_SERVER['HTTP_CF_VISITOR']) &&
    strpos($_SERVER['HTTP_CF_VISITOR'], 'https') !== false
) {
    $_SERVER['HTTPS'] = 'on';
}

if (
    isset($_SERVER['HTTP_X_FORWARDED_PROTO']) &&
    $_SERVER['HTTP_X_FORWARDED_PROTO'] === 'https'
) {
    $_SERVER['HTTPS'] = 'on';
}
```

This code should be placed above the following line:

```php
/* That's all, stop editing! Happy publishing. */
```

The purpose of this configuration is to make WordPress correctly recognize HTTPS requests when the site is behind Cloudflare.

<img width="930" height="559" alt="image" src="https://github.com/user-attachments/assets/d674f5ed-5e68-48ea-aab5-378fdc1bafc5" />


---

# Step 11. Final Website Testing

## Testing Checklist

After the configuration was completed, the website was tested.

The following parts were checked:

- Home page availability;
- About page;
- Contacts page;
- Shop page;
- product pages;
- product images;
- product descriptions;
- product tags;
- cart page;
- checkout page;
- HTTPS connection;
- Cloudflare caching;
- email delivery;
- PDF invoice generation.

## Testing Website Availability

The website availability can be checked with:

```bash
curl -I https://flippaslippa.foo
```

Expected result:

```text
HTTP/2 200
```

A successful response means that the website is available through HTTPS.

<img width="943" height="296" alt="image" src="https://github.com/user-attachments/assets/009f2e14-501c-4d36-b244-95d20d79b285" />

<img width="667" height="467" alt="image" src="https://github.com/user-attachments/assets/92efcf62-acd5-449f-87c0-df6a9a91ba3b" />

---

# Step 13. Backup Recommendation

## DigitalOcean Snapshot

After the final setup, it is recommended to create a **Snapshot** in DigitalOcean.

A Snapshot saves the current state of the server and allows the website to be restored if something breaks during future updates or configuration changes.

To create a Snapshot:

```text
DigitalOcean → Droplets → select the Droplet → Snapshots → Take Snapshot
```

Recommended moments for creating Snapshots:

- after completing the initial setup;
- before installing major plugins;
- before updating WordPress;
- before updating WooCommerce;
- before changing server configuration;
- before modifying DNS or SSL settings.

<img width="733" height="426" alt="image" src="https://github.com/user-attachments/assets/b783e482-e64d-4c8f-9055-8ddbe2a2d627" />


---

# Final Result

As a result, the **flippaslippa.foo** online store was successfully deployed and configured.

The final project includes:

- WordPress installed on a DigitalOcean Droplet;
- WooCommerce online store functionality;
- 6 furry slipper products;
- Home, About, Contacts, and Shop pages;
- product names, descriptions, images, prices, and tags;
- custom domain purchased through name.com;
- domain connected to Cloudflare protection;
- Cloudflare DNS configuration;
- Cloudflare caching for static assets;
- HTTPS configured with Caddy;
- WP Mail SMTP for transactional emails;
- PDF Invoices & Packing Slips for WooCommerce;
- WP-CLI database URL replacement;
- basic backup recommendation using DigitalOcean Snapshots.

The website is ready to be demonstrated as a small educational WooCommerce e-commerce project.
