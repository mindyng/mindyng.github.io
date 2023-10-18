```
# breaking up order creation into different data components
def extract_date_features(data):
    data['created_at'] = pd.to_datetime(data['created_at']) 
    
    data['hour'] = data['created_at'].dt.hour
    data["day"] = data['created_at'].dt.day
    data['day_of_week'] = data['created_at'].dt.day_of_week.astype(int)
    data['is_weekend'] = np.where(data['day_of_week'].isin([5, 6]), 1, 0)
    data["month"] = data['created_at'].dt.month
    data["quarter"] = data['created_at'].dt.quarter
    data["is_month_start"] = data['created_at'].dt.is_month_start.astype(int)
    data["is_month_end"] = data['created_at'].dt.is_month_end.astype(int)
    data["is_quarter_start"] = data['created_at'].dt.is_quarter_start.astype(int)
    data["is_quarter_end"] = data['created_at'].dt.is_quarter_end.astype(int)
#     data["year"] = data['created_at'].dt.year
#     data["is_year_start"] = data['created_at'].dt.is_year_start.astype(int)
#     data["is_year_end"] = data['created_at'].dt.is_year_end.astype(int)
extract_date_features(data)
data.head()
```

```
# Imput string 'NA', not Null's...

query = """
select total_items
, estimated_order_place_duration
, store_id
, max_item_price
, num_distinct_items
, min_item_price
, subtotal
, hour
, day
, day_of_week
, is_weekend
, month
, quarter
, is_month_start
, is_month_end
, is_quarter_start
, is_quarter_end
, if(total_outstanding_orders = 'NA', 33, total_outstanding_orders) as total_outstanding_orders
, if(total_onshift_dashers = 'NA', 4, total_onshift_dashers) as total_onshift_dashers
, if(total_busy_dashers = 'NA', 41, total_busy_dashers) as total_busy_dashers
, if(store_primary_category = 'NA', 'american', store_primary_category) as store_primary_category
, if(order_protocol = 'NA', 1, order_protocol) as order_protocol
, if(market_id = 'NA', 2, market_id) as market_id
, if(estimated_store_to_consumer_driving_duration = 'NA', 535, estimated_store_to_consumer_driving_duration) as estimated_store_to_consumer_driving_duration
from df2
"""

df2 = duckdb.query(query).df()
df2
```
