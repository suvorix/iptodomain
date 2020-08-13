# iptodomain
<img src="https://cloud.githubusercontent.com/assets/6917066/21866468/6590ab3a-d818-11e6-89f7-609e2d8f1171.jpg" alt="iptodomain" height="228" width="504">

Description:

This tool allows you to extract domains from a IP range, using the historic information archived in Virustotal(using API key). It is usefull if you want to know what domains are behind of this IP address, for example in bug bounty programs one of the first steps is to extract subdomains, this tool can help with this task... first you have to find out the IP range that uses a company. Many times a good start point is to know the AS (Autonomus system) number, then you can find the IP range.


To use this tool you have to set up your Virustotal API key in the code, please sign up on Virustotal then they provide you the API key.


Example:
python iptodomain.py -i 103.22.201.25  -f 103.22.201.255  -o 103.22.200.255.txt -v -r IPsCF.txt


Options:


python iptodomain.py 
usage: iptodomain.py [-h] [-i FIRST_IP] [-f LAST_IP] [-w FILE2] [-o FILE1]
                     [-v] [-r FILE3]

This tool allow to extract domains from IP information on Virustotal and save
the output in a file. You have to set up the IP range where you like to
extract domain or subdomain. Additionally it is neccesary set up your
VirusTotal API key in the code.

optional arguments:
  -i FIRST_IP  Первый IP диапазона, который вы хотите просканировать.
  
  -f LAST_IP   Последний IP диапазона, который вы хотите просканировать.
  
  -w FILE2     Имя файла, в котором будет сохранён отчёт со всеми доменами и их IP.
             
  -o FILE1     Имя файла, в котором будут сохранены все найденные домены.
  
  -v           Показывать больше информации во время сканирования.
  
  -r FILE3     Имя конечного отчёта без повторяющихся результатов доменов.
  
  This tool was created by:
  
  Juan Esteban Valencia Pantoja
