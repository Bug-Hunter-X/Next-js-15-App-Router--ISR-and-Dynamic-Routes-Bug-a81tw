# Next.js 15 App Router: ISR and Dynamic Routes Bug

This repository demonstrates a bug encountered in Next.js 15's App Router when using dynamic routes in conjunction with Incremental Static Regeneration (ISR).

## Bug Description

When navigating between pages with dynamic routes that utilize ISR, unexpected behavior occurs.  The issue is particularly noticeable when the data fetching for the ISR is slow or prone to delays. This can lead to stale data being displayed or unpredictable navigation behavior.

## Reproduction Steps

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the development server: `npm run dev`
4. Navigate between different dynamic routes. Observe the data inconsistencies, especially after a delay during ISR.

## Expected Behavior

Consistent and up-to-date data should be displayed across all dynamic routes, reflecting the latest fetched data from the ISR.

## Actual Behavior

Stale or inconsistent data is sometimes displayed, indicating a problem with the data fetching and caching mechanism of ISR in the App Router context.

## Solution

Further investigation is needed to identify the root cause and implement a robust solution.  Possible approaches could involve optimizing the ISR data fetching process or implementing alternative caching strategies.