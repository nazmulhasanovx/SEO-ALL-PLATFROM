# Marketplace Search Architecture (Proposed)

## Intent boundaries
**B2C examples:** “resort in Cox's Bazar”, “hotel in Sreemangal”, “family cottage near [destination]”, “available rooms at [property]”.  
**B2B examples:** “resort management system”, “hotel booking engine software”. These belong to the technology website instead.

## Taxonomy
```text
Marketplace
  Destinations
    Country / Division / District / Area (only with useful real inventory)
  Property listings
    Hotel / Resort / Other verified property types
    Accommodation units
      Room / Cottage / Villa / Apartment / Dormitory (only if actually available)
  Travel guides
    Useful destination and stay-planning information
```

## Candidate URL patterns (DO NOT assume they exist)
`/destinations/{destination-slug}/` for useful real destination pages.  
`/stays/{property-slug}/` for a verified property with sufficient distinct content.

Inventory and pricing changes need an accurate source of truth. No fake availability, rates, review counts or geocoded addresses.

## Linking
Property detail → destination overview → related listings based on real locations.
B2C footer or owner onboarding flow → B2B product website when relevant, without copying SaaS landing pages into travel results.

## Acceptance
Search-engine index only valuable public pages, not guest profiles, reservations, payment details, duplicate search result permutations or site internals.
