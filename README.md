# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
print(df)
```
<img width="853" height="776" alt="Screenshot 2025-10-07 200203" src="https://github.com/user-attachments/assets/9bf5c21a-0bc5-4f8e-821a-0ccc1883cc38" />

```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
print(df.isnull())
```
<img width="882" height="585" alt="Screenshot 2025-10-07 200551" src="https://github.com/user-attachments/assets/cdc12586-4e95-4eaa-a420-711272863db4" />
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
print(df.isnull().sum())
```
<img width="356" height="238" alt="Screenshot 2025-10-07 200737" src="https://github.com/user-attachments/assets/338ea6b1-86f7-42a4-8f63-a71b002877af" />
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
drop=df.dropna()
print("after dropna \n\n",drop)
```
<img width="1071" height="784" alt="Screenshot 2025-10-07 201035" src="https://github.com/user-attachments/assets/763349a8-31a9-420b-b8a0-452cc3f12d23" />

```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
drop=df.dropna(axis=1)
print("after dropna \n\n",drop)
```
<img width="681" height="354" alt="Screenshot 2025-10-07 202341" src="https://github.com/user-attachments/assets/b47affb2-47ea-4304-9a0d-c9bab8a6773e" />

```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
drop=df.dropna(axis=1,inplace=True)
print("after dropna \n\n",drop)
```
<img width="190" height="72" alt="image" src="https://github.com/user-attachments/assets/e056aa7d-beb6-4da3-beb8-a880c70c8783" />
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
loc=df.iloc[1:21:3]
print(loc)
```
<img width="848" height="568" alt="{ED5E4DF6-0343-4521-A400-1163359CBDF1}" src="https://github.com/user-attachments/assets/c4ce09a7-0446-449d-af1c-e27515217f41" />
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
fill=df.fillna(method='ffill')
print(fill)
```
<img width="1004" height="788" alt="{59A0BE58-2972-480A-B3D4-691BB009EACF}" src="https://github.com/user-attachments/assets/6f22fb52-1e16-418b-bdcc-f83a9139aae3" />
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
fill=df.fillna(method='bfill')
print(fill)
```
<img width="981" height="780" alt="{404C8411-B9F3-4619-BAF0-357EACA66D38}" src="https://github.com/user-attachments/assets/3a40959d-7a54-492d-b740-4042f6e68c85" />
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
mean=df.mean()
print(mean)
```
<img width="494" height="140" alt="image" src="https://github.com/user-attachments/assets/7ba6e175-10d9-4018-a4b7-063b65801089" />
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
k=df.median()
print(k)
```
<img width="448" height="151" alt="image" src="https://github.com/user-attachments/assets/4ff3ae2b-bfbe-43b9-a804-87e6050cbf77" />
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
k=df.mode()
print(k)
```
<img width="850" height="773" alt="{9F901C29-93DA-4BB4-8989-50CACE925F4D}" src="https://github.com/user-attachments/assets/94c35d89-db0c-46f2-9dba-f2613be0d8a6" />
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
k=df.drop_duplicates()
print(k)
```
<img width="958" height="778" alt="{B6513E0F-3698-4541-95BC-6C0B9FF0815E}" src="https://github.com/user-attachments/assets/30928eb6-ed14-47f2-aa20-1576f4d25c84" />
```
import pandas as pd
d=pd.read_csv("Data_set.csv")
df=pd.DataFrame(d)
k=df.interpolate()
print(k)
```
<img width="1022" height="786" alt="{D41B9E71-5BFE-4D47-AA14-B17A34420B20}" src="https://github.com/user-attachments/assets/78be8f2d-587c-4e6c-9c7f-816fd5ab3aec" />
```
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
a=[1,3,28,67,94,24,47,98,54,48,35,39,25,97,31,22]
af=pd.DataFrame(a)
af
```
<img width="135" height="555" alt="{B0D705A3-50E8-4330-B644-F940F5BB7489}" src="https://github.com/user-attachments/assets/5549892f-7720-4698-b01d-df7b19f5fba8" />
```
import pandas as pd
d=pd.read_csv("iris.csv")
df=pd.DataFrame(d)
print(df)
df.info()
print(df.describe())
```
<img width="887" height="755" alt="{2CE5F110-9977-4FCE-940C-6B08005C85EF}" src="https://github.com/user-attachments/assets/49fcdbc7-95cd-4817-a9d4-14a1d04d6a15" />
```
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
import seaborn as sns
d=pd.read_csv("iris.csv")
df=pd.DataFrame(d)
df.info
plt.scatter(x='sepal_length',y='petal_width',data=df)
plt.ylabel("sepal")
plt.xlabel("petal")
plt.title("scatter plot")
plt.show()
```
<img width="933" height="573" alt="{65904DEF-BBA7-413D-B4E8-64173F51B834}" src="https://github.com/user-attachments/assets/7dbbc7e5-a846-4dd5-8f9f-736a0191bf04" />
```
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
import seaborn as sns
d=pd.read_csv("iris.csv")
df=pd.DataFrame(d)
df.info
plt.bar(df.index,df['petal_width'])
plt.ylabel("petal")
plt.xlabel("sepal")
plt.title("bar chart")
plt.show()
```
<img width="939" height="583" alt="{CA203D72-422D-42F7-9627-5C03DE742FF1}" src="https://github.com/user-attachments/assets/d6d66ee0-e6ad-4ca7-be93-e16fa25fd757" />





            <<include your coding and its corressponding output screen shots here>>
# Result
          <<include your Result here>>
