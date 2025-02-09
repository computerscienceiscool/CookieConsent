# User Consent Options Tests

## Test Suite Overview
These test cases verify that users have proper control over their cookie preferences and that their choices are correctly implemented.

## Prerequisites
* Clean browser state
* Developer tools
* Network monitoring tools
* Multiple test accounts (if applicable)

## Test Cases

### TC001: Accept All Functionality
**Description:**  
Verify that the "Accept All" option correctly enables all cookie categories.

**Steps:**
1. Clear browser cookies and cache
2. Load website
3. Click "Accept All" in consent banner
4. Check developer tools for cookie creation
5. Verify third-party scripts activation
6. Document all cookies set

**Expected Results:**
- All cookie categories enabled
- Appropriate cookies created
- Third-party scripts activated
- Consent preference stored
- Banner dismisses properly

**Evidence Collection:**
- Before/after cookie list
- Network requests log
- Consent record

### TC002: Reject All Functionality
**Description:**  
Verify that "Reject All" properly blocks non-essential cookies.

**Steps:**
1. Clear browser cookies and cache
2. Load website
3. Click "Reject All" in consent banner
4. Monitor cookie creation
5. Check third-party script behavior
6. Verify site functionality

**Expected Results:**
- Only essential cookies present
- Non-essential scripts blocked
- Basic site functionality maintained
- Preference stored correctly
- Banner dismisses properly

### TC003: Granular Control Options
**Description:**  
Verify users can select individual cookie categories.

**Steps:**
1. Access detailed cookie settings
2. Test each category toggle:
   - Analytics
   - Marketing
   - Preferences
   - Social Media
3. Save preferences
4. Verify implementation

**Expected Results:**
- Each category toggles independently
- Selected categories work
- Unselected categories blocked
- Changes saved correctly
- Clear feedback provided

### TC004: Preference Center Access
**Description:**  
Verify users can access and modify preferences after initial choice.

**Steps:**
1. Make initial consent choice
2. Locate preference center link
3. Access preference center
4. Modify selections
5. Save changes
6. Verify updates

**Expected Results:**
- Easy access to preference center
- Current settings displayed
- Changes save correctly
- Cookie behavior updates
- Clear confirmation provided

### TC005: Remember User Preferences
**Description:**  
Verify user preferences persist across sessions.

**Steps:**
1. Set specific cookie preferences
2. Close browser
3. Reopen site in new session
4. Check applied preferences
5. Verify cookie status

**Expected Results:**
- Preferences maintained
- Correct cookies present/blocked
- No new consent request
- Settings match previous choices

## Compliance Notes
* Verify compliance with:
  - GDPR consent requirements
  - CCPA opt-out requirements
  - ePrivacy Directive
  - Local privacy laws

## Technical Notes
* Document all preference storage methods
* Note any cross-domain consent sharing
* Record preference version control
* Document audit trail capabilities
