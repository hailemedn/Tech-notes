# Total data throughput comparison

## Netact
Abhinav -> monthly report -> total throughput -> configure slotwise, 8 days -> export

## Columns to add inside excel

### Throughput
=(ulMaxMbps + d1MaxMbps) / 1000

### Date
=INT(A3)
- A3 -> value of Period start time

### time
=MOD(A3,1)

Select the whole sheet (ctrl + A) -> insert -> pivotTable -> New Document

## PivotTable Fields

### under values
- Throughput

### under Rows
- date
- time

