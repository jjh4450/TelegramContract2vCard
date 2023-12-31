# TelegramContract2vCard
## make telegram contacts to vCard
### install
```sh
pip install TelegramContract2vCard
```
### Usage
1. Export your telegram contacts to `contacts.html` or `result.json`(download step is below)
2. get path of `contacts.html` or `result.json` file
3. Run this script
```py
from TelegramContract2vCard import html2vcf, json2vcf, html2dict, json2dict, dict2vcf
```
```py
# make html or json to vcf
# use path from step 2
html2vcf('./contacts.html')
json2vcf('./result.json')

# you can also make html or json to vcf with custom name and custom path
html2vcf('contacts.html', 'custom_name', 'your/path/to/save/vcf')
json2vcf('result.json', 'custom_name', 'your/path/to/save/vcf')

# make json and html to dict
html2dict('contacts.html')
json2dict('result.json')
#result is like this
# {name: {phone: phone_number, date: date}, ...}

# make dict that is made by html or json to vcf
contract = html2dict('contacts.html')
dict2vcf(contract)
#or
dict2vcf(contract, 'custom_name', 'your/path/to/save/vcf')
```
4. You will get contacts.vcf
5. Import contacts.vcf to your phone
6. Enjoy!
---
### download contacts.html or result.json
1. Open Telegram Desktop
2. Click `Settings`  
![step1](./img/step1.png)
---
3. Click `Advanced`  
![step1](./img/step2.png)
---
4. Click `Export Telegram Data`  
![step1](./img/step3.png)
---
5. Click `Export contacts`  
**you can choose `HTML` or `JSON` below `Export contacts`**  
![step1](./img/step4.png)
6. you will get `contacts.html` or `result.json` in your download folder
---
### Note
2. This script is tested on `Windows 11` and `Telegram Desktop 4.8.10`
