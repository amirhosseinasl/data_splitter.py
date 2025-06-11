# data_splitter.py
train test split(Data)
# 🧪 data_splitter.py

A simple and practical utility for splitting datasets into training and testing sets — with support for **deterministic hashing-based splitting** using stable identifiers.

## 📦 Features

- ✅ Random shuffle-based splitting (like `sklearn.model_selection.train_test_split`)
- ✅ Deterministic, stable test/train split based on hashing
- ✅ Ideal for ML pipelines that need reproducibility
- ✅ Utility to create unique identifiers from coordinates (lat/lon)

---

## 🛠️ Functions

### `shuffle_and_split_df(df, test_ratio=0.2, seed=42)`
Splits a DataFrame randomly into training and testing sets.

### `split_train_test_by_id(df, test_ratio, id_column)`
Deterministically splits the DataFrame using hash of a unique ID column.

### `is_identifier_in_test_set(identifier, test_ratio)`
Internal function to determine if an identifier belongs to the test set using `crc32`.

### `generate_identifier_from_coords(df, lat_col='latitude', lon_col='longitude', id_col='identifier')`
Creates a numerical identifier from geographic coordinates.

---

## 📌 Example
