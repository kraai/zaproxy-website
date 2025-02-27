---
# This page was generated from the add-on.
title: Traditional Markdown Report
type: userguide
---

# Traditional Markdown Report

### Sample

#### Header `Risk (Confidence)`

This header is a combination identifier, showing Risk followed by Confidence. For example `High (Medium)` , would indicate a High risk issue identified with Medium confidence.

```

# ZAP Scanning Report

## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 2 |
| Medium | 4 |
| Low | 8 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- |
| Anti-CSRF Tokens Check | High | 10 |
| Cross Site Scripting (Reflected) | High | 2 |
| Buffer Overflow | Medium | 529 |
| Content Security Policy (CSP) Header Not Set | Medium | 58 |
| Example Passive Scan Rule: Denial of Service | Medium | 7 |
| X-Frame-Options Header Not Set | Medium | 55 |
| Absence of Anti-CSRF Tokens | Low | 73 |
| Application Error Disclosure | Low | 1 |
| Cookie No HttpOnly Flag | Low | 1 |
| Cookie without SameSite Attribute | Low | 2 |
| In Page Banner Information Leak | Low | 3 |
| Information Disclosure - Debug Error Messages | Low | 1 |
| Permissions Policy Header Not Set | Low | 59 |
| X-Content-Type-Options Header Missing | Low | 62 |
| Information Disclosure - Suspicious Comments | Informational | 58 |
| Loosely Scoped Cookie | Informational | 3 |
| Modern Web Application | Informational | 33 |
| Non-Storable Content | Informational | 2 |
| Storable and Cacheable Content | Informational | 64 |
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 32 |

## Alert Detail

### [ Anti-CSRF Tokens Check ](https://www.zaproxy.org/docs/alerts/20012/)

##### High (Medium)

### Description

A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.

CSRF attacks are effective in a number of situations, including:
    * The victim has an active session on the target site.
    * The victim is authenticated via HTTP auth on the target site.
    * The victim is on the same local network as the target site.

CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.

* URL: http://localhost:8080/bodgeit/advanced.jsp
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<form id="advanced" name="advanced" method="POST" onsubmit="return validateForm(this);false;">`
* URL: http://localhost:8080/bodgeit/advanced.jsp
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<form id="query" name="advanced" method="POST">`
* URL: http://localhost:8080/bodgeit/basket.jsp
  * Method: `GET`
  * Parameter: ``
  * Attack: ``
  * Evidence: `<form action="basket.jsp" method="post">`

```
