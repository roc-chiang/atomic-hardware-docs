# Metafields Configuration Guide

The **Atomic Forge Commerce** framework extracts raw technical parameters directly from Shopify product metafields to render dynamic specification tables, card footprints, and exploded blueprint manifests.

This guide details the namespace keys and values required to fully populate these fields.

---

## 1. Core Metafield Schema

To expose parameters on product cards and specs tables, define the following metafields under **Settings** > **Custom data** > **Products** in your Shopify Admin:

### A. Weight Parameter
- **Namespace & Key**: `custom.weight`
- **Type**: Single line text
- **Description**: Technical weight readout of the item.
- **Example Value**: `38.0g // APEX WEIGHT`

### B. Material Composition
- **Namespace & Key**: `custom.material`
- **Type**: Single line text
- **Description**: Main structural alloy or compound.
- **Example Value**: `Grade 5 Titanium (Ti-6Al-4V)`

### C. Ingress Protection
- **Namespace & Key**: `custom.protection_rating`
- **Type**: Single line text
- **Description**: Waterproof or weather certification rating.
- **Example Value**: `IP68 Pressurized (2.0M / 24H)`

### D. Production Tolerance
- **Namespace & Key**: `custom.tolerance`
- **Type**: Single line text
- **Description**: CNC lathe cutting tolerance allowance.
- **Example Value**: `±0.01mm Calibration`

---

## 2. Setting Up in Shopify Admin

Follow these steps to register keys so they populate automatically on your live store:

1. In your Shopify Admin, click **Settings** (bottom left) > **Custom data**.
2. Click **Products** > **Add definition**.
3. In the **Name** field, enter: `Material` (matching key `material`).
4. Set the **Namespace and key** to exactly: `custom.material`.
5. Select the content type: **Single line text**.
6. Repeat the process for `custom.weight`, `custom.protection_rating`, and `custom.tolerance`.
7. Once registered, edit any Product inside Shopify, scroll to the **Metafields** section at the bottom, and fill in the values.
