# MAIZE PREDICTION SYSTEM FOR KENYA

This repository includes a Plotly Dash v1.5 dashboard and Python forecasting API for
county-level maize production in all 47 counties of Kenya. It accepts
historical CSV data and Excel workbooks, including the supplied
county/year/indicator/value maize workbook format. It forecasts from observed
production, not invented data.

See [maize_prediction/README.md](maize_prediction/README.md) for setup,
the CSV schema, training and forecast API instructions, and tests.

The [Render Blueprint](render.yaml) deploys the Dash dashboard and API as a
single Python web service. The dashboard is served at `/`, while the API
documentation is at `/docs`. Source is bundled in
[maize_prediction_system.zip](maize_prediction_system.zip) for Render; the
source archive does not include the workbook or a trained model. After
deploying, train the API with the workbook. The free service does not persist
its trained model across restarts, so re-upload it if the service restarts.
