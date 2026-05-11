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

# Coding and Output:
```
import pandas as pd
data=pd.read_csv("/content/SAMPLEIDS.csv")
data
```
<img width="1198" height="670" alt="image" src="https://github.com/user-attachments/assets/e67cb9db-0373-493e-836f-ebd11b9bdb44" /><br>
```
data.info()
```
<img width="837" height="507" alt="image" src="https://github.com/user-attachments/assets/003747fd-2448-4e10-94f8-89642332345f" /><br>
```
data.describe()
```
<img width="1177" height="457" alt="image" src="https://github.com/user-attachments/assets/f23d2b37-d306-4b12-8b5e-e91081a6a452" /><br>
```
data.isnull()
```
<img width="1138" height="657" alt="image" src="https://github.com/user-attachments/assets/e9d8104f-bf16-4172-95af-b1282b563843" /><br>
```
data.isnull().sum()
```
<img width="821" height="622" alt="image" src="https://github.com/user-attachments/assets/dc91ba7c-7fd3-4c1e-924f-ecc7319dfcd0" /><br>
```
data.notnull()
```
<img width="1123" height="652" alt="image" src="https://github.com/user-attachments/assets/8453f993-4410-494a-8bad-dc436f952240" /><br>
```
data.notnull().sum()
```
<img width="581" height="628" alt="image" src="https://github.com/user-attachments/assets/498f2b57-7b1f-499f-9ce1-e3a6eee7d7b0" /><br>
```
data.dropna()
```
<img width="1380" height="621" alt="image" src="https://github.com/user-attachments/assets/d33193c6-38f1-4960-8320-fc6ef2150826" /><br>
```
data.dropna(axis=1)
```
<img width="730" height="701" alt="image" src="https://github.com/user-attachments/assets/db24897c-34d9-4706-a38c-84fcf84a5fc2" /><br>
```
data
```
<img width="1212" height="695" alt="image" src="https://github.com/user-attachments/assets/dd7f08f8-add5-42f6-9a8b-138b02de0fb9" /><br>
```
data.dropna(inplace=True)
data
```
<img width="1136" height="612" alt="image" src="https://github.com/user-attachments/assets/f61eeaa8-76f2-4b72-9e83-93c5f0801e4c" /><br>
```
import pandas as pd
data1=pd.read_csv("/content/Loan_data.csv")
data1
```

<img width="1747" height="582" alt="image" src="https://github.com/user-attachments/assets/b91c7bff-b515-409b-825e-ec6ccc544a98" /><br>
```
data.isnull()
```

<img width="1003" height="560" alt="image" src="https://github.com/user-attachments/assets/5b14477e-1580-4cb0-9513-b4b664127a3b" /><br>
```
data.isnull().sum()
```

<img width="821" height="561" alt="image" src="https://github.com/user-attachments/assets/724f5f38-e5ec-4f87-b331-6c48e9fa24a2" /><br>
```
data.fillna("Datascience")
```

<img width="1346" height="561" alt="image" src="https://github.com/user-attachments/assets/f63d9a1e-fcfc-4f5b-873a-e03eb84e200c" /><br>
```
data
```

<img width="1215" height="571" alt="image" src="https://github.com/user-attachments/assets/5b0c5e04-9cf6-4601-b9ea-1d1cdcbb0dfe" /><br>
```
data.ffill()
```

<img width="1156" height="551" alt="image" src="https://github.com/user-attachments/assets/75ed9422-b5ef-471d-9e73-7047b1a96699" /><br>
```
data=pd.read_csv("/content/SAMPLEIDS.csv")
data
```

<img width="1090" height="703" alt="image" src="https://github.com/user-attachments/assets/660f546b-60de-43d0-aec5-150ab83cb492" /><br>
```
data.ffill()
```

<img width="1110" height="707" alt="image" src="https://github.com/user-attachments/assets/777d4e4b-e3c4-4043-b4e8-bc4de32f66d8" /><br>
```
data.bfill()
```

<img width="965" height="702" alt="image" src="https://github.com/user-attachments/assets/247c9e25-408b-4a0b-8683-94f5ed04bbbc" /><br>
```
data['TOTAL'].fillna(method='bfill',inplace=True)
```

<img width="1788" height="306" alt="image" src="https://github.com/user-attachments/assets/f460178f-09be-4901-b055-209723f3a06c" /><br>
```
data
```

<img width="1210" height="705" alt="image" src="https://github.com/user-attachments/assets/6228dfbf-c348-44b9-b8f6-d9c18dca41eb" /><br>
```
data['M4'].fillna(value=data['M4'].mean(),inplace=True)
```

<img width="1791" height="246" alt="image" src="https://github.com/user-attachments/assets/942f2562-a06c-4c13-b2af-d12e58ead56e" /><br>
```
data
```
<img width="1196" height="707" alt="image" src="https://github.com/user-attachments/assets/1fccb69f-9aab-4ad7-bab1-5eba39ea9e50" /><br>
```
data['M4'].fillna(value=data['M4'].median(),inplace=True)
```

<img width="1802" height="248" alt="image" src="https://github.com/user-attachments/assets/ce2eb49b-732b-4fd0-b75c-cab324de82a6" /><br>
```
data
```

<img width="1133" height="717" alt="image" src="https://github.com/user-attachments/assets/00ed6aa7-0b2e-4e9a-8f94-0371cf409068" /><br>
```
data['M4'].fillna(value=data['M4'].mode(),inplace=True)
```

<img width="1771" height="225" alt="image" src="https://github.com/user-attachments/assets/e28c534f-592f-441b-a4a8-427009dd000d" /><br>
```
data
```

<img width="1127" height="711" alt="image" src="https://github.com/user-attachments/assets/12a8cf6e-eec4-47ec-8cb7-1100628c8249" /><br>

# IQR Method:
```
import pandas as pd
ir=pd.read_csv("iris.csv")
ir
```

<img width="596" height="437" alt="image" src="https://github.com/user-attachments/assets/4071b6a6-6b83-4fd4-82ba-566e7eb5c25d" /><br>
```
ir.describe()
```

<img width="492" height="297" alt="image" src="https://github.com/user-attachments/assets/f3de7f9a-6ff0-4cbe-ad15-6d0be77eddad" /><br>
```
ir.shape
```
```
(150, 5)
```
```
ir.info()
```

<img width="458" height="257" alt="image" src="https://github.com/user-attachments/assets/30cf4ea3-9f94-4dcc-8e4b-f3fa71f7767e" /><br>
```
import seaborn as sns
sns.boxplot(x='sepal_width',data=ir)
```

<img width="712" height="582" alt="image" src="https://github.com/user-attachments/assets/3dd0ee96-0adb-4771-bb1e-49f3721bf85b" /><br>
```
 q1=ir.sepal_width.quantile(0.25)
 q3=ir.sepal_width.quantile(0.75)
 iqr=q3-q1
 print(iqr)
```
```
0.5
```
```
 out=ir[((ir.sepal_width<(q1-1.5*iqr))|(ir.sepal_width>(q3+1.5*iqr)))]
 out['sepal_width']
```

<img width="326" height="116" alt="image" src="https://github.com/user-attachments/assets/f59d31e6-5f29-4455-90e3-6e035fcd78ff" /><br>
```
 nor=ir[~((ir.sepal_width<(q1-1.5*iqr))|(ir.sepal_width>(q3+1.5*iqr)))]
 nor['sepal_width']
```

<img width="487" height="268" alt="image" src="https://github.com/user-attachments/assets/c137dcbb-24a2-45e8-a782-c8cd1f57c734" /><br>
```
sns.boxplot(x='sepal_width',data=nor)
```

<img width="672" height="578" alt="image" src="https://github.com/user-attachments/assets/bddb1196-a195-4374-8389-9dc9051f8149" /><br>

# Z-Score Method:
```
import numpy as np
import pandas as pd
df=pd.read_csv("heights.csv")
df
```

<img width="192" height="498" alt="image" src="https://github.com/user-attachments/assets/f021b511-b8d2-4c08-9210-bc19d4c0ca6b" /><br>
```
import scipy.stats as stats
q1 = df['height'].quantile(0.25)
q2 = df['height'].quantile(0.5)
q3 = df['height'].quantile(0.75)
iqr = q3-q1
iqr
```
```
0.92499999999999998
```
```
low = q1 - 1.5*iqr
print(low)
high = q3 + 1.5*iqr
print(high)
```


<img width="205" height="55" alt="image" src="https://github.com/user-attachments/assets/88e81149-7dc7-4cd7-9b50-f521773e9ac9" /><br>
```
df1 = df[((df['height'] >=low)& (df['height'] <=high))]
df1
```

<img width="213" height="433" alt="image" src="https://github.com/user-attachments/assets/937d8b76-b3de-40c3-9786-2f220fb59228" /><br>
```
z = np.abs(stats.zscore(df['height']))
z
```

<img width="291" height="328" alt="image" src="https://github.com/user-attachments/assets/b18c516c-5f18-4474-9366-9d26dd8ccfcf" /><br>
```
df1 = df[z<3]
df1
```

<img width="186" height="461" alt="image" src="https://github.com/user-attachments/assets/de52217b-a2f1-4253-9021-a3b5e801fa5d" />












# Result:
The given dataset was successfully read and cleaned using Python. Missing values and duplicate records were handled properly, and the cleaned data was saved into a new file named cleaned_data.csv and removed the outliers using IQR and Z-score method.
