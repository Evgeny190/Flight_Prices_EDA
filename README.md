# Flight Price EDA — Edmonton to Popular International Destinations

A junior data analytics portfolio project exploring round-trip flight prices from **Edmonton (YEG)** for **November 23 to December 5, 2026**.

## Project objective

The goal is to compare a shortlist of popular destinations in Central America, South America, the Caribbean, and Iceland and identify lower-cost travel options for the same dates.

I first searched 30 popular airport destinations and then verified the 10 cheapest results individually. The repository contains the verified top-10 snapshot used in the analysis.

## Questions explored

- Which destinations have the lowest round-trip fares?
- How large is the spread between the cheapest and most expensive options?
- Do lower fares require more stops?
- Is price related to outbound itinerary duration?
- Which airlines appear most often in the cheapest group?
- What limitations should be considered before making a travel decision?

## Tools

- Python
- pandas
- NumPy
- Matplotlib
- requests / JSON
- Jupyter Notebook
- SerpApi / Google Flights results

## Repository structure

```text
flight_price_portfolio/
├── Flight_Price_EDA.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── data/
    └── verified_top10_flights.csv
```

## Main findings

- Punta Cana was the cheapest verified option at **CAD 529 round trip**.
- Montego Bay (**CAD 544**) and Belize City (**CAD 550**) were close behind.
- The verified top-10 fares ranged from **CAD 529 to CAD 738**.
- The cheapest fare was also a nonstop outbound itinerary, but the sample is too small to conclude that nonstop flights are generally cheaper.
- Price alone does not capture convenience: some low-cost options involved long itineraries and multiple stops.

## Data notes

The CSV is a saved price snapshot, not a live fare feed. Flight prices can change rapidly.

The main analysis uses the saved CSV so the notebook can be viewed and run without an API key. An appendix demonstrates how the data can be collected through SerpApi without exposing credentials.

## How to run

1. Clone or download this repository.
2. Install the packages:

```bash
pip install -r requirements.txt
```

3. Open `Flight_Price_EDA.ipynb` in JupyterLab or VS Code.
4. Run the notebook from top to bottom.

## Optional live API use

If you want to run live SerpApi requests, set the environment variable:

```text
SERPAPI_API_KEY=your_key_here
```

Do not commit your real API key to GitHub.

## Limitations

- One fixed travel period.
- Only the verified top 10 from a selected list of 30 destinations.
- Prices are dynamic.
- Outbound stops and duration describe the returned outbound itinerary; the fare is round trip.
- The sample is exploratory and is not sufficient for predictive airfare modeling.

## Next steps

- Collect prices daily.
- Calculate days before departure.
- Compare Edmonton with Calgary.
- Repeat the analysis across multiple travel dates.
- Build a Tableau or Power BI dashboard.
- Explore fare prediction only after collecting a much larger historical dataset.
