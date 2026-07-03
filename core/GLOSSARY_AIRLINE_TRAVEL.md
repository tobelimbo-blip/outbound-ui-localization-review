# Airline and Travel Glossary

Confirm each carrier's approved terminology, locale, product model, and operational data definitions. Do not treat related states as synonyms.

| Chinese / Intent | Recommended | Avoid | Context | Notes | Risk |
|---|---|---|---|---|---|
| 预订 / 订单 | Booking / Reservation | Order | Trip management | Use `booking` for a reservation record; do not assume a ticket was issued. | High |
| 行程 | Trip / Itinerary | Journey order | My Trips, travel details | `Trip` is customer-friendly; `itinerary` is the structured travel plan. | Medium |
| 管理预订 | Manage booking | Booking management | Navigation, CTA | Confirm singular or plural product style. | Low |
| 机票 | Ticket / Flight | Booking | Purchase, ticket status | A booking, ticket, and completed purchase are not automatic synonyms. | High |
| 奖励机票 | Award ticket | Free ticket | Loyalty redemption | Fees or eligibility may still apply; avoid `free`. | High |
| 航班状态 | Flight status | Booking status | Operations | Keep operational flight state separate from booking and ticket state. | High |
| 计划 | Scheduled | Planned | Departure, arrival | Refers to the published schedule, not a current estimate. | High |
| 预计 | Estimated | Expected schedule | Departure, arrival | Label the relevant time and data source when material. | High |
| 延误 | Delayed | Late / Postponed | Flight status | Do not imply cancellation. | High |
| 取消 | Cancelled / Canceled | Closed | Flight status | Follow the selected English locale consistently. | High |
| 已起飞 / 已出发 | Departed | Took off | Flight status | Confirm whether the source means gate departure or takeoff. | High |
| 已到达 | Arrived | Landed | Flight status | Confirm whether the source means landing or gate arrival. | High |
| 登机中 | Boarding | Boarding now soon | Flight status | Distinguish active boarding from boarding time. | High |
| 值机 | Check-in / Check in | Checkin | Service, action | `Check-in` is a noun; `Check in` is a verb. | Medium |
| 值机开放 | Check-in open | Flight open | Status | Include channel or time restrictions when material. | High |
| 值机关闭 | Check-in closed | Check-in finished | Status | Does not mean the flight is cancelled. | High |
| 选座 | Seat selection / Select seats | Choose chair | Service, CTA | Confirm whether selection is paid or restricted. | Medium |
| 额外行李 | Extra baggage | Extra luggage | Ancillary service | Do not imply it was already purchased. | Medium |
| 预付费行李 | Prepaid baggage | Bought baggage | Ancillary service | Carrier definitions and cutoff times vary. | High |
| 行李额 | Baggage allowance | Baggage amount | Fare, policy | Specify weight, pieces, route, or fare rules when relevant. | High |
| 特殊协助 | Special assistance | Special service | Accessibility, travel support | Use a specific service name when available. | High |
| 轮椅服务 | Wheelchair assistance | Wheelchair service request done | Assistance request | Clarify airport stage or assistance level when distinguished. | High |
| 赚取里程 | Earn miles | Get mileage | Loyalty | Do not imply every purchase or flight qualifies. | Medium |
| 兑换里程 | Redeem miles | Exchange miles | Loyalty | Distinguish redemption from transfer or conversion. | Medium |
| 里程余额 | Mileage balance | Miles amount | Loyalty account | Clarify available, pending, or expiring miles when relevant. | High |
