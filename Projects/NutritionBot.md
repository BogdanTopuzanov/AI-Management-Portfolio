# AI Nutrition & Chef Bot

## Overview
A smart, proactive Telegram bot designed to act as a personal nutritionist. Unlike standard bots, it initiates conversations based on the user's schedule.

## Features
- Proactively asks about available ingredients and cooking time using fast Inline Keyboards.
- Maintains a persistent SQLite database of user dietary restrictions and ingredient history.
- Uses AI to generate step-by-step recipes on the fly based *only* on available ingredients.

## Role of AI Management
- Designed the Finite State Machine (FSM) architecture for the bot.
- Instructed AI on prompt engineering for recipe generation to prevent hallucinations (e.g., adding ingredients the user doesn't have).
