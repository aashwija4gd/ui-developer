# Locale Formatting

## Numbers and currency

- Right-align numbers in tables.
- Add thousands separators.
- Show currency symbols explicitly.
- Keep decimals consistent within a column.
- Use locale-specific formatting for USD, EUR, INR, and JPY.
- Never mix formatting conventions in one column.

## Dates and times

- Use relative time for recent events.
- Use absolute dates for older events.
- Show the time when precision matters.
- Display in the user's local time zone.
- Keep formats consistent throughout the product.

## Phone numbers

- Format for human readability.
- Use E.164 as the canonical base.
- Never display raw digit strings.
- Use `tel:` for clickable phone numbers on mobile.

## Addresses and postal codes

- Order fields by country convention.
- Show Country first in forms.
- Validate postal codes by the selected country.
- Do not force one address format globally.

## Measurement units

- Default to the user's locale.
- Always show the unit alongside the value.
- Allow switching between systems where relevant.

## File sizes, temperature, and time zones

- Use decimal file-size units in UI.
- Show temperature with the correct scale symbol and no extra spacing.
- Store timestamps in UTC and display them in the user's local time.
- Show the time zone when ambiguity exists.
