### Change size of notebook width
from IPython.core.display import display, HTML
display(HTML("<style>.container { width:90% !important; }</style>"))

### Auto reload packages
%load_ext autoreload
%autoreload 2
