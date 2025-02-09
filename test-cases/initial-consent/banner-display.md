# Cookie Consent Banner Display Tests

## Test Suite Overview
These test cases verify the proper display and functionality of the initial cookie consent banner.

## Prerequisites
* Clean browser state (no existing cookies)
* Access to multiple browsers
* Developer tools enabled
* Network inspection tools

## Test Cases

### TC001: Initial Banner Display
**Description:**  
Verify that the cookie consent banner appears on first visit to the website.

**Steps:**
1. Clear browser cookies and cache
2. Open website in a new browser session
3. Observe initial page load
4. Check banner visibility and positioning
5. Verify no scroll is required to see key options

**Expected Results:**
- Banner appears immediately on page load
- Banner is clearly visible
- All consent options are accessible
- Banner doesn't block critical page content
- No cookies are set before consent (except strictly necessary)

**Evidence Collection:**
- Screenshot of banner
- Developer tools cookie list
- Network tab requests

### TC002: Banner Content Validation
**Description:**  
Verify that the banner contains all required information and options.

**Steps:**
1. Inspect banner content
2. Review all available options
3. Check language clarity
4. Verify links to privacy policy and cookie policy
5. Validate presence of accept/reject options

**Expected Results:**
- Clear explanation of cookie usage
- No pre-ticked boxes
- "Accept All" and "Reject All" options clearly visible
- Access to granular controls available
- Links to relevant policies functional

### TC003: Banner Responsive Design
**Description:**  
Verify banner displays correctly across different screen sizes.

**Steps:**
1. Test on desktop (various resolutions)
2. Test on tablet view
3. Test on mobile view
4. Check orientation changes on mobile
5. Verify all options remain accessible

**Expected Results:**
- Banner adjusts to screen size
- All options remain clickable
- Text remains readable
- No horizontal scrolling required
- Proper spacing maintained

## Compliance Notes
- GDPR Article 7 requirements for consent
- ePrivacy Directive requirements
- CCPA notice requirements
