# Supermarket Price Aggregator (In Development)

## Overview
An automated system consisting of web-scraping bots that monitor major grocery store websites to compare food prices and discounts in real-time. The end goal is a location-aware application that helps users find the cheapest places to buy specific products near them.

## Features
- Scalable web scrapers that bypass anti-bot protections to gather daily price data from multiple supermarket chains.
- Geolocation-based suggestions showing the most cost-effective stores for a user's specific shopping list.
- Real-time updates on discounts and promotional offers.

## Role of AI Management
- Utilized AI to write and maintain complex Playwright/Selenium scraping scripts that adapt to changes in supermarket website layouts.
- Managed the AI architect role to design a fast, high-concurrency database (e.g., PostgreSQL + Redis) capable of handling thousands of price updates per minute.
