# Buy and Sell a Stock Once

**Question**
Given an array of stock prices throughout the day, find the maximum profit that can be gained from buying and selling the
stock onces. Buying and selling must be in cronological order. 

```python
def profit(array):
    minimum_price_seen = array[0]
    max_difference = 0

    for price in array:
        minimum_price_seen = min(price, minimum_price_seen)
        max_difference = max(max_difference, (price - minimum_price_seen))

    return max_difference
```