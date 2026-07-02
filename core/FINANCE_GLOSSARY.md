# Finance and Fintech UI Glossary

This is a practical UI review reference, not an official financial dictionary. Meanings vary by product, jurisdiction, ledger model, and payment rail. Confirm the underlying business state before replacing a financial term.

| Term | Usage note |
|---|---|
| Account balance | A general balance recorded for an account; clarify whether it is current, ledger, available, or another defined balance. |
| Available balance | Funds currently available for use under the product's rules; it may exclude holds, pending debits, or unavailable deposits. Do not substitute `account balance` without checking the calculation. |
| Total assets | Aggregated asset value within the stated scope; specify included accounts, valuation time, and currency when material. |
| Pending transaction | A transaction initiated but not final; do not imply that it has settled, failed, or can always be cancelled. |
| Transaction history | A record of account activity; state whether pending items, filters, or a limited date range are included. |
| Transfer | Movement of funds between accounts or parties; clarify source, destination, timing, and fees when they affect the action. |
| Recipient | The person or entity receiving funds or a message; often the clearest general consumer term. |
| Beneficiary | A formal banking term for a party designated to receive funds; do not use it merely to sound more financial. |
| Payment | Money sent or due for goods, services, obligations, or another defined purpose; distinguish initiated, completed, failed, and refunded states. |
| Scheduled payment | A payment set to be initiated on a future date; do not imply that funds have already been sent or reserved unless true. |
| Exchange rate | The rate used to convert one currency to another; identify the currency pair, direction, rate timing, and whether fees or markups are separate when material. |
| Currency exchange | The action or service of converting currencies; use `exchange rate` for the numeric rate itself. |
| Cross-border transfer | A transfer across countries or relevant payment jurisdictions; state currencies, fees, recipient amount, and timing when needed. |
| Cash flow | Money moving into and out of a business or account over a period; usually an analytical label, not a synonym for balance. |
| Funds in transit | Funds sent through a transfer process but not yet available to the recipient. Confirm whether the product tracks initiation, clearing, settlement, or availability before using this label. |
| Incoming payment | Money expected or received by the account; pair with a precise status to show whether it is pending or available. |
| Outgoing payment | Money being sent or already sent from the account; pair with a precise status to show whether it is scheduled, pending, or completed. |
| Approval | A business or workflow decision permitting an action; it is not automatically the same as payment authorization. |
| Authorization | Permission or a hold associated with a transaction or account action. In card flows, authorization does not necessarily mean capture or settlement. |
| Settlement | The stage at which obligations or transferred funds are finalized under the relevant system; do not use it as a generic synonym for payment completion without confirmation. |
| Invoice | A document or record requesting payment for specified goods or services; distinguish draft, issued, paid, overdue, and void states. |

## Review cautions

- Keep available, current, ledger, pending, and total balances distinct.
- Keep approval, authorization, capture, payment, clearing, and settlement distinct when the product exposes those stages.
- Never invent a fee-inclusive rate, settlement promise, or fund-availability claim.
- State the currency, direction, effective time, and fee treatment when an exchange-rate label could otherwise mislead.
