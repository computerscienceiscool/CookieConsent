# Cookie Checker Tool

## Overview
This tool helps analyze and validate cookies set by websites, checking for compliance with privacy regulations and security best practices.

## Features
- Cookie detection and analysis
- Compliance validation
- Security check
- Reporting capabilities

## Usage Example
```javascript
// Cookie Checker Tool
class CookieChecker {
    constructor() {
        this.cookies = [];
    }

    // Get all cookies from current page
    getAllCookies() {
        return document.cookie.split(';').map(cookie => {
            const [name, value] = cookie.split('=').map(c => c.trim());
            return {
                name,
                value,
                attributes: this.getCookieAttributes(name)
            };
        });
    }

    // Get specific cookie attributes
    getCookieAttributes(cookieName) {
        // Use browser dev tools API to get full cookie info
        return {
            secure: true, // example
            httpOnly: true,
            sameSite: 'Strict',
            domain: '.example.com',
            path: '/',
            expires: 'session'
        };
    }

    // Check cookie compliance
    checkCompliance(cookie) {
        return {
            hasSecureFlag: cookie.attributes.secure,
            hasHttpOnlyFlag: cookie.attributes.httpOnly,
            hasSameSiteAttribute: !!cookie.attributes.sameSite,
            appropriateExpiry: this.checkExpiry(cookie.attributes.expires),
            appropriateScope: this.checkScope(cookie.attributes.domain, cookie.attributes.path)
        };
    }

    // Generate report
    generateReport() {
        const cookies = this.getAllCookies();
        return cookies.map(cookie => ({
            cookie,
            compliance: this.checkCompliance(cookie),
            recommendations: this.generateRecommendations(cookie)
        }));
    }
}

// Usage
const checker = new CookieChecker();
const report = checker.generateReport();
console.log('Cookie Analysis Report:', report);
```

## Testing Script
```javascript
// Example test script for cookie checker
async function testCookieCompliance() {
    try {
        // Initialize checker
        const checker = new CookieChecker();
        
        // Get current cookies
        const cookies = checker.getAllCookies();
        
        // Test results
        const results = {
            totalCookies: cookies.length,
            compliantCookies: 0,
            issues: []
        };
        
        // Check each cookie
        cookies.forEach(cookie => {
            const compliance = checker.checkCompliance(cookie);
            if (Object.values(compliance).every(v => v === true)) {
                results.compliantCookies++;
            } else {
                results.issues.push({
                    cookie: cookie.name,
                    issues: Object.entries(compliance)
                        .filter(([_, value]) => !value)
                        .map(([key]) => key)
                });
            }
        });
        
        return results;
    } catch (error) {
        console.error('Error testing cookies:', error);
        throw error;
    }
}
```

## Features to Add
1. Automated category detection
2. Third-party cookie analysis
3. Consent matching validation
4. Compliance report generation
5. Cookie lifetime monitoring

## Usage Instructions
1. Open browser developer tools
2. Copy script to console
3. Run the checker
4. Review generated report

## Integration Notes
- Can be integrated with automated testing
- Works with major testing frameworks
- Supports CI/CD pipelines
- Can generate compliance reports