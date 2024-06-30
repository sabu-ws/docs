# Yara Rules
!!! info "Info"

    Files are stored in `/sabu/server/core/yararules`  
    The script is stored in `/sabu/server/core/yararules/index_gen.sh`  
    (During execution, the script scans subfolders and creates a Yara index for the rules in that folder. Then it creates an index "index.yar" with all the Yara rules.)

## Create custom Yara rules
- Create folder with your name or company in `/sabu/server/core/yararules`
- Add your Yara rule in this folder
- Execute script **index_gen.sh** in `/sabu/server/core/yararules`  
(Script update index.yar and create custom XXX_index.yar with your folder name and include yara's files)

!!! success "Success"

    Now your can use your SABU with new Yara Rule.

## Update / Remove Yara rules
- Update or remove your Yara rule
- Execute script **index_gen.sh** in `/sabu/server/core/yararules`  

!!! success "Success"

    Your Yara rule has been update/remove.