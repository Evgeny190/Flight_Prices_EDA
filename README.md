# Edmonton International Flight Price Analysis

An end-to-end junior data analytics portfolio project using Python and Google Flights data to explore two practical travel questions:

1. **When can a fixed flight itinerary be cheaper to book?**
2. **Which international destinations are cheapest from Edmonton for the same travel dates?**

## Project story

The project did not begin with a finished dataset. I built it iteratively:

1. Tested the Google Flights results available through SerpApi.
2. Collected historical price data for **Edmonton (YEG) → Mexico City (MEX)**.
3. Converted Unix timestamps into dates and calculated **days before departure**.
4. Tested the same historical-price idea for **YEG → Buenos Aires (EZE)**.
5. Expanded the project from booking timing to destination discovery.
6. Used airport metadata to create a regional search universe that produced **511 scheduled-service airports**.
7. Reduced that universe to **30 selected popular international/leisure destinations**.
8. Searched the 30 airports in batches for **November 23–December 5, 2026**.
9. Individually verified the 10 cheapest destinations.
10. Performed exploratory analysis on price, stops, duration, and airlines.

## Main findings

- Lowest observed YEG → MEX historical fare in the saved data: **CAD 651**.
- Observed YEG → EZE minimum: **CAD 1,218**, 130 days before departure.
- Cheapest individually verified destination for Nov 23–Dec 5: **Punta Cana — CAD 529 round trip**.
- Montego Bay (**CAD 544**) and Belize City (**CAD 550**) were close behind.
- The verified top-10 fares ranged from **CAD 529 to CAD 738**.
- Price alone did not capture travel convenience; some cheap options involved long itineraries or multiple stops.

## Skills demonstrated

- Python
- pandas
- NumPy
- Matplotlib
- REST API requests
- JSON parsing
- data cleaning
- feature engineering
- exploratory data analysis
- validation of search results
- communicating assumptions and limitations

## Repository structure

```text
flight_price_full_project/
├── Edmonton_Flight_Price_Analysis.ipynb
├── README.md
├── requirements.txt
├── .gitignore
├── assets/
│   └── yeg_eze_price_history_chart.png
└── data/
    ├── yeg_mex_price_history.csv
    ├── yeg_eze_observed_minimum.csv
    ├── selected_30_airports.csv
    └── verified_top10_flights.csv
```

## Data collection

Flight-search data was obtained through SerpApi's Google Flights results.

The notebook uses saved CSV snapshots for reproducibility. Live collection code is included, but the API key is intentionally not stored in the repository.

To use live API requests, set:

```text
SERPAPI_API_KEY=your_key_here
```

Never commit a real API key to GitHub.

## Limitations

- Airfares change frequently.
- Historical booking analysis currently covers only a small number of routes.
- The destination ranking uses one fixed vacation period.
- The 30 destinations were manually selected from a larger airport universe and are not a formal popularity ranking.
- Final destination EDA uses the verified top 10, so it is intentionally a selected sample.
- Baggage and other optional fees are not included.

## Next steps

- Collect prices daily.
- Add Calgary (YYC) as a second origin.
- Repeat the search for multiple travel windows.
- Analyze booking windows across many departures.
- Add return-flight duration, baggage cost, and total journey convenience.
- Build a Tableau or Power BI dashboard.
