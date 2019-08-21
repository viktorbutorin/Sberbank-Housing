# Sberbank Russian Housing Market
This is intitial data cleaning and preparation of the Kaggle Sberbank Russian Housing Market dataset. 

51 of 292 or 17% of variables in the dataset have NaN values. Furthermore, list_price which is target variable, is artificially low in ~10% of entries.

Steps involved in data cleaning include:

1) Removing almost 90% of entries in Tverskoe district - those were most probably assigned to geographical centre of Moscow due to lack of real location provided.
2) Finding median for sub_area price_m2 for each year due to change in economic situation in 2011-2015. 
3) Updating price of listings with artificially low price
4) Filling missing "full_sq", "floor", "num_room", values
5) Splitting build_year variable into three: 1955-1997, 1997-2011, 2011-2015
6) Splitting kitch_sq variable into two: <5m and >5m
7) Changing product_type variable to binary investment_type
8) Dropping several variables

Next steps: run PCA for secondary variebles, merge with economic data dataset, find appropriate split for sub_area variable
