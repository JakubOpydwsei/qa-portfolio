# Exploratory Testing – Allegro.pl

**Date:** 2025-07-04  
**Tester:** Jakub Opyd  
**Browser:** Google Chrome  
**Test Duration:** approx. 45 minutes  
**Test Scope:** Homepage - Search - Product Page - Cart - Login - UI/Responsiveness

---

## 1. Homepage

- Page loads correctly, banners and navigation are visible.
- No major errors in DevTools console.
- Key UI elements such as "Log in", "Cart", and "Categories" are clickable and working.
- Site looks responsive and reacts properly to basic interactions.

## 2. Product Search

- Typed "headphones" and pressed enter.
- Search results appeared fast with relevant products.
- Filtering by price and brand works correctly, no reload issues or visual problems.

## 3. Product Page

- Product images work — hovering enlarges the image.
- Clicked the first result in the list.
- Price, product description, and seller details are clearly visible.
- No warnings, alerts, or issues found on the page and in DevTools console.
- "Add to Cart" button is working and responsive.

## 4. Cart

- After adding a product, a confirmation appeared.
- Cart icon updated to reflect 1 item added.
- Inside the cart: quantity can be changed, product can be removed — all seems functional.
- Noticed promotion being applied dynamically:  
  when increasing the quantity (e.g. from 1 to 2), the page temporarily disables the checkout button for ~2s, then updates the total with the discounted price and re-enables the button.

## 5. Login

- Clicked on "Log in".
- Entered a fake email and random password — correct error message shown.
- Entering only password prompts user to provide email — working validation.
- Entering only email prompts user to provide password — working validation.
- Successfully logged in using valid credentials.
- No warnings and errors in DevTools console.

## 6. Responsiveness

- Tested in mobile view using Chrome DevTools.
- Navigation bar collapses correctly, menu works.
- On very small screens (e.g. <425px width), navigation area (promo banners, deals) becomes clipped and a horizontal scrollbar appears — very poor UX visually.

---

## Console Errors

```
main.MTBjODI0ODZkMA.js:1 [TikTok Pixel] - Invalid pixel ID  
Issue: The pixel ID is invalid. This could prevent your pixel from receiving data.
```

---

## Observed Issues Summary

| Area| Issue | Suggestion |
| --- | --- | --- |
| Responsiveness | Horizontal scrollbar appears below 425px width in promo/nav section| Improve responsive layout or hide certain elements on small screens |
| Analytics | TikTok Pixel reports invalid pixel ID in console | Validate or remove faulty third-party script integration |

---

## Conclusion

Allegro’s web platform is functional and performs well under normal user flows. No major blockers were found. Minor issues related to UX and third-party integration (analytics) were observed. Overall, the platform seems stable, user-friendly, and responsive.
