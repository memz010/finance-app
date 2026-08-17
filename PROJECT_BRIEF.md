# Finance App Project Brief

## Product idea

A responsive personal-finance web application that helps many users manage income, expenses, budgets, savings, and financial goals. Each user's financial data must remain private and separate.

## Planned features

Status convention: `+` means pending and `-` means completed and verified.

+1. User registration, login, logout, email verification, and password recovery.
+2. Add salary and other sources of income.
+3. Create custom spending, saving, and investment categories.
+4. Allocate a fixed amount or percentage of income to each category.
+5. Show the calculated amount for percentage-based allocations and allow users to mark allocations as completed.
+6. Record expenses with amount, date, category, wallet, currency, and description.
+7. Support multiple currencies, especially USD and Syrian pound (SYP).
+8. Let users select a Central Bank rate, market rate, or custom manual exchange rate.
+9. Store the original amount, original currency, exchange rate used, converted amount, and transaction date for every financial transaction.
+10. Create financial goals with a target amount and target date.
+11. Recommend how much and what percentage of income the user should save toward a goal, and display progress and an estimated completion date.
+12. Calculate a safe daily spending allowance from the remaining monthly budget and remaining days.
+13. Provide daily, weekly, and monthly summaries.
+14. Show spending totals by category and charts comparing income, expenses, and savings.
+15. Display online exchange rates and gold prices, with cached data and manual fallbacks.
+16. Provide Arabic and English interfaces and a mobile-friendly design.

## External data plan

- LiraScope is the initial candidate for Syrian Central Bank and market exchange rates.
- Gold API is the initial candidate for international gold prices.
- External data will be requested by the backend, cached, and periodically refreshed instead of being requested separately by every user's browser.
- API providers and their terms must be verified again during implementation.

## Technology plan

- Application: Next.js with TypeScript and App Router
- Styling: Tailwind CSS
- Database: PostgreSQL hosted by Supabase
- Authentication: Supabase Auth
- Database security: Supabase Row Level Security plus server-side ownership checks
- Charts: Recharts
- Hosting: Vercel
- Source control: Git and GitHub
- Repository: https://github.com/memz010/finance-app.git

## Planned implementation order

1. Initialize the Next.js project.
2. Create the responsive layout and navigation.
3. Configure Supabase and authentication.
4. Design the database schema and Row Level Security policies.
5. Build wallets and currency settings.
6. Build income and expense tracking.
7. Build categories and budget allocations.
8. Build daily spending calculations.
9. Build financial goals.
10. Build reports and charts.
11. Integrate exchange-rate and gold-price services.
12. Test security, calculations, currencies, and mobile layouts.
13. Deploy to Vercel and configure production settings.

## Development rule

Implement and test one stage at a time. Never expose database administrator credentials or third-party API secrets in browser code or commit `.env.local` to Git.
