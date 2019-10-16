# MBTdelay
MBTdelay builds machine learning models using LightGBM to calculate delay forecasting on the MBTA's Green Line. 

### Note: 10/15/2019
There have been recent issues with GitHub rendering Jupyter notebooks. If a notebook fails to load and gives the message "Sorry, something went wrong. Reload?", the notebook is still viewable using [https://nbviewer.jupyter.org](https://nbviewer.jupyter.org/). Apologies for the inconvenience.

### Prerequisites

Everything was built in Python 3.7.4.

Need to ``pip install``

```
arrow, io, flask, lightgbm, numpy, pandas, pickle, requests, sklearn, matplotlib
```

## Outline

To build dataset and models, MBTdelay's workflow is as follows:

``get_stations_and_weather.ipynb`` gets station names for current line from MBTA provided stop list (``DATA/GreenLineDStops.csv``).

``headway.ipynb`` gets headway timing data and saves to file -- needs API key from MBTA performance: [here](https://www.mbta.com/developers/mbta-performance)

``fenway_events.ipynb`` cleans and organizes web-scraped events at Fenway Park.

``build_datasets.ipynb`` combines all data into modeling-ready format.

``model_LinearRegression.ipynb`` contains the model training and saving for the linear regression model (used as machine learning baseline)

``model_LightGBM.ipynb`` contains the model training and saving for the LightGBM model.

## Author
* **Mark Mace** - [email](mailto:mark.f.mace@gmail.com) - [GitHub](https://github.com/markfmace) - [Website](https://mbtdelay.xyz)

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## License
MIT License

Copyright (c) 2019 Mark Mace

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
