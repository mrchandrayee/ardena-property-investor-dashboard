# Ardena — Property Investor Dashboard

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=for-the-badge&logo=github)](https://mrchandrayee.github.io/ardena-property-investor-dashboard/)
[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org) [![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org) [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE)

Runnable HTML/CSS/JavaScript reconstruction of the uploaded **5.1-second** screen recording (720 × 1280, 30 fps).

## Run locally
1. Extract `ardena-property-investor-dashboard.zip`.
2. Open `index.html` in a modern browser.
3. No npm, build tools, or backend required.

Optional:
```bash
python3 -m http.server 8000
```
Then visit `http://localhost:8000`.

## What the recording shows

A dark glassmorphism property-investing workspace branded **Ardena — Property investing**, for Marta Lindqvist in Lisbon, Portugal. The screen includes a persistent left navigation, search, notifications, new action, net worth summary, and a Dark glass toggle.

### Visible navigation
- Invest: Desk, Portfolio, Market, Analytics
- Plan: Calculators, Advisor
- Account: Settings

### Investor desk
- Portfolio value: **€4,565,112** (shown +2.0% since Dec)
- Homes / cities summary: 7 homes in 6 cities; 14 of 15 units let; 50% borrowed against them
- Monthly rent: **€22,701**
- Equity: **€2.30M**
- Needs you today: rent collection and late-payment reminders
- Loan repayments chart and property value by city
- Statement and Add property actions

### Calculators screen (shown in the video)
Tabs: Mortgage, Rental yield, Rent or buy.

Visible Mortgage inputs:
- Home price: **€420,000**
- Deposit: **30% · €126k**
- Interest rate: **3.4%**
- Term: **30 years**

Visible result:
- Each month: **€1,122**
- Borrowed: **€252,996**
- Interest in total: **€150,920**
- Total repaid: **€403,916**

The demo calculator computes a standard amortising monthly payment from its input values. The visible source values above are transcribed from the video.

### Other screens in the recording
- Portfolio: property cards and asset list.
- Market: market tracking and opportunity list.
- Analytics: portfolio performance and income breakdown.
- Mortgage calculator screen.
- Advisor: suggested actions and question entry.
- Property images/cards visible on the final screen.

## Readable source code visible in the video

The code panel is titled `src/motion.ts`. The visible TypeScript function is:

```ts
// every page's cards land in reading order
export function landCards(
  cards: Element[],
  { y = 26, stagger = 0.06, delay = 0 } = {},
) {
  const tl = gsap.timeline({ delay: dur(delay) });
  if (!cards.length) return tl;
  tl.fromTo(cards,
    { opacity: 0, y, scale: 0.985 },
    { opacity: 1, y: 0, scale: 1, duration: dur(0.8),
      ease: 'expo.out', stagger: dur(stagger),
      clearProps: 'transform,opacity' });
  return tl;
}
```

This is the visible snippet transcribed from the code panel. `dur()` is referenced but its definition is outside the visible area. The recreated project uses CSS transitions and a small JavaScript page renderer; GSAP is not required.

## Included functionality
- Desk, Portfolio, Market, Analytics, Calculators, Advisor and Settings pages.
- Responsive dark-glass dashboard and collapsible sidebar.
- Dark / light appearance toggle.
- Portfolio property cards and add-property modal.
- Portfolio value, rental income, equity and yield metrics.
- Mortgage repayment calculator.
- Rental-yield calculator.
- Rent-or-buy comparison helper.
- Market watchlist and illustrative listing table.
- Analytics and income breakdown panels.
- Search navigation and demo statement/reminder actions.

## Files
- `index.html` — app shell and add-property modal.
- `styles.css` — responsive dark-glass visual system, charts, cards and layout.
- `app.js` — sample property data, navigation, dashboard pages and calculators.
- `README.md` — source observations, visible snippet and run instructions.

## Accuracy / limitations
The recording shows the running dashboard and a readable `src/motion.ts` animation snippet, not the original full application source repository. This project is a screen-based reconstruction; it does not reproduce proprietary source code that is not visible in the recording. The property list and some market/analytics figures are illustrative where the video does not show their exact values. The calculator's Mortgage defaults and headline result are aligned to the figures visible in the video; calculations update when inputs are changed.

No bank, mortgage lender, property listing provider, rent collection, tenant records, valuation provider, or external market data is connected. Add-property, reminders and statement export are local demo actions. Property photographs load from Unsplash when internet is available.

## 👨‍💻 Author

**mrchandrayee** · [GitHub](https://github.com/mrchandrayee)

## 📄 License

[MIT License](./LICENSE)
