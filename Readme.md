# Late deliveries on Olist

Why are orders on Olist, a Brazilian e-commerce marketplace, delivered late, and what can be done about it?

- **Data:** Kaggle's olistbr/brazilian-ecommerce: 99,092 orders from Jan 2017 to Aug 2018.
- **Slides:** [Olist – Late deliveries](https://docs.google.com/presentation/d/1sB2HCSQnkUJ1zn6dvesM29FHtNqCruZHDlvIneC-L2Q/edit?usp=sharing) · [PDF slides](olist_late_deliveries_slides.pdf)

## Findings
- **6.8% of delivered orders are late**, and customers punish it. On-time orders average 4.3 stars; late orders reviewed while the customer is still waiting average 1.8.
- **Lateness comes in waves.** Black Friday 2017, Feb–Mar 2018 and the May 2018 truckers' strike add about 37% of all late orders on top of a steady rate of about 4%.
- **Carriers cause most late orders.** In 72% the seller handed over on time, and in another 15% the order would have been late anyway.
- **Two route groups, SP → Rio and SP → North-East, carry 15% of orders but a third of carrier-late orders:** more than twice the average rate. SP → Rio is mostly the spells; SP → North-East is structural.
- **The North-East's promise covers typical deliveries, not the long tail.** Its 90th percentile arrives on the promised day.

## Recommendations
1. Fix the hotspot routes: route-level on-time targets for carriers, and alternative carriers.
2. Expand the seller base outside São Paulo.
3. Set promises by route and season.
4. Improve processes and data collection.

## Run it
    uv venv && uv pip install -r requirements.txt

Then run `notebooks/late_orders.ipynb`. It downloads the data itself via kagglehub.
