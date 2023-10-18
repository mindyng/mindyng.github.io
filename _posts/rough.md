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

