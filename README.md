from datetime import datetime
import calendar

D = {   
        '2020-01-01':4,'2020-01-02':4,'2020-01-03':6,'2020-01-04':8,
        '2020-01-05':2,'2020-01-06':-6,'2020-01-07':2,'2020-01-08':-2
    }
val = {'Mon':0, 'Tue':0, 'Wed':0, 'Thu':0, 'Fri':0, 'Sat':0, 'Sun':0 }
    
for x, y in D.items():
    curr_date = datetime.strptime(x, "%Y-%m-%d")
    
    ans =  calendar.day_name[curr_date.weekday()]
    if ans == 'Monday':
        val['Mon'] = val['Mon'] + y
    elif ans == 'Tuesday':
        val['Tue'] = val['Tue'] + y
    elif ans == 'Wednesday':
        val['Wed'] = val['Wed'] + y
    elif ans == 'Thursday':
        val['Thu'] = val['Thu'] + y
    elif ans == 'Friday':
        val['Fri'] = val['Fri'] + y
    elif ans == 'Saturday':
        val['Sat'] = val['Sat'] + y
    elif ans == 'Sunday':
        val['Sun'] = val['Sun'] + y

print(val)
