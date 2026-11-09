# Reservation Module — Evidence and Scope
**Evidence checked:** 2026-11-09 via public pages; live behaviour not technically tested.

## Public evidence
1. https://technology.bingi.com.bd/solutions/hotels — describes booking arrival at reception, reservation creation, room preparation, check-in/out.
2. https://technology.bingi.com.bd/ecosystem — describes marketplace, website and front desk sources flowing toward HMS reservations and inventory.
3. https://technology.bingi.com.bd/pricing — lists reservation and booking-related plan features; entitlements require per-plan verification.

## Safe factual positioning for editorial drafts
“BinGi presents reservation management as part of its connected hotel operations ecosystem, linking booking sources with the front desk and room-related workflows.”

## Features requiring owner/engineering evidence BEFORE public assertion
- Which booking sources automatically sync in current production?
- Is walk-in/manual booking supported for each commercial plan?
- Can users reschedule, transfer or merge bookings? What restrictions?
- Do room inventory locks and conflict prevention work in all cases?
- Is OTA/channel manager sync available and under which contract?
- What notifications, payment collection and cancellation rules exist?
- What is the exact booking calendar UI, permissions, availability model and time-zone handling?
- Does the booking flow work offline? Do not imply offline connectivity.
- Which dashboard metrics are real production fields?

## Terminology
Reservation = booking record; source = marketplace, hotel website, front desk, or external channel as actually integrated; inventory = availability of physical units (not accommodation type alone).

**Status:** Copy is drafted conservatively and still requires final product checks.
