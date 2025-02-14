# DevOps Tech Challenge

## **Challenge Details - The Magic Item Identifier**

The DevOps team at YAGRO serve as the infrastructure engineers for the company. Strong competency with both AWS (or other cloud environments) and creating CI/CD pipelines are required for this position.

This challenge is not about creating an all-singing and all-dancing product, it is about seeing how you implement a solution and the ways you go about it. Don’t go and give up a whole week working on this, that wouldn’t be fair on you 😃

## Overview
You will create a Python-based AWS Lambda function that serves an API providing metadata about magic items for a game. Given an item name as a query parameter, the API will return predefined details about the item, including its rarity, description, and power level.

## Requirements
### 1. Write a Python function that:
- Accepts an HTTP request with a magic item name as a query parameter.
- Looks up the item in a predefined dictionary of 10 items.
- Returns a JSON response with:
  - Name: The item name
  - Rarity: One of (Common, Uncommon, Rare, Epic, Legendary)
  - Description: A short predefined description
  - Power: An integer between 1-100
### 2. Deploy the function as an AWS Lambda behind API Gateway, making it accessible via HTTP.
### 3. URL Structure: 

- `GET https://your-api-url.com/item?name=Shadowfang`
- If the item exists, return its details.
- If it doesn’t, return an error message.

### 4.	Data Source
The API should serve the following 10 predefined items:
```JSON
{
  "items": {
    "Shadowfang": {
      "rarity": "Epic",
      "description": "A blade that whispers the secrets of the night.",
      "power": 87
    },
    "Stormbringer": {
      "rarity": "Legendary",
      "description": "A hammer crackling with the energy of a thousand storms.",
      "power": 95
    },
    "Eldertome": {
      "rarity": "Rare",
      "description": "A dusty tome filled with forgotten spells.",
      "power": 72
    },
    "Phantom Cloak": {
      "rarity": "Uncommon",
      "description": "A cloak that flickers between the material and ethereal planes.",
      "power": 58
    },
    "Inferno Dagger": {
      "rarity": "Rare",
      "description": "A dagger that burns with an undying flame.",
      "power": 80
    },
    "Gauntlet of Titans": {
      "rarity": "Legendary",
      "description": "A massive gauntlet that grants superhuman strength.",
      "power": 99
    },
    "Venomfang": {
      "rarity": "Epic",
      "description": "A bow that poisons its targets with deadly precision.",
      "power": 85
    },
    "Void Amulet": {
      "rarity": "Common",
      "description": "A mysterious amulet that absorbs weak spells.",
      "power": 40
    },
    "Echoing Horn": {
      "rarity": "Uncommon",
      "description": "A horn that, when blown, repeats its sound three times.",
      "power": 55
    },
    "Crystal Aegis": {
      "rarity": "Rare",
      "description": "A shield made of enchanted crystal, reflecting magic attacks.",
      "power": 78
    }
  }
}
```

### 5.	Error Handling
- If an item isn’t found, return:
```JSON
{
  "error": "Item not found. Try another name."
}
```


## Bonus Tasks (if time allows)
- Add case-insensitive lookup (e.g., “shadowfang” should still match “Shadowfang”).
- Support a wildcard query (`GET /item?name=random`) to return a random item.
- Implement basic logging (e.g., log request timestamps and item lookups).

## **Submission**

Please upload your code to GitHub (or alike) and submit via email to the YAGRO team member you have been speaking too.
