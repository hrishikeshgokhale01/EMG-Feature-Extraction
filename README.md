# EMG-Feature-Extraction
Extract features from EMG signals using Python.

## Features being extracted:

1. RMS: Calculates the root mean square of the data, which is the square root of the mean of the
squared values of the data.
2. Histogram: Computes the histogram of the data with a specified number of bins (default is 20). It
returns a tuple containing the histogram values and the bin edges.
3. Entropy: Calculates the entropy of the data. It first estimates the probability density function (PDF)
using a histogram with 20 bins and then computes the entropy of the PDF.
4. Kurtosis: Computes the kurtosis of the data, which is a measure of the "tailedness" or
"peakedness" of the data distribution.
5. Zero Cross: Counts the number of zero crossings in the data array. It calculates the number of times
the data changes sign (from positive to negative or vice versa).
6. Min and Max: Returns the minimum and maximum values of the data.
7. Mean: Calculates the arithmetic mean (average) of the data.
8. Median: Computes the median of the data, which is the middle value when the data is sorted.
9. FFT: Computes the discrete Fourier transform (DFT) of the data using NumPy’s fft function.
10. PSD: Calculates the power spectral density (PSD) of the data by taking the squared magnitude of
the Fourier transform.

## Cepstral features being extracted:

1. Spectral roll-off point: Computes the frequency below which a specified percentage of the total
spectral energy lies in the given data. It uses the cumulative sum of the sorted power spectral
density values to find the roll-off frequency.
2. Spectral Flatness: Calculates the spectral flatness of a given data array by finding the ratio of the
geometric mean to the arithmetic mean of the power spectral density (PSD) values, expressed in
decibels (dB). It measures how "flat" or "peaked" the spectrum is, with higher values indicating a
more uniform frequency distribution.
3. Spectral Crust: Calculates the frequency below which a specified percentage of the total spectral
energy lies in the given data array, using the cumulative distribution of the power spectral density. It
returns the crust frequency based on the cumulative distribution exceeding the specified crust
percentage.
4. Spectral Decrease: Calculates the spectral decrease of a given data array by finding the negative
average of the derivative of the logarithmically transformed power spectral density. It quantifies the
rate at which the spectral energy decreases with increasing frequency.
5. Spectral slope: Calculates the spectral slope of a given data array by computing the power spectral
density (PSD) using the Fourier transform and performing linear regression on the frequencies and
PSD values. The resulting slope coefficient indicates the rate at which the spectral energy changes
with increasing frequency.
6. Spectral Spread: Calculates the spectral spread of a given data array by fitting a linear regression
model to the power spectral density (PSD) values and frequencies. It quantifies the spread of the
spectral energy around the regression line, representing the bandwidth of the spectrum.
