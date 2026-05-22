# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [kline_service/v1/model.proto](#kline_service_v1_model-proto)
    - [Kline](#kline_service-v1-Kline)
  
- [kline_service/v1/request.proto](#kline_service_v1_request-proto)
    - [SearchKlineRequest](#kline_service-v1-SearchKlineRequest)
  
- [kline_service/v1/response.proto](#kline_service_v1_response-proto)
    - [SearchKlineResponse](#kline_service-v1-SearchKlineResponse)
  
- [kline_service/v1/service.proto](#kline_service_v1_service-proto)
    - [KlineService](#kline_service-v1-KlineService)
  
- [Scalar Value Types](#scalar-value-types)



<a name="kline_service_v1_model-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## kline_service/v1/model.proto



<a name="kline_service-v1-Kline"></a>

### Kline



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| kline_id | [string](#string) |  | UUIDv7. |
| symbol | [string](#string) |  | Trading pair symbol, e.g. BTCUSDT, ETHUSDT. |
| interval | [string](#string) |  | Kline/candlestick interval (timeframe), e.g. 1m, 5m, 15m, 1h, 4h, 1d. |
| start_time | [google.protobuf.Timestamp](#google-protobuf-Timestamp) |  | Start time of the kline (opening time). |
| close_time | [google.protobuf.Timestamp](#google-protobuf-Timestamp) |  | Close time of the kline. |
| open_price | [string](#string) |  | Opening price. Stored as string to avoid floating-point precision issues. |
| close_price | [string](#string) |  | Closing price. |
| high_price | [string](#string) |  | Highest price during the interval. |
| low_price | [string](#string) |  | Lowest price during the interval. |
| base_asset_volume | [string](#string) |  | Trading volume in base asset (e.g. amount of BTC traded). |
| quote_asset_volume | [string](#string) |  | Trading volume in quote asset (e.g. amount of USDT traded). |





 

 

 

 



<a name="kline_service_v1_request-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## kline_service/v1/request.proto



<a name="kline_service-v1-SearchKlineRequest"></a>

### SearchKlineRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| pagination | [common.filter.v1.Pagination](#common-filter-v1-Pagination) |  | Pagination parameters. |
| sort | [common.filter.v1.Sort](#common-filter-v1-Sort) |  | Sorting options. |
| search | [string](#string) | optional | Search query. |
| kline_id_val | [common.filter.v1.StringFieldFilter](#common-filter-v1-StringFieldFilter) |  | Filter for id. |
| symbol_val | [common.filter.v1.StringFieldFilter](#common-filter-v1-StringFieldFilter) |  | Filter for symbol. |
| interval_val | [common.filter.v1.StringFieldFilter](#common-filter-v1-StringFieldFilter) |  | Filter for interval. |
| open_price_val | [common.filter.v1.StringNumberFieldFilter](#common-filter-v1-StringNumberFieldFilter) |  | Filter for open_price. |
| close_price_val | [common.filter.v1.StringNumberFieldFilter](#common-filter-v1-StringNumberFieldFilter) |  | Filter for close_price. |
| high_price_val | [common.filter.v1.StringNumberFieldFilter](#common-filter-v1-StringNumberFieldFilter) |  | Filter for high_price. |
| low_price_val | [common.filter.v1.StringNumberFieldFilter](#common-filter-v1-StringNumberFieldFilter) |  | Filter for low_price. |
| base_asset_volume_val | [common.filter.v1.StringNumberFieldFilter](#common-filter-v1-StringNumberFieldFilter) |  | Filter for base_asset_volume. |
| quote_asset_volume_val | [common.filter.v1.StringNumberFieldFilter](#common-filter-v1-StringNumberFieldFilter) |  | Filter for quote_asset_volume. |
| with_count | [bool](#bool) |  | Total count of all kline in response. |





 

 

 

 



<a name="kline_service_v1_response-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## kline_service/v1/response.proto



<a name="kline_service-v1-SearchKlineResponse"></a>

### SearchKlineResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| items | [Kline](#kline_service-v1-Kline) | repeated |  |
| count | [uint64](#uint64) | optional |  |





 

 

 

 



<a name="kline_service_v1_service-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## kline_service/v1/service.proto


 

 

 


<a name="kline_service-v1-KlineService"></a>

### KlineService


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| SearchKline | [SearchKlineRequest](#kline_service-v1-SearchKlineRequest) | [SearchKlineResponse](#kline_service-v1-SearchKlineResponse) |  |

 



## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |

