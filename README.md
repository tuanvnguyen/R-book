<p align="center">
    <img src=".github/logo.svg?sanitize=true" />
</p>

## Description
This site contains all datasets for the book 'Phân tích dữ liệu với R' (Nxb Tổng Hợp, 2016). 

## How to read the dataset online?

- Get the name of dataset which you want to read
- Copy the following code and change the variable `name` 

### For instance readataset with row names: 

Reading the Dataset `ExampleData.csv`

```r
# Get the name of dataset
name = "ExampleData.csv"

# Get the link of dataset
page = "https://raw.githubusercontent.com/tuanvnguyen/R-book/master/"
theLink = paste(page,name,sep="")

# Read the dataset
dat = read.csv(theLink,       # The file input or the link input
               header=T,      # Set the first row as the header
               row.names=1)   # Set the first column as the name of individuals
head(dat)
```
<table class="dataframe">
<caption>Output table</caption>
<thead>
	<tr><th></th><th scope=col>e2b1</th><th scope=col>g1b1</th><th scope=col>i11</th><th scope=col>pcs1</th><th scope=col>mcs1</th><th scope=col>cesd1</th><th scope=col>indtot1</th><th scope=col>drugrisk1</th><th scope=col>sexrisk1</th><th scope=col>pcrec1</th><th scope=col>...</th><th scope=col>satreat</th><th scope=col>drinkstatus</th><th scope=col>daysdrink</th><th scope=col>anysubstatus</th><th scope=col>daysanysub</th><th scope=col>linkstatus</th><th scope=col>dayslink</th><th scope=col>female</th><th scope=col>substance</th><th scope=col>racegrp</th></tr>
	<tr><th></th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;dbl&gt;</th><th scope=col>&lt;dbl&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>...</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;int&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope=row>1</th><td>NA</td><td>0</td><td>NA</td><td>54.22583</td><td>52.23480</td><td> 7</td><td> 5</td><td> 0</td><td>1</td><td>1</td><td>...</td><td>0</td><td>1</td><td>177</td><td>1</td><td>177</td><td> 1</td><td>225</td><td>0</td><td>cocaine</td><td>black</td></tr>
	<tr><th scope=row>2</th><td>NA</td><td>0</td><td> 8</td><td>59.56066</td><td>41.72696</td><td>11</td><td>12</td><td> 0</td><td>0</td><td>0</td><td>...</td><td>0</td><td>1</td><td>  2</td><td>1</td><td>  2</td><td>NA</td><td> NA</td><td>0</td><td>alcohol</td><td>white</td></tr>
	<tr><th scope=row>3</th><td>NA</td><td>0</td><td>NA</td><td>58.45777</td><td>56.77131</td><td>14</td><td>99</td><td>13</td><td>4</td><td>0</td><td>...</td><td>0</td><td>1</td><td>  3</td><td>1</td><td>  3</td><td> 0</td><td>365</td><td>0</td><td>heroin </td><td>black</td></tr>
	<tr><th scope=row>4</th><td>NA</td><td>0</td><td>NA</td><td>46.60988</td><td>14.65925</td><td>44</td><td>97</td><td> 0</td><td>4</td><td>0</td><td>...</td><td>1</td><td>0</td><td>196</td><td>1</td><td>189</td><td> 0</td><td>343</td><td>1</td><td>heroin </td><td>white</td></tr>
	<tr><th scope=row>5</th><td>NA</td><td>0</td><td>64</td><td>31.41642</td><td>40.67421</td><td>26</td><td>55</td><td> 0</td><td>4</td><td>0</td><td>...</td><td>0</td><td>1</td><td>  2</td><td>1</td><td>  2</td><td> 1</td><td> 57</td><td>0</td><td>cocaine</td><td>black</td></tr>
</tbody>
</table>

### Read dataset without row names

```r
# Get the name of dataset
name = "PISA DATA.csv"

# Get the link of dataset
page = "https://raw.githubusercontent.com/tuanvnguyen/R-book/master/"
theLink = paste(page,name,sep="")

# Read the dataset
dat = read.csv(theLink,       # The file input or the link input
               header=T,)      # Set the first row as the header

head(dat)
```
<p align="center">
<table class="dataframe">
<caption>A data.frame: 6 × 7</caption>
<thead>
	<tr><th></th><th scope=col>REGION</th><th scope=col>TYPE</th><th scope=col>AREA</th><th scope=col>GENDER</th><th scope=col>MATH</th><th scope=col>READING</th><th scope=col>SCIENCE</th></tr>
	<tr><th></th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;chr&gt;</th><th scope=col>&lt;dbl&gt;</th><th scope=col>&lt;dbl&gt;</th><th scope=col>&lt;dbl&gt;</th></tr>
</thead>
<tbody>
	<tr><th scope=row>1</th><td>CENTRAL</td><td>PUBLIC</td><td>URBAN</td><td>Male  </td><td>604.775</td><td>506.490</td><td>540.228</td></tr>
	<tr><th scope=row>2</th><td>CENTRAL</td><td>PUBLIC</td><td>URBAN</td><td>Male  </td><td>565.127</td><td>534.879</td><td>542.466</td></tr>
	<tr><th scope=row>3</th><td>CENTRAL</td><td>PUBLIC</td><td>URBAN</td><td>Female</td><td>536.073</td><td>510.269</td><td>547.128</td></tr>
	<tr><th scope=row>4</th><td>CENTRAL</td><td>PUBLIC</td><td>URBAN</td><td>Male  </td><td>622.846</td><td>599.195</td><td>621.354</td></tr>
	<tr><th scope=row>5</th><td>CENTRAL</td><td>PUBLIC</td><td>URBAN</td><td>Female</td><td>544.641</td><td>583.981</td><td>548.993</td></tr>
	<tr><th scope=row>6</th><td>CENTRAL</td><td>PUBLIC</td><td>URBAN</td><td>Female</td><td>472.200</td><td>480.085</td><td>441.570</td></tr>
</tbody>
</table></p>

## Youtube Courses

You can find out the courses about R-Book on [Youtube](https://www.youtube.com/results?search_query=nguyen+van+tuan)
