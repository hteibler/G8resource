# G8resource
create an excel-sheet out of Resource consumption info
with Cloudspaces and VMs

by start and end date
per account

# Steps to do

you need a proper installed pythen3 environment,
for modules see code


# 1.) Accessing the openvcloud
  For accessing the OVC you need your credentials from IYO
  go to itsyou.online and copy your API key
  and put this values in environment variables

  export CLIENT_ID="...."
  export CLIENT_SECRET="....."

# 2.) Which Data do you want?
  Set this environment variables
  (example for October 2018)

  export START=$(date -d '10/01/2018 00:00:01' +"%s")
  export END=$(date -d '10/30/2018 23:59:59' +"%s")

# 3.) Excel files
  template file
  this will be copied to the target file
  and filled with data
  you can adjust you values (prices) in the "tab" param ( yellow fields)

  export XLS_FILE_TPL="consumption_tpl.xlsx"

  output file
  (example)
  export XLS_FILE="consumption_2018_10.xlsx"

# 4.) for which account do you want the data
  List your accessible accounts

  python3 export_all_in_zip.py List

# 5.) create the final excel sheet

  python3 export_all_in_zip.py <account_id>

  you can still adjust you prices!
