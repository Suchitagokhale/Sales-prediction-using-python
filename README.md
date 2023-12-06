{
 "cells": [
 
  {
  
   "cell_type": "markdown",
   
   "id": "5803d41f",
   
   "metadata": {},
   
   "source": [
   
    "# Import Necessary Libraries "
    
   ]
   
  },
  
  {
   "cell_type": "code",
   
   "execution_count": 1,
   
   "id": "ce0e0753",
   
   "metadata": {},
   
   "outputs": [],
   
   "source": [
   
    "import numpy as np  #linear algebra\n",
    
    "import pandas as pd  #data processing "
    
   ]
   
  },
  
  {
  
   "cell_type": "markdown",
   
   "id": "d6b68367",
   
   "metadata": {},
   
   "source": [
   
    "# Reading CSV File"
    
   ]
  },
  
  {
   "cell_type": "code",
   
   "execution_count": 2,
   
   "id": "3b4f31a2",
   
   "metadata": {},
   
   "outputs": [],
   
   "source": [
   
    "df=pd.read_csv(\"Advertising.csv\")  #read dataset"
    
   ]
   
  },
  
  {
  
   "cell_type": "code",
   
   "execution_count": 3,
   
   "id": "20cdff1e",
   
   "metadata": {},
   
   "outputs": [
   
    {
     "data": {
     
      "text/html": [
      
       "<div>\n",
       
       "<style scoped>\n",
       
       "    .dataframe tbody tr th:only-of-type {\n",
       
       "        vertical-align: middle;\n",
       
       "    }\n",
       
       "\n",
       
       "    .dataframe tbody tr th {\n",
       
       "        vertical-align: top;\n",
       
       "    }\n",
       
       "\n",
       
       "    .dataframe thead th {\n",
       
       "        text-align: right;\n",
       
       "    }\n",
       
       "</style>\n",
       
       "<table border=\"1\" class=\"dataframe\">\n",
       
       "  <thead>\n",
       
       "    <tr style=\"text-align: right;\">\n",
       
       "      <th></th>\n",
       
       "      <th>Unnamed: 0</th>\n",
       
       "      <th>TV</th>\n",
       
       "      <th>Radio</th>\n",
       
       "      <th>Newspaper</th>\n",
       
       "      <th>Sales</th>\n",
       
       "    </tr>\n",
       
       "  </thead>\n",
       
       "  <tbody>\n",
       
       "    <tr>\n",
       
       "      <th>0</th>\n",
       
       "      <td>1</td>\n",
       
       "      <td>230.1</td>\n",
       
       "      <td>37.8</td>\n",
       
       "      <td>69.2</td>\n",
       
       "      <td>22.1</td>\n",
       
       "    </tr>\n",
       
       "    <tr>\n",
       
       "      <th>1</th>\n",
       
       "      <td>2</td>\n",
       
       "      <td>44.5</td>\n",
       
       "      <td>39.3</td>\n",
       
       "      <td>45.1</td>\n",
       
       "      <td>10.4</td>\n",
       
       "    </tr>\n",
       
       "    <tr>\n",
       
       "      <th>2</th>\n",
       
       "      <td>3</td>\n",
       
       "      <td>17.2</td>\n",
       
       "      <td>45.9</td>\n",
       
       "      <td>69.3</td>\n",
       
       "      <td>9.3</td>\n",
       "    </tr>\n",
       
       "    <tr>\n",
       
       "      <th>3</th>\n",
       
       "      <td>4</td>\n",
       
       "      <td>151.5</td>\n",
       
       "      <td>41.3</td>\n",
       
       "      <td>58.5</td>\n",
       
       "      <td>18.5</td>\n",
       
       "    </tr>\n",
       
       "    <tr>\n",
       
       "      <th>4</th>\n",
       
       
       "      <td>5</td>\n",
       "      <td>180.8</td>\n",
       
       "      <td>10.8</td>\n",
       
       "      <td>58.4</td>\n",
       
       "      <td>12.9</td>\n",
       
       "    </tr>\n",
       
       "  </tbody>\n",
       
       "</table>\n",
       
       "</div>"
       
      ],
      "text/plain": [
      
       "   Unnamed: 0     TV  Radio  Newspaper  Sales\n",
       "0           1  230.1   37.8       69.2   22.1\n",
       "1           2   44.5   39.3       45.1   10.4\n",
       "2           3   17.2   45.9       69.3    9.3\n",
       "3           4  151.5   41.3       58.5   18.5\n",
       "4           5  180.8   10.8       58.4   12.9"
      ]
     },
     
     "execution_count": 3,
     
     "metadata": {},
     
     "output_type": "execute_result"
     
    }
   ],
   "source": [
   
    "df.head()  #returns first 5 entries"
    
   ]
  },
  {
   "cell_type": "code",
   
   "execution_count": 4,
   
   "id": "0398f5f8",
   
   "metadata": {},
   
   "outputs": [
   
    {
    
     "data": {
     
      "text/html": [
      
       "<div>\n",
       
       
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       
       "        vertical-align: middle;\n",
       
       "    }\n",
       
       "\n",

       
       "    .dataframe tbody tr th {\n",
       
       "        vertical-align: top;\n",
       
       "    }\n",
       
       "\n",
       
       /
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       
       /
       "    }\n",
       "</style>\n",
       
       "<table border=\"1\" class=\"dataframe\">\n",
       
       "  <thead>\n",
       
       "    <tr style=\"text-align: right;\">\n",
       
       "      <th></th>\n",
       
       "      <th>Unnamed: 0</th>\n",
       
       "      <th>TV</th>\n",
       
       "      <th>Radio</th>\n",
       
       "      <th>Newspaper</th>\n",
       
       "      <th>Sales</th>\n",
       
       "    </tr>\n",
       
       "  </thead>\n",
       
       "  <tbody>\n",
       
       "    <tr>\n",
       
       "      <th>195</th>\n",
       
       "      <td>196</td>\n",

       
       "      <td>38.2</td>\n",
       
       "      <td>3.7</td>\n",
       
       "      <td>13.8</td>\n",
       
       "      <td>7.6</td>\n",
       
       "    </tr>\n",
       
       "    <tr>\n",
       
       "      <th>196</th>\n",
       
       "      <td>197</td>\n",
       
       "      <td>94.2</td>\n",
       
       "      <td>4.9</td>\n",
       
       "      <td>8.1</td>\n",
       
       "      <td>9.7</td>\n",
       
       "    </tr>\n",
       
       "    <tr>\n",
       
       "      <th>197</th>\n",
       
       "      <td>198</td>\n",
       
       "      <td>177.0</td>\n",
       
       "      <td>9.3</td>\n",
       
       
       "      <td>6.4</td>\n",
       "      <td>12.8</td>\n",
       
       "    </tr>\n",
       
       "    <tr>\n",
       
       "      <th>198</th>\n",
       
       "      <td>199</td>\n",
       
       "      <td>283.6</td>\n",
       
       "      <td>42.0</td>\n",

       
       "      <td>66.2</td>\n",
       
       "      <td>25.5</td>\n",
       
       "    </tr>\n",
       
       "    <tr>\n",
       
       "      <th>199</th>\n",
       
       "      <td>200</td>\n",
       
       "      <td>232.1</td>\n",
       
       "      <td>8.6</td>\n",
       
       "      <td>8.7</td>\n",
       
       "      <td>13.4</td>\n",
       
       "    </tr>\n",
       
       "  </tbody>\n",
       
       "</table>\n",
       
       "</div>"
       
      ],
      
      "text/plain": [
       "     Unnamed: 0     TV  Radio  Newspaper  Sales\n",
       "195         196   38.2    3.7       13.8    7.6\n",
       "196         197   94.2    4.9        8.1    9.7\n",
       "197         198  177.0    9.3        6.4   12.8\n",
       "198         199  283.6   42.0       66.2   25.5\n",
       "199         200  232.1    8.6        8.7   13.4"
      ]
     },
     
     "execution_count": 4,
     
     "metadata": {},
     
     "output_type": "execute_result"
     
    }
   ],
   "source": [
    "df.tail()  #returns last 5 entries"
    
   ]
  },
  
  {
  
   "cell_type": "code",
   
   "execution_count": 5,
   
   "id": "2744cac3",
   
   "metadata": {},
   
   "outputs": [
   
    {
    
     "data": {
     
      "text/plain": [
      
       "(200, 5)"
       
      ]
      
     },
     
     "execution_count": 5,
     
     "metadata": {},
     
     "output_type": "execute_result"
     
    }
    
   ],
   
   "source": [
   
    "#returns tuple of shape (Rows, columns) of dataframe\n",
    
    "df.shape"
    
   ]
   
  },
  
  {
  
  / "cell_type": "code",
  
   "execution_count": 6,
   
   "id": "9171bd17",
   

   
   "metadata": {},
   
   "outputs": [
   
    {
    
     "name": "stdout",
     
     "output_type": "stream",
     
     "text": [
     
      "<class 'pandas.core.frame.DataFrame'>\n",
      
      "RangeIndex: 200 entries, 0 to 199\n",
      
      "Data columns (total 5 columns):\n",
      
      " #   Column      Non-Null Count  Dtype  \n",
      
      "---  ------      --------------  -----  \n",
      
      " 0   Unnamed: 0  200 non-null    int64  \n",
      
      " 1   TV          200 non-null    float64\n",
      
      " 2   Radio       200 non-null    float64\n",
      
      " 3   Newspaper   200 non-null    float64\n",
      
      " 4   Sales       200 non-null    float64\n",
      
      "dtypes: float64(4), int64(1)\n",
      
      "memory usage: 7.9 KB\n"
      
     ]
     
    }
   ],
   
   "source": [
   
    "#prints information about the dataframe\n",
    
    "df.info()"
    
   ]
   
  },
  
  {
  
   "cell_type": "code",
   
   "execution_count": 7,
   
   
   "id": "9a65def3",
   "metadata": {},
   
   "outputs": [
   
    {
     "data": {
     
      "text/html": [
      
       "<div>\n",
       
       "<style scoped>\n",
       
       "    .dataframe tbody tr th:only-of-type {\n",
       
       "        vertical-align: middle;\n",
       
       "    }\n",
       
       "\n",
       
       "    .dataframe tbody tr th {\n",
       
       "        vertical-align: top;\n",
       
       "    }\n",
       
       "\n",
       
       "    .dataframe thead th {\n",
       
       "        text-align: right;\n",
       
       "    }\n",
       
       "</style>\n",
       
       "<table border=\"1\" class=\"dataframe\">\n",
       
       "  <thead>\n",
       
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Unnamed: 0</th>\n",
       "      <th>TV</th>\n",
       "      <th>Radio</th>\n",
       "      <th>Newspaper</th>\n",
       "      <th>Sales</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>count</th>\n",
       "      <td>200.000000</td>\n",
       "      <td>200.000000</td>\n",
       "      <td>200.000000</td>\n",
       "      <td>200.000000</td>\n",
       "      <td>200.000000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>mean</th>\n",
       "      <td>100.500000</td>\n",
       "      <td>147.042500</td>\n",
       "      <td>23.264000</td>\n",
       "      <td>30.554000</td>\n",
       "      <td>14.022500</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>std</th>\n",
       "      <td>57.879185</td>\n",
       "      <td>85.854236</td>\n",
       "      <td>14.846809</td>\n",
       "      <td>21.778621</td>\n",
       "      <td>5.217457</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>min</th>\n",
       "      <td>1.000000</td>\n",
       "      <td>0.700000</td>\n",
       "      <td>0.000000</td>\n",
       "      <td>0.300000</td>\n",
       "      <td>1.600000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>25%</th>\n",
       "      <td>50.750000</td>\n",
       "      <td>74.375000</td>\n",
       "      <td>9.975000</td>\n",
       "      <td>12.750000</td>\n",
       "      <td>10.375000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>50%</th>\n",
       "      <td>100.500000</td>\n",
       "      <td>149.750000</td>\n",
       "      <td>22.900000</td>\n",
       "      <td>25.750000</td>\n",
       "      <td>12.900000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>75%</th>\n",
       "      <td>150.250000</td>\n",
       "      <td>218.825000</td>\n",
       "      <td>36.525000</td>\n",
       "      <td>45.100000</td>\n",
       "      <td>17.400000</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>max</th>\n",
       "      <td>200.000000</td>\n",
       "      <td>296.400000</td>\n",
       "      <td>49.600000</td>\n",
       "      <td>114.000000</td>\n",
       "      <td>27.000000</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       Unnamed: 0          TV       Radio   Newspaper       Sales\n",
       "count  200.000000  200.000000  200.000000  200.000000  200.000000\n",
       "mean   100.500000  147.042500   23.264000   30.554000   14.022500\n",
       "std     57.879185   85.854236   14.846809   21.778621    5.217457\n",
       "min      1.000000    0.700000    0.000000    0.300000    1.600000\n",
       "25%     50.750000   74.375000    9.975000   12.750000   10.375000\n",
       "50%    100.500000  149.750000   22.900000   25.750000   12.900000\n",
       "75%    150.250000  218.825000   36.525000   45.100000   17.400000\n",
       "max    200.000000  296.400000   49.600000  114.000000   27.000000"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#returns numerical description of the data in the dataframe\n",
    "df.describe()"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "8fcf2924",
   "metadata": {},
   "source": [
    "# Droping the Column "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "id": "6e52b76f",
   "metadata": {},
   "outputs": [],
   "source": [
    "#dropping the column 'Unnamed: 0'\n",
    "df=df.drop(columns=[\"Unnamed: 0\"])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "id": "5b9c87cf",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>TV</th>\n",
       "      <th>Radio</th>\n",
       "      <th>Newspaper</th>\n",
       "      <th>Sales</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>230.1</td>\n",
       "      <td>37.8</td>\n",
       "      <td>69.2</td>\n",
       "      <td>22.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>44.5</td>\n",
       "      <td>39.3</td>\n",
       "      <td>45.1</td>\n",
       "      <td>10.4</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>17.2</td>\n",
       "      <td>45.9</td>\n",
       "      <td>69.3</td>\n",
       "      <td>9.3</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>151.5</td>\n",
       "      <td>41.3</td>\n",
       "      <td>58.5</td>\n",
       "      <td>18.5</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>180.8</td>\n",
       "      <td>10.8</td>\n",
       "      <td>58.4</td>\n",
       "      <td>12.9</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>195</th>\n",
       "      <td>38.2</td>\n",
       "      <td>3.7</td>\n",
       "      <td>13.8</td>\n",
       "      <td>7.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>196</th>\n",
       "      <td>94.2</td>\n",
       "      <td>4.9</td>\n",
       "      <td>8.1</td>\n",
       "      <td>9.7</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>197</th>\n",
       "      <td>177.0</td>\n",
       "      <td>9.3</td>\n",
       "      <td>6.4</td>\n",
       "      <td>12.8</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>198</th>\n",
       "      <td>283.6</td>\n",
       "      <td>42.0</td>\n",
       "      <td>66.2</td>\n",
       "      <td>25.5</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>199</th>\n",
       "      <td>232.1</td>\n",
       "      <td>8.6</td>\n",
       "      <td>8.7</td>\n",
       "      <td>13.4</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>200 rows × 4 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "        TV  Radio  Newspaper  Sales\n",
       "0    230.1   37.8       69.2   22.1\n",
       "1     44.5   39.3       45.1   10.4\n",
       "2     17.2   45.9       69.3    9.3\n",
       "3    151.5   41.3       58.5   18.5\n",
       "4    180.8   10.8       58.4   12.9\n",
       "..     ...    ...        ...    ...\n",
       "195   38.2    3.7       13.8    7.6\n",
       "196   94.2    4.9        8.1    9.7\n",
       "197  177.0    9.3        6.4   12.8\n",
       "198  283.6   42.0       66.2   25.5\n",
       "199  232.1    8.6        8.7   13.4\n",
       "\n",
       "[200 rows x 4 columns]"
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "df  #return dataframe"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "id": "d2bb5f6a",
   "metadata": {},
   "outputs": [],
   "source": [
    "x=df.iloc[:, 0:-1]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "id": "103f5aea",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>TV</th>\n",
       "      <th>Radio</th>\n",
       "      <th>Newspaper</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>230.1</td>\n",
       "      <td>37.8</td>\n",
       "      <td>69.2</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>44.5</td>\n",
       "      <td>39.3</td>\n",
       "      <td>45.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>17.2</td>\n",
       "      <td>45.9</td>\n",
       "      <td>69.3</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>151.5</td>\n",
       "      <td>41.3</td>\n",
       "      <td>58.5</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>180.8</td>\n",
       "      <td>10.8</td>\n",
       "      <td>58.4</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>195</th>\n",
       "      <td>38.2</td>\n",
       "      <td>3.7</td>\n",
       "      <td>13.8</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>196</th>\n",
       "      <td>94.2</td>\n",
       "      <td>4.9</td>\n",
       "      <td>8.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>197</th>\n",
       "      <td>177.0</td>\n",
       "      <td>9.3</td>\n",
       "      <td>6.4</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>198</th>\n",
       "      <td>283.6</td>\n",
       "      <td>42.0</td>\n",
       "      <td>66.2</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>199</th>\n",
       "      <td>232.1</td>\n",
       "      <td>8.6</td>\n",
       "      <td>8.7</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>200 rows × 3 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "        TV  Radio  Newspaper\n",
       "0    230.1   37.8       69.2\n",
       "1     44.5   39.3       45.1\n",
       "2     17.2   45.9       69.3\n",
       "3    151.5   41.3       58.5\n",
       "4    180.8   10.8       58.4\n",
       "..     ...    ...        ...\n",
       "195   38.2    3.7       13.8\n",
       "196   94.2    4.9        8.1\n",
       "197  177.0    9.3        6.4\n",
       "198  283.6   42.0       66.2\n",
       "199  232.1    8.6        8.7\n",
       "\n",
       "[200 rows x 3 columns]"
      ]
     },
     "execution_count": 11,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "x"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "id": "43454178",
   "metadata": {},
   "outputs": [],
   "source": [
    "y=df.iloc[:,-1]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "id": "b3aa473b",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0      22.1\n",
       "1      10.4\n",
       "2       9.3\n",
       "3      18.5\n",
       "4      12.9\n",
       "       ... \n",
       "195     7.6\n",
       "196     9.7\n",
       "197    12.8\n",
       "198    25.5\n",
       "199    13.4\n",
       "Name: Sales, Length: 200, dtype: float64"
      ]
     },
     "execution_count": 13,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "y"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "8ad81cff",
   "metadata": {},
   "source": [
    "# Train Test Split"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "id": "cbcdcde6",
   "metadata": {},
   "outputs": [],
   "source": [
    "from sklearn.model_selection import train_test_split\n",
    "x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=43)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "id": "8e2c0b20",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>TV</th>\n",
       "      <th>Radio</th>\n",
       "      <th>Newspaper</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>116</th>\n",
       "      <td>139.2</td>\n",
       "      <td>14.3</td>\n",
       "      <td>25.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>138</th>\n",
       "      <td>43.0</td>\n",
       "      <td>25.9</td>\n",
       "      <td>20.5</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>155</th>\n",
       "      <td>4.1</td>\n",
       "      <td>11.6</td>\n",
       "      <td>5.7</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>82</th>\n",
       "      <td>75.3</td>\n",
       "      <td>20.3</td>\n",
       "      <td>32.5</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>160</th>\n",
       "      <td>172.5</td>\n",
       "      <td>18.1</td>\n",
       "      <td>30.7</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>58</th>\n",
       "      <td>210.8</td>\n",
       "      <td>49.6</td>\n",
       "      <td>37.7</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>21</th>\n",
       "      <td>237.4</td>\n",
       "      <td>5.1</td>\n",
       "      <td>23.5</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>49</th>\n",
       "      <td>66.9</td>\n",
       "      <td>11.7</td>\n",
       "      <td>36.8</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>64</th>\n",
       "      <td>131.1</td>\n",
       "      <td>42.8</td>\n",
       "      <td>28.9</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>68</th>\n",
       "      <td>237.4</td>\n",
       "      <td>27.5</td>\n",
       "      <td>11.0</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>160 rows × 3 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "        TV  Radio  Newspaper\n",
       "116  139.2   14.3       25.6\n",
       "138   43.0   25.9       20.5\n",
       "155    4.1   11.6        5.7\n",
       "82    75.3   20.3       32.5\n",
       "160  172.5   18.1       30.7\n",
       "..     ...    ...        ...\n",
       "58   210.8   49.6       37.7\n",
       "21   237.4    5.1       23.5\n",
       "49    66.9   11.7       36.8\n",
       "64   131.1   42.8       28.9\n",
       "68   237.4   27.5       11.0\n",
       "\n",
       "[160 rows x 3 columns]"
      ]
     },
     "execution_count": 15,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "x_train"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 16,
   "id": "e0ce61c9",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>TV</th>\n",
       "      <th>Radio</th>\n",
       "      <th>Newspaper</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>56</th>\n",
       "      <td>7.3</td>\n",
       "      <td>28.1</td>\n",
       "      <td>41.4</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>37</th>\n",
       "      <td>74.7</td>\n",
       "      <td>49.4</td>\n",
       "      <td>45.7</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>67</th>\n",
       "      <td>139.3</td>\n",
       "      <td>14.5</td>\n",
       "      <td>10.2</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>79</th>\n",
       "      <td>116.0</td>\n",
       "      <td>7.7</td>\n",
       "      <td>23.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>80</th>\n",
       "      <td>76.4</td>\n",
       "      <td>26.7</td>\n",
       "      <td>22.3</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>188</th>\n",
       "      <td>286.0</td>\n",
       "      <td>13.9</td>\n",
       "      <td>3.7</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>183</th>\n",
       "      <td>287.6</td>\n",
       "      <td>43.0</td>\n",
       "      <td>71.8</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>10</th>\n",
       "      <td>66.1</td>\n",
       "      <td>5.8</td>\n",
       "      <td>24.2</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>128</th>\n",
       "      <td>220.3</td>\n",
       "      <td>49.0</td>\n",
       "      <td>3.2</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>62</th>\n",
       "      <td>239.3</td>\n",
       "      <td>15.5</td>\n",
       "      <td>27.3</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>65</th>\n",
       "      <td>69.0</td>\n",
       "      <td>9.3</td>\n",
       "      <td>0.9</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>17</th>\n",
       "      <td>281.4</td>\n",
       "      <td>39.6</td>\n",
       "      <td>55.8</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>133</th>\n",
       "      <td>219.8</td>\n",
       "      <td>33.5</td>\n",
       "      <td>45.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>195</th>\n",
       "      <td>38.2</td>\n",
       "      <td>3.7</td>\n",
       "      <td>13.8</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>146</th>\n",
       "      <td>240.1</td>\n",
       "      <td>7.3</td>\n",
       "      <td>8.7</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>38</th>\n",
       "      <td>43.1</td>\n",
       "      <td>26.7</td>\n",
       "      <td>35.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>173</th>\n",
       "      <td>168.4</td>\n",
       "      <td>7.1</td>\n",
       "      <td>12.8</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>149</th>\n",
       "      <td>44.7</td>\n",
       "      <td>25.8</td>\n",
       "      <td>20.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>93</th>\n",
       "      <td>250.9</td>\n",
       "      <td>36.5</td>\n",
       "      <td>72.3</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>29</th>\n",
       "      <td>70.6</td>\n",
       "      <td>16.0</td>\n",
       "      <td>40.8</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>230.1</td>\n",
       "      <td>37.8</td>\n",
       "      <td>69.2</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>17.2</td>\n",
       "      <td>45.9</td>\n",
       "      <td>69.3</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>122</th>\n",
       "      <td>224.0</td>\n",
       "      <td>2.4</td>\n",
       "      <td>15.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>180</th>\n",
       "      <td>156.6</td>\n",
       "      <td>2.6</td>\n",
       "      <td>8.3</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>95</th>\n",
       "      <td>163.3</td>\n",
       "      <td>31.6</td>\n",
       "      <td>52.9</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>121</th>\n",
       "      <td>18.8</td>\n",
       "      <td>21.7</td>\n",
       "      <td>50.4</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>185</th>\n",
       "      <td>205.0</td>\n",
       "      <td>45.1</td>\n",
       "      <td>19.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>39</th>\n",
       "      <td>228.0</td>\n",
       "      <td>37.7</td>\n",
       "      <td>32.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>66</th>\n",
       "      <td>31.5</td>\n",
       "      <td>24.6</td>\n",
       "      <td>2.2</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>19</th>\n",
       "      <td>147.3</td>\n",
       "      <td>23.9</td>\n",
       "      <td>19.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>11</th>\n",
       "      <td>214.7</td>\n",
       "      <td>24.0</td>\n",
       "      <td>4.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>45</th>\n",
       "      <td>175.1</td>\n",
       "      <td>22.5</td>\n",
       "      <td>31.5</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>41</th>\n",
       "      <td>177.0</td>\n",
       "      <td>33.4</td>\n",
       "      <td>38.7</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>92</th>\n",
       "      <td>217.7</td>\n",
       "      <td>33.5</td>\n",
       "      <td>59.0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>168</th>\n",
       "      <td>215.4</td>\n",
       "      <td>23.6</td>\n",
       "      <td>57.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>44.5</td>\n",
       "      <td>39.3</td>\n",
       "      <td>45.1</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>57</th>\n",
       "      <td>136.2</td>\n",
       "      <td>19.2</td>\n",
       "      <td>16.6</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>189</th>\n",
       "      <td>18.7</td>\n",
       "      <td>12.1</td>\n",
       "      <td>23.4</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>151</th>\n",
       "      <td>121.0</td>\n",
       "      <td>8.4</td>\n",
       "      <td>48.7</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>167</th>\n",
       "      <td>206.8</td>\n",
       "      <td>5.2</td>\n",
       "      <td>19.4</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "        TV  Radio  Newspaper\n",
       "56     7.3   28.1       41.4\n",
       "37    74.7   49.4       45.7\n",
       "67   139.3   14.5       10.2\n",
       "79   116.0    7.7       23.1\n",
       "80    76.4   26.7       22.3\n",
       "188  286.0   13.9        3.7\n",
       "183  287.6   43.0       71.8\n",
       "10    66.1    5.8       24.2\n",
       "128  220.3   49.0        3.2\n",
       "62   239.3   15.5       27.3\n",
       "65    69.0    9.3        0.9\n",
       "17   281.4   39.6       55.8\n",
       "133  219.8   33.5       45.1\n",
       "195   38.2    3.7       13.8\n",
       "146  240.1    7.3        8.7\n",
       "38    43.1   26.7       35.1\n",
       "173  168.4    7.1       12.8\n",
       "149   44.7   25.8       20.6\n",
       "93   250.9   36.5       72.3\n",
       "29    70.6   16.0       40.8\n",
       "0    230.1   37.8       69.2\n",
       "2     17.2   45.9       69.3\n",
       "122  224.0    2.4       15.6\n",
       "180  156.6    2.6        8.3\n",
       "95   163.3   31.6       52.9\n",
       "121   18.8   21.7       50.4\n",
       "185  205.0   45.1       19.6\n",
       "39   228.0   37.7       32.0\n",
       "66    31.5   24.6        2.2\n",
       "19   147.3   23.9       19.1\n",
       "11   214.7   24.0        4.0\n",
       "45   175.1   22.5       31.5\n",
       "41   177.0   33.4       38.7\n",
       "92   217.7   33.5       59.0\n",
       "168  215.4   23.6       57.6\n",
       "1     44.5   39.3       45.1\n",
       "57   136.2   19.2       16.6\n",
       "189   18.7   12.1       23.4\n",
       "151  121.0    8.4       48.7\n",
       "167  206.8    5.2       19.4"
      ]
     },
     "execution_count": 16,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "x_test"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "id": "ce62320d",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "116    12.2\n",
       "138     9.6\n",
       "155     3.2\n",
       "82     11.3\n",
       "160    14.4\n",
       "       ... \n",
       "58     23.8\n",
       "21     12.5\n",
       "49      9.7\n",
       "64     18.0\n",
       "68     18.9\n",
       "Name: Sales, Length: 160, dtype: float64"
      ]
     },
     "execution_count": 17,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "y_train"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "id": "72c25124",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "56      5.5\n",
       "37     14.7\n",
       "67     13.4\n",
       "79     11.0\n",
       "80     11.8\n",
       "188    15.9\n",
       "183    26.2\n",
       "10      8.6\n",
       "128    24.7\n",
       "62     15.7\n",
       "65      9.3\n",
       "17     24.4\n",
       "133    19.6\n",
       "195     7.6\n",
       "146    13.2\n",
       "38     10.1\n",
       "173    11.7\n",
       "149    10.1\n",
       "93     22.2\n",
       "29     10.5\n",
       "0      22.1\n",
       "2       9.3\n",
       "122    11.6\n",
       "180    10.5\n",
       "95     16.9\n",
       "121     7.0\n",
       "185    22.6\n",
       "39     21.5\n",
       "66      9.5\n",
       "19     14.6\n",
       "11     17.4\n",
       "45     14.9\n",
       "41     17.1\n",
       "92     19.4\n",
       "168    17.1\n",
       "1      10.4\n",
       "57     13.2\n",
       "189     6.7\n",
       "151    11.6\n",
       "167    12.2\n",
       "Name: Sales, dtype: float64"
      ]
     },
     "execution_count": 18,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "y_test"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "id": "d89f8196",
   "metadata": {},
   "outputs": [],
   "source": [
    "x_train=x_train.astype(int)\n",
    "y_train=y_train.astype(int)\n",
    "x_test=x_test.astype(int)\n",
    "y_test=y_test.astype(int)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "id": "177fc550",
   "metadata": {},
   "outputs": [],
   "source": [
    "from sklearn.preprocessing import StandardScaler\n",
    "Sc=StandardScaler()\n",
    "x_train_scaled=Sc.fit_transform(x_train)\n",
    "x_test_scaled=Sc.fit_transform(x_test)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "9cac2107",
   "metadata": {},
   "source": [
    "# Applying Linear Regression "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "id": "6a67dc42",
   "metadata": {},
   "outputs": [],
   "source": [
    "from sklearn.linear_model import LinearRegression"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 22,
   "id": "3a9b79b0",
   "metadata": {},
   "outputs": [],
   "source": [
    "lr=LinearRegression()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "id": "41438645",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<style>#sk-container-id-1 {color: black;background-color: white;}#sk-container-id-1 pre{padding: 0;}#sk-container-id-1 div.sk-toggleable {background-color: white;}#sk-container-id-1 label.sk-toggleable_label {cursor: pointer;display: block;width: 100%;margin-bottom: 0;padding: 0.3em;box-sizing: border-box;text-align: center;}#sk-container-id-1 label.sk-toggleablelabel-arrow:before {content: \"▸\";float: left;margin-right: 0.25em;color: #696969;}#sk-container-id-1 label.sk-toggleablelabel-arrow:hover:before {color: black;}#sk-container-id-1 div.sk-estimator:hover label.sk-toggleablelabel-arrow:before {color: black;}#sk-container-id-1 div.sk-toggleablecontent {max-height: 0;max-width: 0;overflow: hidden;text-align: left;background-color: #f0f8ff;}#sk-container-id-1 div.sk-toggleablecontent pre {margin: 0.2em;color: black;border-radius: 0.25em;background-color: #f0f8ff;}#sk-container-id-1 input.sk-toggleablecontrol:checked~div.sk-toggleablecontent {max-height: 200px;max-width: 100%;overflow: auto;}#sk-container-id-1 input.sk-toggleablecontrol:checked~label.sk-toggleablelabel-arrow:before {content: \"▾\";}#sk-container-id-1 div.sk-estimator input.sk-toggleablecontrol:checked~label.sk-toggleablelabel {background-color: #d4ebff;}#sk-container-id-1 div.sk-label input.sk-toggleablecontrol:checked~label.sk-toggleablelabel {background-color: #d4ebff;}#sk-container-id-1 input.sk-hidden--visually {border: 0;clip: rect(1px 1px 1px 1px);clip: rect(1px, 1px, 1px, 1px);height: 1px;margin: -1px;overflow: hidden;padding: 0;position: absolute;width: 1px;}#sk-container-id-1 div.sk-estimator {font-family: monospace;background-color: #f0f8ff;border: 1px dotted black;border-radius: 0.25em;box-sizing: border-box;margin-bottom: 0.5em;}#sk-container-id-1 div.sk-estimator:hover {background-color: #d4ebff;}#sk-container-id-1 div.sk-parallel-item::after {content: \"\";width: 100%;border-bottom: 1px solid gray;flex-grow: 1;}#sk-container-id-1 div.sk-label:hover label.sk-toggleable_label {background-color: #d4ebff;}#sk-container-id-1 div.sk-serial::before {content: \"\";position: absolute;border-left: 1px solid gray;box-sizing: border-box;top: 0;bottom: 0;left: 50%;z-index: 0;}#sk-container-id-1 div.sk-serial {display: flex;flex-direction: column;align-items: center;background-color: white;padding-right: 0.2em;padding-left: 0.2em;position: relative;}#sk-container-id-1 div.sk-item {position: relative;z-index: 1;}#sk-container-id-1 div.sk-parallel {display: flex;align-items: stretch;justify-content: center;background-color: white;position: relative;}#sk-container-id-1 div.sk-item::before, #sk-container-id-1 div.sk-parallel-item::before {content: \"\";position: absolute;border-left: 1px solid gray;box-sizing: border-box;top: 0;bottom: 0;left: 50%;z-index: -1;}#sk-container-id-1 div.sk-parallel-item {display: flex;flex-direction: column;z-index: 1;position: relative;background-color: white;}#sk-container-id-1 div.sk-parallel-item:first-child::after {align-self: flex-end;width: 50%;}#sk-container-id-1 div.sk-parallel-item:last-child::after {align-self: flex-start;width: 50%;}#sk-container-id-1 div.sk-parallel-item:only-child::after {width: 0;}#sk-container-id-1 div.sk-dashed-wrapped {border: 1px dashed gray;margin: 0 0.4em 0.5em 0.4em;box-sizing: border-box;padding-bottom: 0.4em;background-color: white;}#sk-container-id-1 div.sk-label label {font-family: monospace;font-weight: bold;display: inline-block;line-height: 1.2em;}#sk-container-id-1 div.sk-label-container {text-align: center;}#sk-container-id-1 div.sk-container {/* jupyter's normalize.less sets [hidden] { display: none; } but bootstrap.min.css set [hidden] { display: none !important; } so we also need the !important here to be able to override the default hidden behavior on the sphinx rendered scikit-learn.org. See: https://github.com/scikit-learn/scikit-learn/issues/21755 */display: inline-block !important;position: relative;}#sk-container-id-1 div.sk-text-repr-fallback {display: none;}</style><div id=\"sk-container-id-1\" class=\"sk-top-container\"><div class=\"sk-text-repr-fallback\"><pre>LinearRegression()</pre><b>In a Jupyter environment, please rerun this cell to show the HTML representation or trust the notebook. <br />On GitHub, the HTML representation is unable to render, please try loading this page with nbviewer.org.</b></div><div class=\"sk-container\" hidden><div class=\"sk-item\"><div class=\"sk-estimator sk-toggleable\"><input class=\"sk-toggleable_control sk-hidden--visually\" id=\"sk-estimator-id-1\" type=\"checkbox\" checked><label for=\"sk-estimator-id-1\" class=\"sk-toggleablelabel sk-toggleablelabel-arrow\">LinearRegression</label><div class=\"sk-toggleable_content\"><pre>LinearRegression()</pre></div></div></div></div></div>"
      ],
      "text/plain": [
       "LinearRegression()"
      ]
     },
     "execution_count": 23,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "lr.fit(x_train_scaled,y_train)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "id": "6138d837",
   "metadata": {},
   "outputs": [],
   "source": [
    "y_pred=lr.predict(x_test_scaled)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "efe7366f",
   "metadata": {},
   "source": [
    "# Evaluate the performance of a Linear Regerssion Model"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 25,
   "id": "c1e94067",
   "metadata": {},
   "outputs": [],
   "source": [
    "from sklearn.metrics import r2_score"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 26,
   "id": "68eddf7f",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0.9222988021105912"
      ]
     },
     "execution_count": 26,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "r2_score(y_test,y_pred)"
   ]
  },
  {
   "cell_type": "markdown",
   "id": "826e5cdb",
   "metadata": {},
   "source": [
    "# Analyzing Data By Scatter Plot"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 27,
   "id": "ef9a3718",
   "metadata": {},
   "outputs": [],
   "source": [
    "import matplotlib.pyplot as plt"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "id": "0ea974d1",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "<matplotlib.collections.PathCollection at 0x264fd918810>"
      ]
     },
     "execution_count": 28,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "iVBORw0KGgoAAAANSUhEUgAAAiwAAAGdCAYAAAAxCSikAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjYuMywgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy/P9b71AAAACXBIWXMAAA9hAAAPYQGoP6dpAAAzNElEQVR4nO3df3DUdX7H8dc3KwTPywbDj/xgNwT8AZwKttTLoa4HhSOb61AgRpTzTvA4nVqwiYhnuakC1Rlar9dJHDmddk6xY+EuZBb8UZspcgTiCFyVY5ROZCAXzG8U2uwmUSKz++0fdrdudhPYZH98N3k+Ot8Z9/v97Jf3zk5uX/18Pz8M0zRNAQAAWFhGqgsAAAC4HAILAACwPAILAACwPAILAACwPAILAACwPAILAACwPAILAACwPAILAACwvKtSXUA8BAIBdXR0KCsrS4ZhpLocAABwBUzTVE9PjwoKCpSRMXQfyqgILB0dHXI6nakuAwAADENra6scDseQbUZFYMnKypL01Qe22+0prgYAAFwJn88np9MZ+h0fyqgILMHHQHa7ncACAECauZLhHAy6BQAAlkdgAQAAlkdgAQAAlkdgAQAAlkdgAQAAlkdgAQAAlkdgAQAAlkdgAQAAljcqFo4DAACJ4Q/41dDSoM6eTuVn5ctV6JItw5b0OggsAAAgKk+jRxV1FWrztYXOOewOVburVTanLKm18EgIAABE8DR6VF5THhZWJKnd167ymnJ5Gj1JrYfAAgAAwvgDflXUVciUGXEteK6yrlL+gD9pNRFYAABAmIaWhoiela8zZarV16qGloak1URgAQAAYTp7OuPaLh4ILAAAIEx+Vn5c28UDgQUAAIRxFbrksDtkyIh63ZAhp90pV6EraTURWAAAQBhbhk3V7mpJiggtwddV7qqkrsdCYAEAABHK5pSpdlWtptmnhZ132B2qXVWb9HVYDNM0I+cspRmfz6fs7Gx5vV7Z7fZUlwMAwKiRyJVuY/n9ZqVbAAAwKFuGTQuLFqa6DB4JAQAA6yOwAAAAyyOwAAAAyyOwAAAAyyOwAAAAyyOwAAAAyyOwAAAAy2MdFgAAkiyRi7GNVgQWAACSyNPoUUVdhdp8baFzDrtD1e7qpC93n054JAQAQJJ4Gj0qrykPCyuS1O5rV3lNuTyNnhRVZn0EFgAAksAf8KuirkKmIrfwC56rrKuUP+BPdmlpgcACAEASNLQ0RPSsfJ0pU62+VjW0NCSxqvQRU2DZvn27brvtNmVlZWnq1KlasWKFTp06Fbr+3//933r00Uc1a9YsXX311SosLNRf/dVfyev1DnnftWvXyjCMsMPtdg/vEwEAYEGdPZ1xbTfWxBRYDh06pPXr1+vo0aPav3+/Ll26pKVLl6qvr0+S1NHRoY6ODv3DP/yDTp48qZ07d6qurk7r1q277L3dbrc6OztDx+7du4f3iQAAsKD8rPy4thtrDNM0Ix+mXaHPPvtMU6dO1aFDh3TXXXdFbbNnzx798Ic/VF9fn666KvqkpLVr16q7u1v79u0bVh0+n0/Z2dnyer2y2+3DugcAAInkD/hVVF2kdl971HEshgw57A41VzSPmSnOsfx+j2gMS/BRT05OzpBt7Hb7oGElqL6+XlOnTtWsWbP0yCOP6MKFC4O27e/vl8/nCzsAALAyW4ZN1e5qSV+Fk68Lvq5yV42ZsBKrYQeWQCCgyspK3XHHHbr55pujtjl//ryeeeYZPfzww0Pey+1261/+5V904MAB/f3f/70OHTqk0tJS+f3RR0pv375d2dnZocPpdA73YwAAkDRlc8pUu6pW0+zTws477A7VrqplHZYhDPuR0COPPKJ///d/17vvviuHwxFx3efz6Xvf+55ycnL0xhtvaNy4cVd87z/84Q+67rrr9M4772jx4sUR1/v7+9Xf3x/2bzmdTh4JAQDSAivdfiWWR0LDWul2w4YNeuutt3T48OGoYaWnp0dut1tZWVnau3dvTGFFkmbOnKnJkyfrzJkzUQNLZmamMjMzh1M6AAApZ8uwaWHRwlSXkVZiCiymaerRRx/V3r17VV9frxkzZkS08fl8KikpUWZmpt544w1NmDAh5qLa2tp04cIF5eczUhoAMPrQwxK7mMawrF+/Xq+99pp27dqlrKwsdXV1qaurS1988YWkr8JKcJrzr371K/l8vlCbr49HmT17tvbu3StJ6u3t1RNPPKGjR4/q7NmzOnDggJYvX67rr79eJSUlcfyoAACknqfRo6LqIi16dZF+4PmBFr26SEXVRSzLfxkxjWExDCPq+VdeeUVr165VfX29Fi1aFLVNc3OzioqKQvcJvueLL77QihUr9Pvf/17d3d0qKCjQ0qVL9cwzzyg3N/eK6mJaMwAgHQT3Eho4rTk4S2isDbyN5fd7ROuwWAWBBQBgdcF1WAZbnp91WBK4DgsAALgy7CU0MgQWAACSgL2ERobAAgBAErCX0MgQWAAASAJXoUsOuyNiWf4gQ4acdqdcha4kV5YeCCwAACQBewmNDIEFAIAkYS+h4WNaMwAAScZKt19J+F5CAABg+NhLKHY8EgIAAJZHYAEAAJZHYAEAAJZHYAEAAJZHYAEAAJZHYAEAAJZHYAEAAJZHYAEAAJZHYAEAAJZHYAEAAJZHYAEAAJbHXkIAgFGBDQVHNwILACDteRo9qqirUJuvLXTOYXeo2l2tsjllKawM8cIjIQBAWvM0elReUx4WViSp3deu8ppyeRo9KaoM8URgAQCkLX/Ar4q6CpkyI64Fz1XWVcof8Ce7NMQZgQUAkLYaWhoiela+zpSpVl+rGloaklgVEoHAAgBIW509nXFtB+sisAAA0tbUa6bGtR2si8ACAAAsj8ACAEhbn/Z9Gtd2sC4CCwAgbeVn5ce1HayLwAIASFuuQpccdocMGVGvGzLktDvlKnQluTLEG4EFAJC2bBk2VburJSkitARfV7mrWKJ/FCCwAADSWtmcMtWuqtW0rGlh56fZp6l2VS1L848SMQWW7du367bbblNWVpamTp2qFStW6NSpU2FtLl68qPXr12vSpEn65je/qbvvvlvnzp0b8r6maerpp59Wfn6+rr76ai1ZskSnT5+O/dMAANKCP+BX/dl67f5ot+rP1sdlJdqBq92aZuTqt0hfMQWWQ4cOaf369Tp69Kj279+vS5cuaenSperr6wu1eeyxx/Tmm29qz549OnTokDo6OlRWNnS6fe655/T888/rpZde0rFjx3TNNdeopKREFy9eHN6nAgBYlqfRo6LqIi16dZF+4PmBFr26SEXVRcPe8ye4l1B7T3vY+Y6eDvYSGkUMcwQR9LPPPtPUqVN16NAh3XXXXfJ6vZoyZYp27dql8vJySdLHH3+sOXPm6MiRI/rOd74TcQ/TNFVQUKDHH39cmzZtkiR5vV7l5uZq586duu+++y5bh8/nU3Z2trxer+x2+3A/DgAgwYLhYmBvSHC8SayPcPwBv4qqiwZdnt+QIYfdoeaKZsaxWFAsv98jGsPi9XolSTk5OZKkDz74QJcuXdKSJUtCbWbPnq3CwkIdOXIk6j2am5vV1dUV9p7s7GwVFxcP+p7+/n75fL6wAwBgbYnYqJC9hMaOYQeWQCCgyspK3XHHHbr55pslSV1dXRo/frwmTpwY1jY3N1ddXV1R7xM8n5ube8Xv2b59u7Kzs0OH0+kc7scAACRJIsIFewmNHcMOLOvXr9fJkyf161//Op71XJHNmzfL6/WGjtbW1qTXAACITSLCBQvHjR3DCiwbNmzQW2+9pYMHD8rhcITO5+Xl6csvv1R3d3dY+3PnzikvLy/qvYLnB84kGuo9mZmZstvtYQcAwNoSES5YOG7siCmwmKapDRs2aO/evfrtb3+rGTNmhF2fP3++xo0bpwMHDoTOnTp1Si0tLVqwYEHUe86YMUN5eXlh7/H5fDp27Nig7wEApJ9EhAsWjhs7Ygos69ev12uvvaZdu3YpKytLXV1d6urq0hdffCHpq8Gy69at08aNG3Xw4EF98MEHevDBB7VgwYKwGUKzZ8/W3r17JUmGYaiyslLPPvus3njjDX300Ud64IEHVFBQoBUrVsTvkwIAUipR4SK0cJw9fOE4h93BwnGjSEzTmg0jeip+5ZVXtHbtWklfLRz3+OOPa/fu3erv71dJSYl++ctfhj3eMQwj7D2maWrLli36p3/6J3V3d+vOO+/UL3/5S914441XVBfTmgEgfXgaPaqoqwgbgOu0O1XlrhpRuPAH/GpoaVBnT6fys/LlKnTRs2Jxsfx+j2gdFqsgsABAeiFcQIrt9/uqJNUEAECILcOmhUULU10G0gibHwIAAMsjsAAAAMsjsAAAAMsjsAAAAMsjsAAAAMsjsAAAAMsjsAAAAMsjsAAAAMsjsAAAAMsjsAAAAMtjaX4AGCXYnwejGYEFAEaBaDsgO+wOVburR7QDMmAVPBICgDTnafSovKY8LKxIUpuvTeU15fI0elJUGRA/BBYASGP+gF8VdRUyZUa9bspUZV2l/AF/kisD4ovAAgBprKGlIaJnZaBWX6saWhqSVBGQGAQWAEhj7b72uLYDrIrAAgBp7LPPP4trO8CqCCwAkMamfGNKXNsBVkVgAYA0Ns0+La7tAKsisABAGnMVuuSwO4Zs47Q75Sp0JakiIDEILACQxmwZNlW7q2X83/99XfBclbuKFW+R9ggsAJDmyuaUqXZVbcRjH4fdodpVtax0i1HBME0z+mpDacTn8yk7O1ter1d2uz3V5QBASrCXENJNLL/f7CUEAKOELcOmhUULU10GkBA8EgIAAJZHYAEAAJZHYAEAAJZHYAEAAJbHoFsAScdsFgCxIrAASCpPo0cVdRVq87WFzjnsDlW7q1kvBMCgeCQEIGk8jR6V15SHhRVJave1q7ymXJ5GT4oqA2B1MQeWw4cPa9myZSooKJBhGNq3b1/YdcMwoh4///nPB73n1q1bI9rPnj075g8DwLr8Ab8q6ipkKnKtyuC5yrpK+QP+ZJcGIA3EHFj6+vo0b9487dixI+r1zs7OsOPll1+WYRi6++67h7zvTTfdFPa+d999N9bSAFhYQ0tDRM/K15ky1eprVUNLQxKrApAuYh7DUlpaqtLS0kGv5+Xlhb1+/fXXtWjRIs2cOXPoQq66KuK9AEaPzp7OuLYDMLYkdAzLuXPn9G//9m9at27dZduePn1aBQUFmjlzpu6//361tLQM2ra/v18+ny/sAGBt+Vn5cW0HYGxJaGB59dVXlZWVpbKyoUf+FxcXa+fOnaqrq9OLL76o5uZmuVwu9fT0RG2/fft2ZWdnhw6n05mI8gHEkavQJYfdIUNG1OuGDDntTrkKXUmuDEA6SGhgefnll3X//fdrwoQJQ7YrLS3VPffco7lz56qkpERvv/22uru7VVNTE7X95s2b5fV6Q0dra2siygcQR7YMm6rd1ZIUEVqCr6vcVazHAiCqhAWWhoYGnTp1Sj/5yU9ifu/EiRN144036syZM1GvZ2Zmym63hx0ArK9sTplqV9Vqmn1a2HmH3aHaVbWswwJgUAlbOO5Xv/qV5s+fr3nz5sX83t7eXjU1NelHP/pRAioDkEplc8q0fNZyVroFEJOYA0tvb29Yz0dzc7NOnDihnJwcFRYWSpJ8Pp/27NmjX/ziF1HvsXjxYq1cuVIbNmyQJG3atEnLli3T9OnT1dHRoS1btshms2n16tXD+UwALM6WYdPCooWpLgNAGok5sLz//vtatGhR6PXGjRslSWvWrNHOnTslSb/+9a9lmuaggaOpqUnnz58PvW5ra9Pq1at14cIFTZkyRXfeeaeOHj2qKVOmxFoeAAAYhQzTNCOXnUwzPp9P2dnZ8nq9jGcBACBNxPL7zV5CAADA8titGQCG4A/4GSAMWACBBQAG4Wn0qKKuImwPJIfdoWp3NVOwgSTjkRAAROFp9Ki8pjxiw8Z2X7vKa8rlafSkqDJgbCKwAMAA/oBfFXUVMhU5J8H8v/+rrKuUP+BPQXXA2ERgAYABGloaInpWBmr1taqhpSFJFQEgsADAAO2+9ri2AzByBBYAGOCzzz+LazsAI0dgAYABpnzjylbZvtJ2AEaOwAIAAwzcTXqk7QCMHIEFAAa43XG7bMbQi8PZDJtud9yepIoAEFgAYID32t6T3xx6yrLf9Ou9tveSVBEAAgsADNDZ0xnXdgBGjsACAAPkZ+XHtR2AkSOwAMAArkKXHHaHDBlRrxsy5LQ75Sp0JbkyYOwisADAALYMm6rd1ZIUEVqCr6vcVezaDCQRgQVA0vkDftWfrdfuj3ar/my9JffkKZtTptpVtRFTlx12h2pX1bJbM5Bkhmmakbt7pRmfz6fs7Gx5vV7Z7fZUlwNgCJ5GjyrqKsL26nHYHap2V1syBPgDfjW0NKizp1P5WflyFbroWQHiJJbfbwILgKTxNHpUXlMesQty8DELPRfA2BLL7zePhAAkhT/gV0VdRURYkRQ6V1lXOezHQ+nwmAnA8F2V6gIAjA0NLQ1hj4EGMmWq1deqhpYGLSxaGNO90+0xE4DY0cMCICkStRhb8DHTwDDU7mtXeU25PI2emO4HwJoILACSIhGLsSX6MRMA6yCwAEiKRCzGFstjJgDpjcACICkSsRgbe/4AYweBBcCg4j3zJt6LsbHnDzB2sA4LgKgSOfMmXoux+QN+FVUXqd3XHnUciyFDDrtDzRXNLPYGWBALxwEYkXRa4C1Yq6Sweq1YK4BwLBwHYNjSbeYNe/4AYwMLxwEIk8gF3hKlbE6Zls9azp4/wChGYAEQJl1n3tgybJYJUADij0dCAMIw8waAFcUcWA4fPqxly5apoKBAhmFo3759YdfXrl0rwzDCDrfbfdn77tixQ0VFRZowYYKKi4v1u9/9LtbSAMRBIhZ4A4CRijmw9PX1ad68edqxY8egbdxutzo7O0PH7t27h7znb37zG23cuFFbtmzR8ePHNW/ePJWUlOjTTz+NtTwAI5SIBd4AYKRiDiylpaV69tlntXLlykHbZGZmKi8vL3Rce+21Q97zH//xH/XQQw/pwQcf1Le+9S299NJL+sY3vqGXX3451vIAxAEzbwBYTUIG3dbX12vq1Km69tpr9ad/+qd69tlnNWnSpKhtv/zyS33wwQfavHlz6FxGRoaWLFmiI0eOJKI8AFeAmTcArCTugcXtdqusrEwzZsxQU1OTfvazn6m0tFRHjhyRzRb5P3Tnz5+X3+9Xbm5u2Pnc3Fx9/PHHUf+N/v5+9ff3h177fL74fggAkph5A8A64h5Y7rvvvtB/33LLLZo7d66uu+461dfXa/HixXH5N7Zv365t27bF5V4AAMD6Ej6teebMmZo8ebLOnDkT9frkyZNls9l07ty5sPPnzp1TXl5e1Pds3rxZXq83dLS2tsa9bgAAYB0JDyxtbW26cOGC8vOjr9kwfvx4zZ8/XwcOHAidCwQCOnDggBYsWBD1PZmZmbLb7WEHAAAYvWIOLL29vTpx4oROnDghSWpubtaJEyfU0tKi3t5ePfHEEzp69KjOnj2rAwcOaPny5br++utVUlISusfixYv1wgsvhF5v3LhR//zP/6xXX31VjY2NeuSRR9TX16cHH3xw5J8QAACkvZjHsLz//vtatGhR6PXGjRslSWvWrNGLL76oDz/8UK+++qq6u7tVUFCgpUuX6plnnlFmZmboPU1NTTp//nzo9b333qvPPvtMTz/9tLq6unTrrbeqrq4uYiAugOTyB/zMEgJgCYZpmpFbsqaZWLanBnBlPI0eVdRVhG2E6LA7VO2uZh0WAHERy+83ewkBo4Q/4Ff92Xrt/mi36s/Wyx/wD/tenkaPymvKI3Ztbve1q7ymXJ5Gz0jLBYCYsFszMArEszfEH/Croq5CpiI7X02ZMmSosq5Sy2ct5/EQgKShhwVIc/HuDWloaYi419eZMtXqa1VDS8Ow6gWA4SCwAGnscr0hklRZVxnT46HOns64tgOAeCCwAGksEb0h+VnR10wabjsAiAcCC5DGEtEb4ip0yWF3yJAR9bohQ067U65C1xXfEwBGisACpLFE9IbYMmyqdldLUkRoCb6uclcx4BZAUhFYgDSWqN6Qsjllql1Vq2n2aWHnHXaHalfVsg4LgKRjWjOQxoK9IeU15TJkhA2+HWlvSNmcMi2ftZyVbgFYAivdAqNAtHVYnHanqtxV9IYAsKxYfr8JLMAowb4/ANJNLL/fPBICRglbhk0LixamugwASAgG3QIAAMsjsAAAAMsjsAAAAMsjsAAAAMtj0C2AQTHzCIBVEFgARBVtbReH3aFqdzVruwBIOh4JAYjgafSovKY8Yifodl+7ymvK5Wn0pKgyAGMVgQVAGH/Ar4q6irBl/oOC5yrrKuUP+JNdGoAxjMACIExDS0NEz8rXmTLV6mtVQ0tDEqsCMNYRWACE6ezpjGs7AIgHAguAMPlZ+XFtBwDxQGABEMZV6JLD7pAhI+p1Q4acdqdcha4kVwZgLCOwAAhjy7Cp2l0tSRGhJfi6yl3FeiwAkorAAiBC2Zwy1a6q1TT7tLDzDrtDtatqWYcFQNIZpmlGzl1MMz6fT9nZ2fJ6vbLb7akuBxg1WOkWQCLF8vvNSrcABmXLsGlh0cJUlwEAPBICAADWR2ABAACWxyMhYAiM4QAAayCwAINgt2IAsA4eCQFRsFsxAFhLzIHl8OHDWrZsmQoKCmQYhvbt2xe6dunSJT355JO65ZZbdM0116igoEAPPPCAOjo6hrzn1q1bZRhG2DF79uyYPwwQD+xWDADWE3Ng6evr07x587Rjx46Ia59//rmOHz+up556SsePH5fH49GpU6f053/+55e970033aTOzs7Q8e6778ZaGhAXid6t2B/wq/5svXZ/tFv1Z+sJPgBwBWIew1JaWqrS0tKo17Kzs7V///6wcy+88IK+/e1vq6WlRYWFhYMXctVVysvLi7UcIO4SuVsx42IAYHgSPobF6/XKMAxNnDhxyHanT59WQUGBZs6cqfvvv18tLS2Dtu3v75fP5ws7gHhJ1G7FjIsBgOFLaGC5ePGinnzySa1evXrIJXeLi4u1c+dO1dXV6cUXX1Rzc7NcLpd6enqitt++fbuys7NDh9PpTNRHwBiUiN2KGRcDACOTsMBy6dIlrVq1SqZp6sUXXxyybWlpqe655x7NnTtXJSUlevvtt9Xd3a2ampqo7Tdv3iyv1xs6WltbE/ERMEYlYrfiRI+LAYDRLiGBJRhWPvnkE+3fvz/mDQknTpyoG2+8UWfOnIl6PTMzU3a7PewA4ineuxUnclxMEIN5AYxmcV84LhhWTp8+rYMHD2rSpEkx36O3t1dNTU360Y9+FO/ygCtWNqdMy2ctj8tKt4kaFxPEYF4Ao13MgaW3tzes56O5uVknTpxQTk6O8vPzVV5eruPHj+utt96S3+9XV1eXJCknJ0fjx4+XJC1evFgrV67Uhg0bJEmbNm3SsmXLNH36dHV0dGjLli2y2WxavXp1PD4jLCYRy90nagn9eO1WHBwX0+5rjzqOxZAhh90R07iYoOBg3oH3DQ7mHU6PEABYTcyB5f3339eiRYtCrzdu3ChJWrNmjbZu3ao33nhDknTrrbeGve/gwYNauHChJKmpqUnnz58PXWtra9Pq1at14cIFTZkyRXfeeaeOHj2qKVOmxFoeLC4RPQHp0LsQHBdTXlMuQ0ZYuBjuuBjp8oN5DRmqrKvU8lnL2QMJQFozTNOM/F+6NOPz+ZSdnS2v18t4FgsbrCcg+IM9nJ6ARNwzkaKFK6fdqSp31bDqrD9br0WvLrpsu4NrDsalpwgA4imW3282P0RSJKInIB17F+I5LkZKzmBeALACAguSIpZpvVfaE5CIeyZDvMbFSIkfzAsAVsFuzUiKRPQE0LuQmEXuAMCKCCxIikT0BNC7kJhF7gDAiggsSIpE9ATQu/CVeC9yBwBWxBgWJEUipvUmaqpwOor3YF4AsBqmNSOp4j2tN1H3BAAkXiy/3wQWJF06rXQLAEgc1mGBpcVzWm8i7wkAsA4G3QIAAMujhwUYJXgsBmA0I7AAo0A6bAAJACPBIyFgCP6AX/Vn67X7o92qP1svf8Cf6pIiBDeAHLhNQbuvXeU15fI0elJUGQDEDz0swCDSodciHTeABIDhoIcFiCJdei1i2QASANIZgQUY4HK9FpJUWVdpicdDbAAJYKwgsAADpFOvBRtAAhgrCCzAAOnUa8EGkADGCgILMEA69VoEN4CUFBFaxtoGkABGNwILMICr0KVJV08ass2kqydZpteibE6ZalfVapp9Wth5h92h2lW1lpnRBAAjwbRmYBQom1Om5bOWs9ItgFGLwAIM0NDSoAtfXBiyzYUvLqihpcFSGy6yASSA0YxHQsAA6TToFgDGCgILMEA6DboFgLGCwAIMwFRhALAeAgswAFOFAcB6CCxAFEwVBgBrMUzTjNwwJc34fD5lZ2fL6/XKbrenuhyMIv6An6nCAJAgsfx+M60ZGAJThQHAGngkBAAALI/AAgAALI/AAgAALC/mwHL48GEtW7ZMBQUFMgxD+/btC7tumqaefvpp5efn6+qrr9aSJUt0+vTpy953x44dKioq0oQJE1RcXKzf/e53sZYGAABGqZgDS19fn+bNm6cdO3ZEvf7cc8/p+eef10svvaRjx47pmmuuUUlJiS5evDjoPX/zm99o48aN2rJli44fP6558+appKREn376aazlAQCAUWhE05oNw9DevXu1YsUKSV/1rhQUFOjxxx/Xpk2bJEler1e5ubnauXOn7rvvvqj3KS4u1m233aYXXnhBkhQIBOR0OvXoo4/qr//6ry9bB9OaAQBIP7H8fsd1DEtzc7O6urq0ZMmS0Lns7GwVFxfryJEjUd/z5Zdf6oMPPgh7T0ZGhpYsWTLoe/r7++Xz+cIOAAAwesU1sHR1dUmScnNzw87n5uaGrg10/vx5+f3+mN6zfft2ZWdnhw6n0xmH6gEAgFWl5SyhzZs3y+v1ho7W1tZUlwQAABIoroElLy9PknTu3Lmw8+fOnQtdG2jy5Mmy2WwxvSczM1N2uz3sAAAAo1dcA8uMGTOUl5enAwcOhM75fD4dO3ZMCxYsiPqe8ePHa/78+WHvCQQCOnDgwKDvAQbyB/yqP1uv3R/tVv3ZevkD/lSXBACIo5j3Eurt7dWZM2dCr5ubm3XixAnl5OSosLBQlZWVevbZZ3XDDTdoxowZeuqpp1RQUBCaSSRJixcv1sqVK7VhwwZJ0saNG7VmzRr9yZ/8ib797W+rqqpKfX19evDBB0f+CTHqeRo9qqirUJuvLXTOYXeo2l3NrsoAMErEHFjef/99LVq0KPR648aNkqQ1a9Zo586d+ulPf6q+vj49/PDD6u7u1p133qm6ujpNmDAh9J6mpiadP38+9Pree+/VZ599pqefflpdXV269dZbVVdXFzEQFxjI0+hReU25TIXPzm/3tau8ply1q2oJLQAwCoxoHRarYB2Wsckf8KuouiisZ+XrDBly2B1qrmiWLcOW5OoAAJeTsnVYgGRqaGkYNKxIkilTrb5WNbQ0JLEqAEAiEFiQtjp7OuPaDgBgXQQWpK38rPy4tgMAWFfMg24Bq7jdcbtshk1+c/ApzDbDptsdtw/73/AH/GpoaVBnT6fys/LlKnQxHgYAUoDAgrT1Xtt7Q4YVSfKbfr3X9p4WFi2M+f5MlwYA6+CRENJWIsewBKdLDxzUG5wu7Wn0xHxPAMDwEViQtqZeMzWu7YL8Ab8q6ioi1naRFDpXWVfJaroAkEQEFmAApksDgPUQWJC2Pu37NK7tgpguDQDWQ2BB2krUtGamSwOA9RBYkLZchS457A4ZMqJeN2TIaXfKVeiyxH0BAMNHYEHasmXYVO2ulqSIcBF8XeWuinndlOB9ow26lb4awzKc+wIAho/AgrRWNqdMtatqNc0+Ley8w+5gp2YAGEXYrRmjQjxXpGUXaABIjlh+v1npFqOCLcM2rNVso4llWnO8/k0AwNAILBgV4tnDwrRmALAeAguSLt4bCsZ7zx+mNQOA9RBYkFTxDhfBPX8GzugJ7vkznIG3wWnN7b72qDOFgmNYmNYMAMnDLCEkTbw3FEzUnj+Jmi4NABg+AguSIhHhIpF7/jBdGgCshUdCSIpEzLxJ9ODYsjllWj5reVzH2wAAhofAgqRIRLhIxuDYeE6XBgAMH4FlCPGezTKWJSJcMDgWAMYOAssg4j2bZaxLRLgIDo4trymXISPsvgyOBYDRhUG3UcR7NgsSN/OGwbEAMDawl9AA7COTWNF6rpx2p6rcVSMKFzy+A4D0E8vvN4FlgPqz9Vr06qLLtju45iCDMYeJcAEAkNj8cETYRybxmHkDAIgVY1gGYB8ZAACsh8AyQHA2y8CBoUGGDDntTqbKAgCQRASWAdhHBgAA6yGwRMFUWQAArCXugaWoqEiGYUQc69evj9p+586dEW0nTJgQ77JiVjanTGcrzurgmoPaVbZLB9ccVHNFM2EFAIAUiPssof/8z/+U3///O+6ePHlS3/ve93TPPfcM+h673a5Tp06FXhtG9PEjycZsFgAArCHugWXKlClhr//u7/5O1113nb773e8O+h7DMJSXlxfvUgAAwCiR0DEsX375pV577TX9+Mc/HrLXpLe3V9OnT5fT6dTy5cv1X//1X4ksCwAApJmEBpZ9+/apu7tba9euHbTNrFmz9PLLL+v111/Xa6+9pkAgoNtvv11tbdGXxpek/v5++Xy+sAMAAIxeCV2av6SkROPHj9ebb755xe+5dOmS5syZo9WrV+uZZ56J2mbr1q3atm1bxPl4LM0PAACSI5al+RPWw/LJJ5/onXfe0U9+8pOY3jdu3Dj90R/9kc6cOTNom82bN8vr9YaO1tbWkZab9vwBv+rP1mv3R7tVf7Ze/oD/8m8CACBNJGwvoVdeeUVTp07Vn/3Zn8X0Pr/fr48++kjf//73B22TmZmpzMzMkZY4akTbAdlhd6jaXc00bADAqJCQHpZAIKBXXnlFa9as0VVXhWeiBx54QJs3bw69/tu//Vv9x3/8h/7whz/o+PHj+uEPf6hPPvkk5p6ZscrT6FF5TXlYWJGkdl+7ymvK5Wn0pKiywdEbBACIVUJ6WN555x21tLToxz/+ccS1lpYWZWT8f076n//5Hz300EPq6urStddeq/nz5+u9997Tt771rUSUNqr4A35V1FXIVOQwJFOmDBmqrKvU8lnLLbOVAL1BAIDhSOig22SJZdDOaFJ/tl6LXl102XYH1xy0xAJ4wd6ggQEruEcT2x4AwNhiiUG3SLzOns64tkuky/UGSVJlXSWPhwAAURFY0lh+Vn5c2yVSQ0tDxDibrzNlqtXXqoaWhiRWBQBIFwSWNOYqdMlhd4QeqQxkyJDT7pSr0JXkyiKlU28QAMB6CCxpzJZhU7W7WpIiQkvwdZW7yhIDbtOpNwgAYD0EljRXNqdMtatqNc0+Ley8w+6w1CDWdOoNAgBYT8IWjkPylM0p0/JZy9XQ0qDOnk7lZ+XLVeiyRM9KULA3qLymXIaMsMG3VusNAgBYD9OakVTR1mFx2p2qcldZpjcIAJAcsfx+E1iQdP6A39K9QQCA5Ijl95tHQkg6W4bNEgvZAQDSB4NuAQCA5RFYAACA5RFYAACA5RFYAACA5RFYAACA5TFLCINi+jEAwCoILIgq2gJvDrtD1e5qFngDACQdj4QQwdPoUXlNeVhYkaR2X7vKa8rlafSkqDIAwFhFYEEYf8CvirqKsL1+goLnKusq5Q/4k10aAGAMI7AgTENLQ0TPyteZMtXqa1VDS0MSqwIAjHUEFoTp7OmMazsAAOKBwIIw+Vn5cW0HAEA8EFgQxlXoksPukCEj6nVDhpx2p1yFriRXBgAYywgsCGPLsKnaXS1JEaEl+LrKXcV6LACApCKwIELZnDLVrqrVNPu0sPMOu0O1q2pZhwUAkHSGaZqR81fTjM/nU3Z2trxer+x2e6rLGTVY6RYAkEix/H6z0i0GZcuwaWHRwlSXAQAAgSXZ6LUAACB2BJYkYn8eAACGh0G3ScL+PAAADB+BJQnYnwcAgJEhsCQB+/MAADAyBJYkYH8eAABGhsCSBOzPAwDAyMQ9sGzdulWGYYQds2fPHvI9e/bs0ezZszVhwgTdcsstevvtt+NdVkqxPw8AACOTkB6Wm266SZ2dnaHj3XffHbTte++9p9WrV2vdunX6/e9/rxUrVmjFihU6efJkIkpLCfbnAQBgZBISWK666irl5eWFjsmTJw/atrq6Wm63W0888YTmzJmjZ555Rn/8x3+sF154IRGlpQz78wAAMHwJWTju9OnTKigo0IQJE7RgwQJt375dhYWFUdseOXJEGzduDDtXUlKiffv2DXr//v5+9ff3h177fL641J1oZXPKtHzWcla6BQAgRnEPLMXFxdq5c6dmzZqlzs5Obdu2TS6XSydPnlRWVlZE+66uLuXm5oady83NVVdX16D/xvbt27Vt27Z4l54U7M8DAEDs4v5IqLS0VPfcc4/mzp2rkpISvf322+ru7lZNTU3c/o3NmzfL6/WGjtbW1rjdGwAAWE/C9xKaOHGibrzxRp05cybq9by8PJ07dy7s3Llz55SXlzfoPTMzM5WZmRnXOgEAgHUlfB2W3t5eNTU1KT8/+hojCxYs0IEDB8LO7d+/XwsWLEh0aQAAIE3EPbBs2rRJhw4d0tmzZ/Xee+9p5cqVstlsWr16tSTpgQce0ObNm0PtKyoqVFdXp1/84hf6+OOPtXXrVr3//vvasGFDvEsDAABpKu6PhNra2rR69WpduHBBU6ZM0Z133qmjR49qypQpkqSWlhZlZPx/Trr99tu1a9cu/c3f/I1+9rOf6YYbbtC+fft08803x7u0Uc0f8DP7CAAwahmmaUZuIZxmfD6fsrOz5fV6ZbfbU11O0nkaPaqoqwjbYNFhd6jaXc36LgAAy4rl95u9hNKcp9Gj8pryiN2g233tKq8pl6fRk6LKAACIHwJLGvMH/Kqoq5CpyE6y4LnKukr5A/5klwYAQFwRWNJYQ0tDRM/K15ky1eprVUNLQxKrAgAg/ggsaayzpzOu7QAAsCoCSxrLz4q+ts1w2wEAYFUEljTmKnTJYXfIkBH1uiFDTrtTrkJXkisDACC+CCxpzJZhU7W7WpIiQkvwdZW7ivVYAABpj8CS5srmlKl2Va2m2aeFnXfYHapdVcs6LACAUYGF40YJVroFAKSbWH6/E75bM5LDlmHTwqKFqS4DAICE4JEQAACwPAILAACwPAILAACwPAILAACwPAILAACwPAILAACwPAILAACwPAILAACwPAILAACwvFGx0m1wdwGfz5fiSgAAwJUK/m5fyS5BoyKw9PT0SJKcTmeKKwEAALHq6elRdnb2kG1GxeaHgUBAHR0dysrKkmEYcb23z+eT0+lUa2vrmN1YMV3wXaUXvq/0wXeVPtLtuzJNUz09PSooKFBGxtCjVEZFD0tGRoYcDkdC/w273Z4WXz74rtIN31f64LtKH+n0XV2uZyWIQbcAAMDyCCwAAMDyCCyXkZmZqS1btigzMzPVpeAy+K7SC99X+uC7Sh+j+bsaFYNuAQDA6EYPCwAAsDwCCwAAsDwCCwAAsDwCCwAAsDwCyyC2bt0qwzDCjtmzZ6e6LEg6fPiwli1bpoKCAhmGoX379oVdN01TTz/9tPLz83X11VdryZIlOn36dGqKHeMu912tXbs24u/M7Xanptgxbvv27brtttuUlZWlqVOnasWKFTp16lRYm4sXL2r9+vWaNGmSvvnNb+ruu+/WuXPnUlTx2HYl39fChQsj/r7+4i/+IkUVjxyBZQg33XSTOjs7Q8e7776b6pIgqa+vT/PmzdOOHTuiXn/uuef0/PPP66WXXtKxY8d0zTXXqKSkRBcvXkxypbjcdyVJbrc77O9s9+7dSawQQYcOHdL69et19OhR7d+/X5cuXdLSpUvV19cXavPYY4/pzTff1J49e3To0CF1dHSorKwshVWPXVfyfUnSQw89FPb39dxzz6Wo4jgwEdWWLVvMefPmpboMXIYkc+/evaHXgUDAzMvLM3/+85+HznV3d5uZmZnm7t27U1AhggZ+V6ZpmmvWrDGXL1+eknowtE8//dSUZB46dMg0za/+jsaNG2fu2bMn1KaxsdGUZB45ciRVZeL/DPy+TNM0v/vd75oVFRWpKyrO6GEZwunTp1VQUKCZM2fq/vvvV0tLS6pLwmU0Nzerq6tLS5YsCZ3Lzs5WcXGxjhw5ksLKMJj6+npNnTpVs2bN0iOPPKILFy6kuiRI8nq9kqScnBxJ0gcffKBLly6F/W3Nnj1bhYWF/G1ZwMDvK+hf//VfNXnyZN18883avHmzPv/881SUFxejYvPDRCguLtbOnTs1a9YsdXZ2atu2bXK5XDp58qSysrJSXR4G0dXVJUnKzc0NO5+bmxu6Butwu90qKyvTjBkz1NTUpJ/97GcqLS3VkSNHZLPZUl3emBUIBFRZWak77rhDN998s6Sv/rbGjx+viRMnhrXlbyv1on1fkvSDH/xA06dPV0FBgT788EM9+eSTOnXqlDweTwqrHT4CyyBKS0tD/z137lwVFxdr+vTpqqmp0bp161JYGTB63HfffaH/vuWWWzR37lxdd911qq+v1+LFi1NY2di2fv16nTx5knF7aWKw7+vhhx8O/fctt9yi/Px8LV68WE1NTbruuuuSXeaI8UjoCk2cOFE33nijzpw5k+pSMIS8vDxJipi5cO7cudA1WNfMmTM1efJk/s5SaMOGDXrrrbd08OBBORyO0Pm8vDx9+eWX6u7uDmvP31ZqDfZ9RVNcXCxJafv3RWC5Qr29vWpqalJ+fn6qS8EQZsyYoby8PB04cCB0zufz6dixY1qwYEEKK8OVaGtr04ULF/g7SwHTNLVhwwbt3btXv/3tbzVjxoyw6/Pnz9e4cePC/rZOnTqllpYW/rZS4HLfVzQnTpyQpLT9++KR0CA2bdqkZcuWafr06ero6NCWLVtks9m0evXqVJc25vX29ob9fwjNzc06ceKEcnJyVFhYqMrKSj377LO64YYbNGPGDD311FMqKCjQihUrUlf0GDXUd5WTk6Nt27bp7rvvVl5enpqamvTTn/5U119/vUpKSlJY9di0fv167dq1S6+//rqysrJC41Kys7N19dVXKzs7W+vWrdPGjRuVk5Mju92uRx99VAsWLNB3vvOdFFc/9lzu+2pqatKuXbv0/e9/X5MmTdKHH36oxx57THfddZfmzp2b4uqHKdXTlKzq3nvvNfPz883x48eb06ZNM++9917zzJkzqS4LpmkePHjQlBRxrFmzxjTNr6Y2P/XUU2Zubq6ZmZlpLl682Dx16lRqix6jhvquPv/8c3Pp0qXmlClTzHHjxpnTp083H3roIbOrqyvVZY9J0b4nSeYrr7wSavPFF1+Yf/mXf2lee+215je+8Q1z5cqVZmdnZ+qKHsMu9321tLSYd911l5mTk2NmZmaa119/vfnEE0+YXq83tYWPgGGappnMgAQAABArxrAAAADLI7AAAADLI7AAAADLI7AAAADLI7AAAADLI7AAAADLI7AAAADLI7AAAADLI7AAAADLI7AAAADLI7AAAADLI7AAAADL+186E2KCuetoqAAAAABJRU5ErkJggg==\n",
      "text/plain": [
       "<Figure size 640x480 with 1 Axes>"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.scatter(y_test,y_pred,c='g')"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.11.0"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
