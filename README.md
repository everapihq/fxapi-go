<p align="center">
<img src="https://app.currencyapi.com/img/logo/currencyapi.png" width="300"/>
</p>

# fxapi-go: Golang Currency Converter

This package is a Golang wrapper for [fxapi.com](https://fxapi.com) that aims to make the usage of the API as easy as possible in your project.

## Usage

Initialize the API with your API Key (get one for free at [fxapi.com]):

```go
fxapi.Init("YOUR-API-KEY")
```

Afterwards you can make calls to the API like this:

### Status Endpoint

```go
fxapi.Status()
```

### Currencies Endpoint

```go
fxapi.Currencies()
```

### Latest Endpoint

```go
fxapi.Latest({
    "base_currency": "USD",
    "currencies": "EUR"
})
```

### Historical Endpoint

```go
fxapi.Historical({
    "base_currency": "USD",
    "currencies": "EUR",
	"date": "2022-09-04"
})
```

### Conversion Endpoint *

```go
fxapi.Convert({
    "base_currency": "USD",
    "currencies": "EUR",
	"date": "2022-09-04",
	"value": "1"
})
```

### Range Endpoint *

```go
fxapi.Range({
    "base_currency": "USD",
    "currencies": "EUR",
	"datetime_start": "2022-09-01T23:59:59Z",
	"datetime_end": "2022-09-03T23:59:59Z",
	"accuracy": "day"
})
```

(*) Requires paid subscription

Find out more about our endpoints, parameters and response data structure in the [docs](https://fxapi.com/docs)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[docs]: https://fxapi.com/docs
[fxapi.com]: https://fxapi.com
