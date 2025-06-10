import sys
sys.path.append('C:/Users/lenovo/Python/climQMBC')

from climQMBC.methods import QM, DQM, QDM, UQM, SDM
from climQMBC.report import report
import pandas as pd
import numpy as np

variable = 'pr'
mult_change = 0
allow_negatives = 1
SDM_var = 1

# Load observed and model data.
obs = pd.read_csv(f'C:/Users/lenovo/Desktop/deneme/obs_{variable}_M.csv')[[variable]].values
mod = pd.read_csv(f'C:/Users/lenovo/Desktop/deneme/mod_{variable}_M.csv')[[variable]].values


import sys
sys.path.append('C:/Users/lenovo/Python/climQMBC')

from climQMBC.methods import QM, DQM, QDM, UQM, SDM
from climQMBC.report import report
import pandas as pd
import numpy as np


frq = 'M'
variable = 'pr'
mult_change = 0
allow_negatives = 0
SDM_var = 1
y_init = 0
y_wind = 0
user_pdf=False
pdf_obs=None
pdf_mod=None

# Load observed and model data.
obs = pd.read_csv(f'C:/Users/lenovo/Desktop/deneme/obs_{variable}_M.csv')[[variable]].values
mod = pd.read_csv(f'C:/Users/lenovo/Desktop/deneme/mod_{variable}_M.csv')[[variable]].values


qm_series, dqm_series, qdm_series, uqm_series, sdm_series = report(
    obs, mod, SDM_var, mult_change, allow_negatives, 
    y_init, y_wind, user_pdf, pdf_obs, pdf_mod


import sys
sys.path.append('C:/Users/lenovo/Python/climQMBC')

from climQMBC.methods import QM, DQM, QDM, UQM, SDM
from climQMBC.report import report
import pandas as pd
import numpy as np


frq = 'M'
variable = 'pr'
mult_change = 0
allow_negatives = 0
SDM_var = 1

# Load observed and model data.
obs = pd.read_csv(f'C:/Users/lenovo/Desktop/deneme/obs_{variable}_M.csv')[[variable]].values
mod = pd.read_csv(f'C:/Users/lenovo/Desktop/deneme/mod_{variable}_M.csv')[[variable]].values

qm_series, dqm_series, qdm_series, uqm_series, sdm_series = report(
    obs, 
    mod, 
    SDM_var, 
    mult_change=mult_change, 
    allow_negatives=allow_negatives, 
    fun=['QM', 'DQM', 'QDM', 'UQM', 'SDM'], 
    y_init=0, 
    y_wind=0, 
    user_pdf=False, 
    pdf_obs=None, 
    pdf_mod=None
)


import sys
sys.path.append('C:/Users/lenovo/Python/climQMBC')

from climQMBC.methods import QM, DQM, QDM, UQM, SDM
from climQMBC.report import report
import pandas as pd
import numpy as np

frq = 'M'
variable = 'pr'
SDM_var = 1

# Load observed and model data.
obs = pd.read_csv(f'C:/Users/lenovo/Desktop/deneme/obs_{variable}_M.csv')[[variable]].values
mod = pd.read_csv(f'C:/Users/lenovo/Desktop/deneme/mod_{variable}_M.csv')[[variable]].values

# report fonksiyonunu çağırırken kullanılabilecek parametreler doğrultusunda kodunuzu güncelleyin
qm_series, dqm_series, qdm_series, uqm_series, sdm_series = report(
    obs, 
    mod, 
    SDM_var, 
    fun=['QM', 'DQM', 'QDM', 'UQM', 'SDM'], 
    y_init=0, 
    y_wind=0, 
    user_pdf=False, 
    pdf_obs=None, 
    pdf_mod=None
)

import sys
sys.path.append('C:/Users/lenovo/Python/climQMBC')

from climQMBC.methods import QM, DQM, QDM, UQM, SDM
from climQMBC.report import report
import pandas as pd
import numpy as np

frq = 'M'
variable = 'pr'
SDM_var = 1

# Load observed and model data.
obs = pd.read_csv(f'C:/Users/lenovo/Desktop/deneme/obs_{variable}_M.csv')[[variable]].values
mod = pd.read_csv(f'C:/Users/lenovo/Desktop/deneme/mod_{variable}_M.csv')[[variable]].values

# report fonksiyonunu çağırırken kullanılabilecek parametreler doğrultusunda kodunuzu güncelleyin
qm_series, dqm_series, qdm_series, uqm_series, sdm_series = report(
    obs, 
    mod, 
    SDM_var, 
    fun=['QM', 'DQM', 'QDM', 'UQM', 'SDM'], 
    y_init=0, 
    y_wind=0, 
    
   
)

qm_series_df = pd.DataFrame(qm_series)
qm_series_df.to_csv('qm_series_output.csv', index=False)


    



