list = [34, 23, 54, 43, 53, 43, 99, 43, 74, 57, 82, 80, 17]

def mean(list):
	mean = sum(list) / len(list)
	return mean
  
mean(list)
output is 54.0
  
def median(list):
  clist = list[:]
  clist.sort()
  if len(clist)%2 == 0: 
      rightmid = len(clist)//2
      leftmid = rightmid - 1
      median = (clist[leftmid] + clist[rightmid])/2
  else:
      mid = len(clist)//2
      median = clist [mid]
  return median
  
median(list)
output is 53
  
def mode(list):
  count = {}
  for item in list:
      if item in count:
          count[item] = count[item]+1
      else:
          count[item] = 1
  countlist = count.values()
  maxcount = max(countlist)
  mlist = []
  for item in count:
      if count[item] == maxcount:
          mlist.append(item)
  return mlist
   
 mode(list)
 output is [43]
