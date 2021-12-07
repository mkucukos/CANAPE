# import pandas and numpy
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import scipy.io



f = h5py.File('somefile.mat','r')


# crete a sample dataframe for Mooring_T1
data = pd.DataFrame({

    'yearday' :     [320, 330, 340, 350, 360, 370, 380,390,400,410],
    'mean_ice_thickness' : [0.51,0.62,0.68,0.73,1.23,0.81,1,1.35,1.24,1.04],
    'max_ice_thikcness' :    [7, 5.92, 9.31, 4.83, 11.3, 8.28,7.61,8.85,11.34,7.37],
    'std_ice_thickness' :  [0.66, 0.44, 0.46, 1.21, 0.71, 0.51,0.66,1.05,1.13,0.57],
})

# view the ice thickness

# select mean ice thickness larger than 0.75
data.loc[data.mean_ice_thickness >= 0.75]

yearday=[320, 330, 340, 350, 360, 370, 380,390,400,410]
mean_ice_thickness=[0.51,0.62,0.68,0.73,1.23,0.81,1,1.35,1.24,1.04]
std=[0.66, 0.44, 0.46, 1.21, 0.71, 0.51,0.66,1.05,1.13,0.57]

plt.plot(yearday,mean_ice_thickness,'bo-')

plt.errorbar(yearday, mean_ice_thickness, std, marker='s', mfc='red',
         mec='green', ms=5, mew=4)


plt.xlabel('yearday')
plt.ylabel('mean ice thickness')

plt.show()
