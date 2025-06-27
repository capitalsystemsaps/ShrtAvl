The data is recorded from the Binance REST API.

date - The END time of the 5-minute bar when the data has been retrieved and recorded
ready - The time when the info for all symbols has been retrieved for the current bar
symbol - The trade-able pair symbol (asset & quote asset, e.g. BTCUSDT)
asset - the underlaying base asset (e.g. BTC)
statusTrading - 1 if the Exchange info "status" for the symbol is: "TRADING", 0 otherwise
spotTrading - Spot Trading Allowed
marginTrading - Margin Trading Allowed for the asset (base asset e.g. BTC)
isBorrowable - The asset can be borrowed	
isMortgageable - The asset can be mortgaged
isMarginTrade - Margin Trading Allowed for the symbol (pair e.g. BTCUSDT)
isAvailable: Base asset is available to borrow. Can have the following values:
	1: there is availability for borrowing
	0: there is no availability for borrowing, 0 has been returned
	-1: there is no availability, error -3045 and 'The system does not have enough assets...' has been returned
	-2: data could not be retrieved in time
	-3: the api call returned an unexpected error

If any value is "NULL", than the data was not provided by the API (not present in the response).