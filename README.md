# programming-class
import time

def fibrec (n):
    if n==0:
        return 0
    elif n==1:
        return 1
    else:
        return fibrec(n-1)+fibrec(n-2)


def fibnonrec(n):
      if (n == 0):
            return 0
      elif (n == 1):
            return 1
      elif (n == 2):
            return 1
      elif (n == 3):
            return 2
      elif (n > 1):
            fn = 0
            fn1 = 1
            fn2 = 2
            for i in range(3, n):
                fn = fn1+fn2
                fn1 = fn2
                fn2 = fn
            return fn
      else:
            return -1
        
def main():
    finalvalue = 30
    termvaluelist = []
    timelist = []
    for count in range(0, finalvalue + 1):
        start = time.clock()
        recresult = fibrec(count)
        timecalc = time.clock()
        timetaken = timecalc - start
        print(recresult, "  ", timetaken)       
    print()
    print()
    nr_terms = []
    nr_times = []
    for counttwo in range(0, finalvalue + 1):
        starttwo = time.clock()
        nonrecresult = fibnonrec(counttwo)
        endtwo = time.clock()
        timetaken_nr = endtwo - starttwo
        print(nonrecresult, "  ", timetaken_nr)


main()

