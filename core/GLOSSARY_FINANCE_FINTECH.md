# Finance and Fintech Glossary

Use the verified product lifecycle and accounting meaning. Do not infer payment, transfer, refund, or balance states from fluent wording alone.

| Chinese / Intent | Recommended | Avoid | Context | Notes | Risk |
|---|---|---|---|---|---|
| 可用余额 | Available balance | Account balance | Account overview | Means funds currently available for use. | High |
| 当前余额 | Current balance | Available balance | Account overview | May include pending or unavailable funds; confirm the product definition. | High |
| 账面余额 | Ledger balance | Book balance | Banking | Use only when it matches the accounting definition. | High |
| 待处理 | Pending | Processing | Payment, transfer | `Pending` names a state; `Processing` implies active work. | High |
| 已授权 | Authorized | Paid / Completed | Card payment | Authorization is not capture or settlement. | High |
| 已扣款 | Captured / Charged | Authorized | Card payment | Confirm whether funds were captured or merely reserved. | High |
| 已结算 | Settled | Completed | Payment, transfer | Use only after settlement in the underlying system. | High |
| 已批准 | Approved | Completed | Internal workflow | Approval does not mean funds were sent or settled. | High |
| 失败 | Failed | Unsuccessful done | Payment, transfer | State whether funds moved and whether retry is safe. | High |
| 退款处理中 | Refund pending / Refund in progress | Refunding | Refund status | Distinguish merchant initiation from bank processing. | High |
| 已退款 | Refunded | Refund successful | Refund status | Confirm full versus partial refund and destination. | High |
| 手续费 | Fee / Service fee | Handling charge | Pricing, summary | Name the fee and whether it is included. | High |
| 汇率 | Exchange rate | Exchange price | Currency conversion | Show currency direction and timestamp when material. | High |
| 到账金额 | Recipient gets / Amount received | Actual arrival amount | Transfer summary | Confirm whether fees are included or estimated. | High |
| 转账 | Transfer | Remittance | Banking, wallet | `Remittance` is appropriate only in relevant formal contexts. | High |
| 收款人 | Recipient / Beneficiary | Receiver | Transfer | `Beneficiary` is common in banking; `recipient` is friendlier. | Medium |
| 银行账户 | Bank account | Banking account | Account, payout | Clarify ownership and account type when required. | High |
| 身份验证 | Identity verification | Identity validation | Onboarding, KYC | Do not claim regulatory approval or verification not performed. | High |
| 自动续费 | Auto-renewal | Automatic fee deduction | Subscription, billing | State timing, amount basis, and cancellation rule in approved copy. | High |
| 账单周期 | Billing cycle | Payment period | Subscription, account | Distinguish billing date from service period. | Medium |
