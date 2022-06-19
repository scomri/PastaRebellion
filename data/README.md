# SISE2601 Project data description
================
Team AN - Omri Sgan-cohen & Shahar Ben-Ishay

## This Markdown file describes the data folder structure and organization ...

--

# DOWNLOAD THE DATA FROM GOOGLE DRIVE LINK INTO THIS FOLDER IN ORDER TO RUN THE PROJECT ON THE DATA

This data folder contains 6 processed data sets.
The data preprocessing is available in the code repository, in the "data_preprocessing" RMD file. 
The preprocessing made was creating 6 data sets with the same features as the original data sets, but with the same Items in all of the different Retailers tables.

The data folder also contains a "raw_data" folder, where you can find the original data sets before the preprocessing.

--

Description of columns in the Prices tables:

+-----------------------------+--------------+--------------------------------------------+
| Column Name                 | Data Type    | Description                                 |
+=============================+==============+=============================================+
| Filename                    | character    | Original file name (without xml extension). |
+-----------------------------+--------------+---------------------------------------------+
| storeid                     | numeric      | ID of the store .                           |
+-----------------------------+--------------+---------------------------------------------+
| uploaddate                  | DateTime     | Date of file download.                      |
+-----------------------------+--------------+---------------------------------------------+
| PriceUpdateDate             | DateTime     | Last date of price change of the item.      |
+-----------------------------+--------------+---------------------------------------------+
| ItemCode                    | numeric      | A unique ID of the item.                    |
+-----------------------------+--------------+---------------------------------------------+
| ItemName                    | character    | The Item's name (in Hebrew).                |
+-----------------------------+--------------+---------------------------------------------+
| ManufacturerName            | character    | Name of the manufacturer of the item.       |
|                             |              | * This data is messy.                       |
+-----------------------------+--------------+---------------------------------------------+
| ManufactureCountry          | character    | Country of item's production.               |
+-----------------------------+--------------+---------------------------------------------+
| ManufacturerItemDescription | character    | Similar to ItemName.                        |
+-----------------------------+--------------+---------------------------------------------+
| UnitQty                     | character    | Unit of measure.                            |
+-----------------------------+--------------+---------------------------------------------+
| Quantity                    | numeric      | Quantity.                                   |
+-----------------------------+--------------+---------------------------------------------+
| UnitOfMeasure               | character    | Unit of measure, mostly by 100 units.       |
+-----------------------------+--------------+---------------------------------------------+
| ItemPrice                   | numeric      | Price in NIS.                               |
+-----------------------------+--------------+---------------------------------------------+
| UnitOfMeasurePrice          | numeric      | Price divided by quantity.                  |
+-----------------------------+--------------+---------------------------------------------+
| AllowDiscount               | numeric      | Boolean/dummy variable.                     |
+-----------------------------+--------------+---------------------------------------------+


Raw data skim:

Data Summary of tables:

> skim(OsherAdPrices)
── Data Summary ────────────────────────
                           Values       
Name                       OsherAdPrices
Number of rows             120859       
Number of columns          15           
_______________________                 
Column type frequency:                  
  character                8            
  Date                     1            
  numeric                  5            
  POSIXct                  1
________________________                
  
 > skim(ramiLeviPrices)
── Data Summary ────────────────────────
                           Values        
Name                       ramiLeviPrices
Number of rows             813291        
Number of columns          15            
_______________________                  
Column type frequency:                   
  character                8             
  Date                     1             
  numeric                  5             
  POSIXct                  1             
________________________

> skim(shufersalPrices)
── Data Summary ────────────────────────
                           Values         
Name                       shufersalPrices
Number of rows             7405456        
Number of columns          15             
_______________________                   
Column type frequency:                    
  character                8              
  Date                     1              
  numeric                  5              
  POSIXct                  1              
________________________

> skim(victoryPrices)
── Data Summary ────────────────────────
                           Values       
Name                       victoryPrices
Number of rows             594216       
Number of columns          15           
_______________________                 
Column type frequency:                  
  character                8            
  logical                  2            
  numeric                  5            
________________________

> skim(yenotBitanPrices)
── Data Summary ────────────────────────
                           Values          
Name                       yenotBitanPrices
Number of rows             346213          
Number of columns          15              
_______________________                    
Column type frequency:                     
  character                8               
  Date                     1               
  numeric                  5               
  POSIXct                  1               
________________________                   

> skim(YohananofPrices)
── Data Summary ────────────────────────
                           Values         
Name                       YohananofPrices
Number of rows             423491         
Number of columns          15             
_______________________                   
Column type frequency:                    
  character                8              
  Date                     1              
  numeric                  5              
  POSIXct                  1              
________________________                 


Description of columns in the stores tables:

+--------------------+------------+------------------------------------------------------+
| Column Name        | Data Type  | Description                                           |
+====================+============+=======================================================+
| ChainName          | character  | The retail chain the store belongs to.                |
+--------------------+------------+-------------------------------------------------------+
| SubChainid         | numeric    | The "type" (sub retail chain) the store belongs to.   |
+--------------------+------------+-------------------------------------------------------+
| SubChainName       | character  | The store's name (mainly neighborhood and city).      |
+--------------------+------------+-------------------------------------------------------+
| StoreId            | character  | A unique ID of the store (as part of a retail chain). |
+--------------------+------------+-------------------------------------------------------+
| StoreName          | character  | The store's name (mainly neighborhood and city).      |
+--------------------+------------+-------------------------------------------------------+
| Address            | character  | Store's address.                                      |
+--------------------+------------+-------------------------------------------------------+
| City               | character  | The city where the store is in.                       |
+--------------------+------------+-------------------------------------------------------+
| Zipcode            | character  | Stor'es zipcode.                                      |
+--------------------+------------+-------------------------------------------------------+

> skim(stores_all)
── Data Summary ────────────────────────
                           Values    
Name                       stores_all
Number of rows             749       
Number of columns          8         
_______________________              
Column type frequency:               
  character                7         
  numeric                  1         
________________________ 
