### ACCESSIBLITY TEST

**Date:** February 26, 2025  
**Evaluated Platform:** Wizer Learning Content  
**Evaluation Tool:** Fezzant Scan

---

## **1. Introduction**

This report presents the findings of an accessibility assessment conducted on the Wizer learning content platform. The assessment was performed to ensure compliance with Web Content Accessibility Guidelines (WCAG) and enhance the overall usability of the platform for all users, including those with disabilities.

## **2. Summary of Findings**

The accessibility evaluation identified a total of **seven (7) issues** that impact the accessibility of the platform. Below is an overview of the issues found:

## **3. Detailed Findings and Recommendations**

### **1. ARIA Attribute Misuse**

**Issue:** Some elements use ARIA attributes that are not permitted for their assigned roles.  
**Example:**

```
<div class="pointer MuiBox-root muiltr-3t06vo" data-testid="button-back-test-id" aria-label="back button">
```

**Recommendation:** Ensure ARIA attributes are correctly applied to elements based on their roles to avoid conflicts and ensure proper screen reader interpretation.

### **2. Buttons Without Discernible Text**

**Issue:** Some buttons lack readable text, which makes them inaccessible to screen readers.  
**Example:**

```
<button class="MuiButtonBase-root MuiIconButton-root ..." tabindex="0" type="button" id=":r3c:" data-testid="iconButton">
```

**Recommendation:** Ensure all buttons have meaningful labels that describe their function.

### **3. Insufficient Color Contrast**

**Issue:** Text and background colors do not meet the minimum contrast ratio required by WCAG 2.1 AA standards. **Examples:**

```
<p class="MuiTypography-root ..." data-id="helpBtn" role="button" tabindex="0" aria-label="Help">Help</p>
<h5 class="MuiTypography-root MuiTypography-h5 ...">Real Life Stories</h5>
```

**Recommendation:** Adjust color contrast to meet the **4.5:1** contrast ratio requirement for normal text and **3:1** for large text.

### **4. Incorrect Heading Order**

**Issue:** Heading levels do not follow a logical sequence (e.g., skipping from H2 to H6). **Example:**

```
<h6 class="MuiTypography-root MuiTypography-subtitle2 text-center muiltr-owxjpu">2</h6>
```

**Recommendation:** Maintain a proper heading hierarchy (e.g., H1 → H2 → H3) to enhance navigation and readability.

### **5. Missing Main Landmark**

**Issue:** The document lacks a primary landmark, which makes it difficult for assistive technologies to navigate. **Example:**

```
<html lang="en">
```

**Recommendation:** Define a main landmark using `<main>` or `role="main"` to improve accessibility.

### **6. Missing Level-One Heading**

**Issue:** The page lacks an `<h1>` element, making it harder for users to understand the main content structure. **Recommendation:** Ensure each page contains a clearly defined `<h1>` element that summarizes its content.

### **7. Uncontained Page Content**

**Issue:** Several elements are not contained within landmarks, affecting navigation. **Examples:**

```
<h5 class="MuiTypography-root MuiTypography-h5 ...">Policies and Procedures</h5>
<a class="MuiTypography-root MuiTypography-caption MuiLink-root ..." href="https://www.wizer-training.com/privacy">Privacy Policy</a>
```

**Recommendation:** Structure content within `<main>`, `<nav>`, `<section>`, and `<article>` elements to improve screen reader navigation.

---

## **4. Conclusion and Next Steps**

The identified issues indicate that Wizer’s learning content needs improvements to ensure full accessibility compliance. The recommended steps for enhancement include:

- Correcting ARIA attributes and adding proper labels.
    
- Improving contrast ratios for better readability.
    
- Ensuring a proper heading structure.
    
- Adding essential landmarks for screen reader navigation.
    

Addressing these issues will significantly improve the user experience for individuals with disabilities and align the platform with WCAG 2.1 AA standards. Further testing is recommended after implementing these fixes to validate the improvements.
