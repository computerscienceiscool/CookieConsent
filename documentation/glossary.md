# Cookie Consent Testing Glossary

## A

### Acceptance Criteria
Conditions that must be met for a test to pass.

### Accessibility Testing
Verification that consent mechanisms are usable by people with disabilities.

## B

### Banner
The initial cookie consent notice shown to users.

### Browser Storage
Methods for storing data including cookies, localStorage, and sessionStorage.

## C

### CCPA (California Consumer Privacy Act)
Privacy law affecting California residents' data rights.

### Consent
User permission for data processing activities.

### Cookie
Small piece of data stored on user's device.
```javascript
// Example cookie structure
{
    name: 'consent_status',
    value: 'accepted',
    domain: '.example.com',
    expires: '2024-12-31',
    secure: true,
    httpOnly: true,
    sameSite: 'Strict'
}
```

## D

### Data Subject Rights
Rights granted to individuals under privacy laws.

### DPIA (Data Protection Impact Assessment)
Assessment of privacy risks in data processing.

## E

### ePrivacy Directive
EU directive concerning electronic communications privacy.

### Evidence
Documentation proving test execution and results.

## G

### GDPR (General Data Protection Regulation)
EU privacy regulation.

### Granular Consent
Allowing users to choose specific processing purposes.

## H

### HTTP-Only Flag
Cookie security attribute preventing JavaScript access.

## I

### Informed Consent
Consent given with full understanding of implications.

## L

### Logging
Recording of consent actions and decisions.

## P

### Preference Center
Interface for managing consent choices.

### Privacy by Design
Incorporating privacy considerations from the start.

## R

### Regression Testing
Testing to ensure changes don't break existing functionality.

### Retention Period
Duration for keeping consent records.

## S

### Same-Site Attribute
Cookie attribute controlling cross-site behavior.

### Secure Flag
Cookie security attribute requiring HTTPS.

### Storage Validation
Verification of consent storage implementation.

## T

### Test Case
Documented set of conditions and steps for testing.

### Third-Party Cookie
Cookie set by domain other than current website.

## U

### User Flow
Sequence of steps users take through consent process.

## V

### Validation
Process of verifying correct implementation.

## Technical Terms

### API Endpoints
```javascript
// Example consent endpoints
const endpoints = {
    getConsent: '/api/consent/status',
    updateConsent: '/api/consent/update',
    withdrawConsent: '/api/consent/withdraw',
    verifyConsent: '/api/consent/verify'
};
```

### Storage Methods
```javascript
// Example storage implementations
const storage = {
    cookie: document.cookie,
    localStorage: window.localStorage,
    sessionStorage: window.sessionStorage,
    indexedDB: window.indexedDB
};
```

### Testing Tools
```javascript
// Example testing utilities
const tools = {
    cookieChecker: 'Browser DevTools',
    networkMonitor: 'Charles Proxy',
    automationTool: 'Selenium WebDriver',
    performanceTool: 'Lighthouse'
};
```

## Compliance Terms

### Legal Bases
Valid reasons for processing personal data:
- Consent
- Contract
- Legal obligation
- Vital interests
- Public task
- Legitimate interests

### Required Documentation
```markdown
1. Privacy Policy
2. Cookie Policy
3. Consent Records
4. Processing Records
5. Impact Assessments
```

### Risk Levels
- Low: Minimal privacy impact
- Medium: Moderate privacy concerns
- High: Significant privacy risks
- Critical: Severe privacy implications