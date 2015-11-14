# converts military time to metric time
import sys

def main():
  normaltime = input('Enter a time in military format (e.g. 2145, 0713): ')

  if len(normaltime) != 4:
    print("Invalid number of digits. Add a 0 to the front if necessary.")
    return 0
  if normaltime > "2359":
    print("Invalid time")
    return 0
  if normaltime < "0":
    print("Invalid time")
    return 0

  normalhour = int(normaltime[:2])
  temphour = int(normalhour/2.4)
  normalmin = int(normaltime[2:])

  if normalmin > 59:
    print("Invalid time")
    return 0

  modmin = float((normalhour%2.4)*60) # number leftover minutes after modding hour
  metricmodmin = modmin * (100/144) # metric minute conversion
  metricnormalmin = float(normalmin * (100/144))
  newmin = int(metricnormalmin + metricmodmin)
  
  if newmin > 99:
    newmin = newmin - 100
    temphour = temphour + 1

  metrichour = "0"+str(temphour)
  if newmin < 10:
    metricmin = "0"+str(newmin)
  else:
    metricmin = str(newmin)

  print("Normal time is " + normaltime)
  print("Metric time is " + metrichour+metricmin)

#if __name__ == __'main'__:
main()

#0000 0100 0200 0300 0400 0500 0600 0700 0800 0900
#0000 0224 0448 0712 0936 1200 1424 1648 1912 2136
