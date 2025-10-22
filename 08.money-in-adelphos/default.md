---
title: 'money in adelphos'
---


# 💰 Money in ἀδελφός

In ἀδελφός, money can be either:

- **Real money** — traditional currency exchanged outside the system
- **Deferred money** — credit exchanged within the system

Deferred money comes in two forms:
- **Redeemable Money (RM)** — credit with a specified due date
- **Unredeemable Money (UM)** — credit without a defined repayment date

---

## 🔁 Redeemable Money (RM)

Redeemable money functions like an IOU: a promise to pay a specific amount by a future date (e.g., “after 180 days” or “after one year”).

Each user defines their **trust level** in ἀδελφός, which determines how much RM they’re willing to accept from others. This is calculated using the inverse of the trust-bel formula.

### 🧾 Example

> Alice wants to buy a used phone from Bob for $300.  
> Bob has registered in ἀδελφός with a trust level of **20tb**.  
> Using the inverse trust formula:
>
> ```
> RM_max = 10^(20 / 10) × τ_HV = 100 × $1 = $100
> ```
>
> Bob can accept **$100 in RM**. The remaining **$200 must be paid in cash**.

The cash exchange happens outside ἀδελφός. Bob certifies receipt of the $200, Alice confirms she received the phone, and ἀδελφός records the $100 IOU.

---

## 🔄 Using RM in the System

RM is **spendable** within ἀδελφός. Bob can use the $100 credit from Alice to purchase goods or services from other users — as long as their trust limits allow it.

### 🧾 Example

> Bob wants to take French lessons from Lucy, who charges **$20/hour** and has a trust level of **20tb**.  
> Bob books **3 hours** for **$60**.  
> Lucy accepts RM up to **$100**, so Bob pays entirely in RM.  
> He now has **$40 RM** remaining.

---

### 🧠 Observations

1. **Trust is relational**: Lucy must trust Alice (the original issuer of the RM) to accept Bob’s payment. This will be explored further in the discussion of **Level Zero and Level One groups**.

2. **Credit is cumulative**: If Lucy already holds $60 in RM, her remaining trust capacity is $40.  
   > If John wants 5 hours of lessons for $100, he can only pay **$40 in RM** and must cover the rest with **real money**.

---

## 🌀 Unredeemable Money (UM)

UM works similarly to RM, but without a defined repayment date. Each user has separate trust levels for RM and UM — typically, trust in UM is lower due to its non-convertibility.

Though UM may be convertible in special cases (to be discussed later), for now:

> **1 UM = 1 RM in system value**

---

## ⚖️ Key Differences Between RM and UM

- **Interest**: RM may accrue interest; UM does not.
- **Responsibility**:
  - Users are responsible for all RM and UM they issue.
  - They are **only responsible for RM** issued by friends they’ve invited into ἀδελφός.



