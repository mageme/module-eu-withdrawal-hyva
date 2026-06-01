# MageMe EU Withdrawal — Hyva Theme Companion

> Hyva theme compatibility for the EU Withdrawal customer flow — pure Tailwind and Alpine.js, no KnockoutJS, no jQuery.

[![Latest Version](https://img.shields.io/packagist/v/mageme/module-eu-withdrawal-hyva.svg?style=flat-square)](https://packagist.org/packages/mageme/module-eu-withdrawal-hyva)
[![Downloads](https://img.shields.io/packagist/dt/mageme/module-eu-withdrawal-hyva.svg?style=flat-square)](https://packagist.org/packages/mageme/module-eu-withdrawal-hyva)
[![Hyva](https://img.shields.io/badge/Hyva-1.3.11%2B-21CFD5.svg?style=flat-square)](https://www.hyva.io)
[![PHP](https://img.shields.io/badge/PHP-8.1%20%7C%208.2%20%7C%208.3%20%7C%208.4%20%7C%208.5-777BB4.svg?style=flat-square)](https://php.net)
[![License](https://img.shields.io/badge/license-MageMe%20EULA-blue.svg?style=flat-square)](https://mageme.com/license/)

Hyva theme companion for [`mageme/module-eu-withdrawal`](https://github.com/mageme/module-eu-withdrawal). Re-renders the storefront-facing withdrawal flow with the Hyva design system. Install it when your storefront runs on a Hyva theme.

**[Documentation](https://docs.mageme.com)** · **[Base module](https://github.com/mageme/module-eu-withdrawal)** · **[Get Pro features](https://mageme.com/magento-2-withdrawal-button-extension.html)**

---

## What it does

Hyva-native rendering for the customer-facing parts of the base module:

- **Withdrawal flow** at `/withdraw-contract/` — the guided flow (find order → select items → review & confirm) for both the guest lookup and the logged-in order picker.
- **Customer account** — the "Withdrawal requests" section.
- **Sales order view** — the "Start return" button and active-withdrawal banner.

Tailwind utility classes and a single Alpine component replace the base module's KnockoutJS. **No compliance behaviour is added or removed** — this is purely a theme-rendering layer.

For **Hyva Checkout** (the pre-contract block and waiver step on the checkout itself), install the separate [Hyva Checkout companion](https://github.com/mageme/module-eu-withdrawal-hyva-checkout).

## Requirements

- **EU Withdrawal** base module (pulled automatically)
- `hyva-themes/magento2-theme-module` **≥ 1.3.11**
- Magento **2.4.4–2.4.9**, **PHP 8.1–8.5**

## Install

```bash
composer require mageme/module-eu-withdrawal-hyva
bin/magento module:enable MageMe_EUWithdrawal Hyva_MageMeEUWithdrawal
bin/magento setup:upgrade
bin/magento cache:flush
```

Recompile the Hyva Tailwind bundle so the classes used by this module are picked up (substitute your child theme's `web/tailwind/` path if applicable):

```bash
cd vendor/hyva-themes/magento2-default-theme/web/tailwind
npm install && npm run build
```

## Custom Magento development

Need a feature an extension doesn't cover, or a bespoke Magento build? MageMe takes on custom extension development and integration work.

→ **[Custom Magento development](https://mageme.com/magento-services/custom-development)**

## Support

- Documentation: [docs.mageme.com](https://docs.mageme.com)
- Bug reports and feature requests: [GitHub Issues](https://github.com/mageme/module-eu-withdrawal-hyva/issues)

## Disclaimer

This is a **technical theme-compatibility shim** — it re-implements the flow in Alpine + Tailwind and adds or removes no compliance functionality. The merchant is responsible for verifying the flow renders correctly under their Hyva theme and version before going to production. See the base module's [full disclaimer](https://docs.mageme.com).

## License

Distributed **free of charge** as a free-tier companion, governed by the **MageMe End User License Agreement** ([mageme.com/license](https://mageme.com/license/)).

---

**MageMe** builds Magento 2 and Adobe Commerce extensions for B2B merchants — form building, quoting, catalog control, and EU compliance.