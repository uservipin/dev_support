### jupyter_extension_command
 This list of command help to intigrate extensions in jupyter notebook using anaconda

### save dependencies in .txt file 
pip install pipreqs # install pipreqs if not install in venv

pipreqs . --force  # execute command to save required dependencies


# Input
ser = pd.Series(['01 Jan 2010', '02-02-2011', '20120303', '2013/04/04', '2014-05-05', '2015-06-06T12:20'])

# Solution
from dateutil.parser import parse
ser_ts = ser.map(lambda x: parse(x))

# day of month
print("Date: ", ser_ts.dt.day.tolist())
