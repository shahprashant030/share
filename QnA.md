# Mithila Sutra - Finance System Questions for Sneha

Hi Sneha! In order to finalise the finance system architecture, I need some clarification from you. Please write your answers in the **Answer:** lines below each question.

---

## Q1. What counts as "inventory" for Mithila Sutra?

We need to agree on what things the system should track as inventory.

Here are all the possible categories - **please tick or mention which ones apply to our business:**

| Category | Examples |
|---|---|
| Raw materials | Maida, sugar, oil, spices, ghee |
| Packaging materials | Pouches, boxes, labels, tape, wrapping |
| Finished goods | Packed Thekua, Ladoo, Anarsa - ready to sell |
| Equipment / Machines | Grinding machine, sealing machine, weighing scale |
| Utensils / Small tools | Kadai, trays, moulds, spatulas |
| Office / Other supplies | Stationery, cleaning materials, spare parts |

**Q1a.** Which of the above categories should the system track?

> **Answer:**

**Q1b.** Is there anything else that belongs in our inventory that is not listed above?

> **Answer:**

**Q1c.** From a Nepal accounting and tax compliance point of view - what are we legally required to maintain stock records for?

> **Answer:**

---

## Q2. How should inventory be managed?

This is the most important question. There are two completely different ways to handle inventory:

---

**Option A: Track stock count in the system (live inventory)**
The system keeps a running count of every item.
- Every purchase → stock goes up
- Every production batch, sale, or wastage → stock goes down
- At any moment, the portal shows: *"Maida: 45 kg remaining. Pouches: 340 remaining."*

This gives full visibility but means every movement must be recorded (purchases, usage, wastage, sales).

---

**Option B: Record money only (finance-only, no stock count)**
The system only records the money side of things.
- *"Bought maida for Rs. 3,000."*
- *"Sold products for Rs. 10,000."*

No running stock count is maintained in the system. Stock levels are managed physically (notebook, manual count, etc.).

This is simpler to use day-to-day, but the system cannot tell you how much maida you have right now.

---

**Q2a.** Which approach fits how the business actually runs - Option A or Option B?

> **Answer:**

**Q2b.** From your perspective as our CA - is keeping a live stock count in the system necessary, or is recording purchases and sales in the finance ledger enough for tax purposes?

> **Answer:**

*(The following Q2c, Q2d, Q2e, Q2f only apply if you choose Option A above. Skip them if Option B.)*

**Q2c.** When we buy raw materials - the money goes out AND stock goes up at the same time. Should that be one single action in the portal (handles both automatically), or two separate steps (one for finance, one for stock)?

> **Answer:**

**Q2d.** When we record an offline sale - money comes in AND finished goods stock goes down. Should that also be one single action, or two separate steps?

> **Answer:**

**Q2e.** Should the system warn us when any item is running low? For example: *"Maida is low - only 3 kg remaining."* Or is this not needed?

> **Answer:**

**Q2f.** How often would we physically count stock and match it against the system - daily, weekly, or monthly?

> **Answer:**

---

## Q3. How should production be recorded?

When we make a batch of products (Thekua, Ladoo, etc.), raw materials are consumed. How should the system record this?

---

**Option A: Manual entry each time**
Every time we use materials, we type it in manually:
- *"Used 5 kg maida"*
- *"Used 3 kg sugar"*
- *"Used 100 pouches"*

Simple, no setup needed. But requires someone to record every usage carefully.

---

**Option B: Recipe-based (set up once, runs automatically)**
We define a recipe once per product:
- *"1 pack Mithila Ladoo 200g = 100g maida + 80g sugar + 1 pouch"*

Then when we record *"produced 50 packs of Mithila Ladoo today"*, the system automatically deducts the right quantities from each raw material.

More powerful - gives accurate cost per unit and warns if stock is insufficient for a planned batch. But requires setting up and maintaining recipes.

---

**Q3a.** Which approach do you prefer for day-to-day use and accounting accuracy - Option A or Option B?

> **Answer:**

---

## Q4. What stock movements (in and out) happen in our business?

Below is a full list of all the ways stock can go up or down. Please confirm which ones actually happen in Mithila Sutra, and mention any we have missed.

**Stock IN (inventory increases):**

| # | When does stock go up? | Example |
|---|---|---|
| 1 | Purchase from supplier | Bought 50 kg maida |
| 2 | Production output | Made 100 packs of Mithila Ladoo today |
| 3 | Customer return | Customer returned a product → back in stock |
| 4 | Supplier sent back our return | We returned goods but supplier rejected and sent back |
| 5 | Stock adjustment (surplus found) | Physical count shows more than the system |

**Stock OUT (inventory decreases):**

| # | When does stock go down? | Example |
|---|---|---|
| 6 | Used in production | 5 kg maida consumed in today's batch |
| 7 | Offline sale | Sold 20 packs at the local market or shop |
| 8 | Wastage / spoilage | 2 kg sugar got wet and cannot be used |
| 9 | Returned to supplier | Sent 10 defective pouches back to the supplier |
| 10 | Machine sold or scrapped | Old grinding machine sold off |
| 11 | Stock adjustment (shortage found) | Physical count shows less than the system |

**Q4a.** Which of the above situations actually happen in our business? (Mention numbers, e.g. "1, 2, 6, 7, 8")

> **Answer:**

**Q4b.** Is there any other reason stock goes up or down in our business that is not in the list above?

> **Answer:**

**Q4c.** For offline sales (situation 7) - who records it and how often? After every single sale, or once at the end of the day as a total?

> **Answer:**

---

## Q5. Machines and equipment

Machines and equipment are different from consumables like maida - they are not "used up". They stay in the business for years until sold, broken, or scrapped.

**Q5a.** Beyond just *"we have 2 machines, they cost Rs. X"*, do we want to track extra details for each machine? For example:
- Purchase date
- Serial number
- Current condition (Working / Needs Repair / Retired)
- Supplier name and warranty expiry

Or is just the cost and quantity enough?

> **Answer:**

**Q5b.** When a machine is eventually sold or scrapped, how should that be recorded in the system?

> **Answer:**

**Q5c.** Do we need **depreciation tracking** - i.e. the system gradually reducing the book value of a machine each year based on its useful life (e.g. a machine worth Rs. 1 lakh reduces by Rs. 20,000 per year over 5 years)? Or is just recording the original purchase cost enough for now?

> **Answer:**

---

## Q6. Units of measurement

Every inventory item needs a unit - maida is in kg, pouches are in pieces, oil is in litres, etc.

**Option A: Fixed list (system provides the options)**
The system gives a standard dropdown to pick from:
- Weight: kg, g
- Volume: litre, ml
- Count: piece, packet, box, roll, set
- Length: metre

Clean and consistent - no spelling differences or typos.

**Option B: Type your own**
Whoever is entering the item types whatever unit they want. Fully flexible but risks inconsistency over time.

**Q6a.** Does our business use any unit that is not in the fixed list above?

> **Answer:**

**Q6b.** Do you prefer a fixed dropdown list (cleaner reports) or the ability to type any unit freely?

> **Answer:**

---

## Q7. VAT Tracking

Mithila Sutra is VAT registered. Every month, VAT is calculated like this:

```
Output VAT  (VAT collected from customers on sales)
−  Input VAT   (VAT we paid to suppliers on purchases)
=  Net VAT payable to IRD
```

For the system to automatically track this, each finance entry involving VAT needs to record the VAT amount separately. For example:

**When buying raw materials (Input VAT):**
```
Paid to supplier:   Rs. 3,390
  Base amount:      Rs. 3,000
  VAT (13%):        Rs.   390  ← this is claimable input VAT
```

**When recording sales (Output VAT):**
```
Received from customer:  Rs. 11,300
  Base amount:           Rs. 10,000
  VAT (13%):             Rs.  1,300  ← this must be remitted to IRD
```

The system could then show a monthly VAT summary: total output VAT, total input VAT, and net amount due to IRD - ready for filing.

**Q7a.** Should every finance entry involving VAT record the VAT amount separately so the system tracks input/output VAT automatically? Or do you prefer to calculate VAT separately outside the system?

> **Answer:**

**Q7b.** Not every purchase has VAT - some suppliers are not VAT registered, and some goods are VAT exempt. Should the system allow marking each entry as *"VAT applicable"* or *"VAT exempt"* so the VAT summary stays accurate?

> **Answer:**

**Q7c.** Should the system produce a monthly VAT return summary - total output VAT, total input VAT, and net payable to IRD - that you can directly use for IRD filing? Or is a simple running total enough?

> **Answer:**

**Q7d.** Nepal IRD requires VAT bills to include a bill number and the buyer's PAN when purchasing from a VAT-registered supplier. Should the system capture the **supplier's VAT bill number** and **supplier's PAN** for each VAT purchase? (Useful during IRD audits as proof of input VAT claims.)

> **Answer:**

---

## Q8. Supplier / Vendor Tracking

Every time we buy something - raw materials, packaging, a machine - it is from a supplier. How should we handle supplier information?

---

**Option A: Just write the name in the entry**
The supplier name is written as plain text in the description:
- *"Bought 50 kg maida from Ram Traders"*

Simple. No setup needed. But you cannot filter by supplier, cannot see total spending with one supplier, and the name might be written differently each time.

---

**Option B: Maintain a supplier list**
We register each supplier once in the system with:
- Business name
- Contact person and phone number
- PAN number (important for input VAT claims)
- Address
- Notes

Each purchase is then linked to a supplier from this list. This allows:
- Seeing all purchases from a specific supplier
- Knowing total spending with each supplier over any period
- Having the supplier's PAN ready when filing VAT returns

---

**Q8a.** Do we deal with the same suppliers repeatedly (regular vendors), or is it usually different people each time?

> **Answer:**

**Q8b.** Are most of our suppliers VAT registered (meaning their PAN matters for our input VAT claims)?

> **Answer:**

**Q8c.** Which option do you prefer - Option A (simple text) or Option B (proper supplier records)?

> **Answer:**

---

## Q9. Credit Purchases and Credit Sales

Sometimes businesses buy on credit (receive goods now, pay later) or sell on credit (deliver now, collect payment later).

**Credit purchase example:**
We buy packaging pouches worth Rs. 5,000 today but agree to pay in 30 days. The money has not left our account yet, but we owe Rs. 5,000. This is a **payable (sundry creditor)**.

**Credit sale example:**
We supply Rs. 10,000 worth of products to a local shop today, but they will pay us next week. The money has not arrived yet, but they owe us Rs. 10,000. This is a **receivable (sundry debtor)**.

If the business does this, the system would track:
- Who owes us money and how much (receivables)
- Who we owe money to and how much (payables)
- When payments are due
- When they are eventually paid

If we always pay and collect cash on the spot, this feature is not needed.

**Q9a.** Do we buy from suppliers on credit (pay later)?

> **Answer:**

**Q9b.** Do we sell to any shops, distributors, or parties on credit (collect later)?

> **Answer:**

**Q9c.** From your perspective as our CA, should the system formally track outstanding receivables and payables?

> **Answer:**

**Q9d.** If yes - should the system send reminders when a payment is overdue?

> **Answer:**

---

## Q10. TDS (Tax Deducted at Source)

Nepal's Income Tax Act requires us to deduct a percentage (TDS) from certain payments and remit it directly to IRD.

Common payments where TDS applies:

| Payment type | TDS rate |
|---|---|
| Rent (office, godown, production space) | 10% |
| Professional / consulting fees | 15% |
| Salary above the taxable threshold | 15–36% (slab-based) |
| Contract / service payments | 1.5% |

**Example - Rent:**
Monthly rent = Rs. 20,000.
We deduct 10% TDS = Rs. 2,000.
We pay the landlord Rs. 18,000 and remit Rs. 2,000 to IRD.

If the system tracks TDS, it would record:
- Full expense: Rs. 20,000 (rent)
- TDS deducted: Rs. 2,000 (to remit to IRD)
- Paid to landlord: Rs. 18,000

And produce a monthly TDS summary for IRD filing.

**Q10a.** Do we make any payments that require TDS deduction - rent, professional fees, salaries, or contract payments?

> **Answer:**

**Q10b.** Should the system track TDS on each applicable payment so you can file monthly TDS returns directly from the system?

> **Answer:**

**Q10c.** Are there any other TDS situations specific to our business that are not listed above?

> **Answer:**

---

## Q11. Dates: BS or AD? Nepal Fiscal Year?

Nepal's fiscal year runs from 1 Shrawan to 31 Ashadh. All official accounting, tax returns, and financial statements use this fiscal year.

**Q11a.** Should the finance system use **BS dates** for all entries and reports, **AD dates**, or show **both**?

> **Answer:**

**Q11b.** Should all financial reports and the main dashboard default to the **Nepal fiscal year** (Shrawan–Ashadh)? For example, when you open the dashboard, "this year" means 1 Shrawan 2082 to today - not 1 January 2026.

> **Answer:**

**Q11c.** For VAT returns and TDS returns filed with IRD - are they submitted using BS dates or AD dates?

> **Answer:**

---

## Q12. Bank Reconciliation

Every month the bank gives us a statement - the official record of what money moved in and out of our account. Our finance system also has entries for the same period. In theory, both should match perfectly. But small differences can appear:

- A cheque issued to a supplier has not cleared the bank yet
- A bank charge appeared on the statement but was not entered in the system
- A timing difference - money deposited on the 31st appears on the bank statement on the 1st

**Without reconciliation in the system:** the system and the bank statement are two separate records. Differences can silently build up and only get discovered during an audit.

**With reconciliation in the system:** at the end of each month, we open the bank statement, match each entry in the system against the bank statement line by line, flag anything that does not match, and mark the month as *"reconciled"*: a permanent record that the books were verified against the real bank.

**Q12a.** Do you currently do bank reconciliation manually every month?

> **Answer:**

**Q12b.** Should the system provide a formal reconciliation workflow (tick off entries against the bank statement, mark month as reconciled)? Or is manually cross-checking the entries against the bank statement outside the system sufficient?

> **Answer:**

**Q12c.** If yes - should each financial account be reconciled separately? (For example: bank account reconciled separately from eSewa wallet, cash-in-hand, etc.)

> **Answer:**

---

*Thank you! Once you fill this in, I will use your answers to finalise the system design before coding begins.*
