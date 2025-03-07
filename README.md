Open terminal run:
set-executionpolicy Unrestricted -Scope Process    
python -m venv venv         
venv\Script\Activate        
pip install -r requirements.txt
  

If Cuda not detected
pip uninstall torch torchvision torchaudio
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
