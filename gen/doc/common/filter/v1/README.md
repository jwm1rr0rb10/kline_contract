# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [common/filter/v1/filter.proto](#common_filter_v1_filter-proto)
    - [ArrayFloatFieldFilter](#common-filter-v1-ArrayFloatFieldFilter)
    - [ArrayIntFieldFilter](#common-filter-v1-ArrayIntFieldFilter)
    - [ArrayStringFieldFilter](#common-filter-v1-ArrayStringFieldFilter)
    - [BoolFieldFilter](#common-filter-v1-BoolFieldFilter)
    - [FloatFieldFilter](#common-filter-v1-FloatFieldFilter)
    - [IntFieldFilter](#common-filter-v1-IntFieldFilter)
    - [Pagination](#common-filter-v1-Pagination)
    - [RangeIntFieldFilter](#common-filter-v1-RangeIntFieldFilter)
    - [RangeStringFieldFilter](#common-filter-v1-RangeStringFieldFilter)
    - [StringFieldFilter](#common-filter-v1-StringFieldFilter)
    - [StringNumberFieldFilter](#common-filter-v1-StringNumberFieldFilter)
  
    - [ArrayFloatFieldFilter.Operator](#common-filter-v1-ArrayFloatFieldFilter-Operator)
    - [ArrayIntFieldFilter.Operator](#common-filter-v1-ArrayIntFieldFilter-Operator)
    - [ArrayStringFieldFilter.Operator](#common-filter-v1-ArrayStringFieldFilter-Operator)
    - [BoolFieldFilter.Operator](#common-filter-v1-BoolFieldFilter-Operator)
    - [FloatFieldFilter.Operator](#common-filter-v1-FloatFieldFilter-Operator)
    - [IntFieldFilter.Operator](#common-filter-v1-IntFieldFilter-Operator)
    - [RangeIntFieldFilter.Operator](#common-filter-v1-RangeIntFieldFilter-Operator)
    - [RangeStringFieldFilter.Operator](#common-filter-v1-RangeStringFieldFilter-Operator)
    - [StringFieldFilter.Operator](#common-filter-v1-StringFieldFilter-Operator)
    - [StringNumberFieldFilter.Operator](#common-filter-v1-StringNumberFieldFilter-Operator)
  
- [common/filter/v1/sort.proto](#common_filter_v1_sort-proto)
    - [Sort](#common-filter-v1-Sort)
  
- [Scalar Value Types](#scalar-value-types)



<a name="common_filter_v1_filter-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## common/filter/v1/filter.proto



<a name="common-filter-v1-ArrayFloatFieldFilter"></a>

### ArrayFloatFieldFilter
Filter for array of int, example: ?price.op=in&amp;price.val=[18.33456, 3.14, 2.72].


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| op | [ArrayFloatFieldFilter.Operator](#common-filter-v1-ArrayFloatFieldFilter-Operator) |  |  |
| val | [float](#float) | repeated |  |






<a name="common-filter-v1-ArrayIntFieldFilter"></a>

### ArrayIntFieldFilter
Filter for array of int, example: ?age.op=in&amp;age.val=[10,20,30].


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| op | [ArrayIntFieldFilter.Operator](#common-filter-v1-ArrayIntFieldFilter-Operator) |  |  |
| val | [int64](#int64) | repeated |  |






<a name="common-filter-v1-ArrayStringFieldFilter"></a>

### ArrayStringFieldFilter
Filter for array of string, example: ?name.op=in&amp;name.val=[&#34;ok&#34;,&#34;not_ok&#34;,&#34;done&#34;].


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| op | [ArrayStringFieldFilter.Operator](#common-filter-v1-ArrayStringFieldFilter-Operator) |  |  |
| val | [string](#string) | repeated |  |






<a name="common-filter-v1-BoolFieldFilter"></a>

### BoolFieldFilter
Filter for bool values, example: ?exist.op=is&amp;email.val=true.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| op | [BoolFieldFilter.Operator](#common-filter-v1-BoolFieldFilter-Operator) |  |  |
| val | [bool](#bool) |  |  |






<a name="common-filter-v1-FloatFieldFilter"></a>

### FloatFieldFilter
Filter for float values, example: ?price.op=gt&amp;price.val=18.33456.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| op | [FloatFieldFilter.Operator](#common-filter-v1-FloatFieldFilter-Operator) |  |  |
| val | [float](#float) |  |  |






<a name="common-filter-v1-IntFieldFilter"></a>

### IntFieldFilter
Filter for int values, example: ?age.op=gt&amp;age.val=18.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| op | [IntFieldFilter.Operator](#common-filter-v1-IntFieldFilter-Operator) |  |  |
| val | [int64](#int64) |  |  |






<a name="common-filter-v1-Pagination"></a>

### Pagination



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| limit | [uint64](#uint64) |  |  |
| offset | [uint64](#uint64) |  |  |






<a name="common-filter-v1-RangeIntFieldFilter"></a>

### RangeIntFieldFilter
Filter for int range, example: ?price.op=range&amp;price.from=100&amp;price.to=1000.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| op | [RangeIntFieldFilter.Operator](#common-filter-v1-RangeIntFieldFilter-Operator) |  |  |
| from | [int64](#int64) |  |  |
| to | [int64](#int64) |  |  |






<a name="common-filter-v1-RangeStringFieldFilter"></a>

### RangeStringFieldFilter
Filter for string range, example: ?amount.op=range&amp;price.from=987.834&amp;price.to=3987.834.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| op | [RangeStringFieldFilter.Operator](#common-filter-v1-RangeStringFieldFilter-Operator) |  |  |
| from | [string](#string) |  |  |
| to | [string](#string) |  |  |






<a name="common-filter-v1-StringFieldFilter"></a>

### StringFieldFilter
Filter for string value, example: ?email.op=eq&amp;email.val=me@example.com.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| op | [StringFieldFilter.Operator](#common-filter-v1-StringFieldFilter-Operator) |  |  |
| val | [string](#string) |  |  |






<a name="common-filter-v1-StringNumberFieldFilter"></a>

### StringNumberFieldFilter
Filter for number as string (decimal) value, example: ?amount.op=gt&amp;email.val=123.456789.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| op | [StringNumberFieldFilter.Operator](#common-filter-v1-StringNumberFieldFilter-Operator) |  |  |
| val | [string](#string) |  |  |





 


<a name="common-filter-v1-ArrayFloatFieldFilter-Operator"></a>

### ArrayFloatFieldFilter.Operator


| Name | Number | Description |
| ---- | ------ | ----------- |
| OPERATOR_UNSPECIFIED | 0 |  |
| OPERATOR_IN | 1 |  |
| OPERATOR_NIN | 2 |  |



<a name="common-filter-v1-ArrayIntFieldFilter-Operator"></a>

### ArrayIntFieldFilter.Operator


| Name | Number | Description |
| ---- | ------ | ----------- |
| OPERATOR_UNSPECIFIED | 0 |  |
| OPERATOR_IN | 1 |  |
| OPERATOR_NIN | 2 |  |



<a name="common-filter-v1-ArrayStringFieldFilter-Operator"></a>

### ArrayStringFieldFilter.Operator


| Name | Number | Description |
| ---- | ------ | ----------- |
| OPERATOR_UNSPECIFIED | 0 |  |
| OPERATOR_IN | 1 |  |
| OPERATOR_NIN | 2 |  |



<a name="common-filter-v1-BoolFieldFilter-Operator"></a>

### BoolFieldFilter.Operator


| Name | Number | Description |
| ---- | ------ | ----------- |
| OPERATOR_UNSPECIFIED | 0 |  |
| OPERATOR_EQ | 1 |  |
| OPERATOR_NEQ | 2 |  |



<a name="common-filter-v1-FloatFieldFilter-Operator"></a>

### FloatFieldFilter.Operator


| Name | Number | Description |
| ---- | ------ | ----------- |
| OPERATOR_UNSPECIFIED | 0 |  |
| OPERATOR_EQ | 1 |  |
| OPERATOR_NEQ | 2 |  |
| OPERATOR_LT | 3 |  |
| OPERATOR_LTE | 4 |  |
| OPERATOR_GT | 5 |  |
| OPERATOR_GTE | 6 |  |



<a name="common-filter-v1-IntFieldFilter-Operator"></a>

### IntFieldFilter.Operator


| Name | Number | Description |
| ---- | ------ | ----------- |
| OPERATOR_UNSPECIFIED | 0 |  |
| OPERATOR_EQ | 1 |  |
| OPERATOR_NEQ | 2 |  |
| OPERATOR_LT | 3 |  |
| OPERATOR_LTE | 4 |  |
| OPERATOR_GT | 5 |  |
| OPERATOR_GTE | 6 |  |



<a name="common-filter-v1-RangeIntFieldFilter-Operator"></a>

### RangeIntFieldFilter.Operator


| Name | Number | Description |
| ---- | ------ | ----------- |
| OPERATOR_UNSPECIFIED | 0 |  |
| OPERATOR_RANGE | 1 |  |



<a name="common-filter-v1-RangeStringFieldFilter-Operator"></a>

### RangeStringFieldFilter.Operator


| Name | Number | Description |
| ---- | ------ | ----------- |
| OPERATOR_UNSPECIFIED | 0 |  |
| OPERATOR_RANGE | 1 |  |



<a name="common-filter-v1-StringFieldFilter-Operator"></a>

### StringFieldFilter.Operator


| Name | Number | Description |
| ---- | ------ | ----------- |
| OPERATOR_UNSPECIFIED | 0 |  |
| OPERATOR_EQ | 1 |  |
| OPERATOR_NEQ | 2 |  |
| OPERATOR_LIKE | 3 |  |
| OPERATOR_ILIKE | 4 |  |



<a name="common-filter-v1-StringNumberFieldFilter-Operator"></a>

### StringNumberFieldFilter.Operator


| Name | Number | Description |
| ---- | ------ | ----------- |
| OPERATOR_UNSPECIFIED | 0 |  |
| OPERATOR_EQ | 1 |  |
| OPERATOR_NEQ | 2 |  |
| OPERATOR_LT | 3 |  |
| OPERATOR_LTE | 4 |  |
| OPERATOR_GT | 5 |  |
| OPERATOR_GTE | 6 |  |


 

 

 



<a name="common_filter_v1_sort-proto"></a>
<p align="right"><a href="#top">Top</a></p>

## common/filter/v1/sort.proto



<a name="common-filter-v1-Sort"></a>

### Sort
Sorting array.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| field | [string](#string) |  |  |
| desc | [bool](#bool) |  |  |





 

 

 

 



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

