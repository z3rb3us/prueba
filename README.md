# prueba
pruena


#colours
greenColour="\e[0;32m\033[1m"
endColour="\033[0m\e[0m"
redColour="\e[0;31m\033[1m"
blueColour="\e[0;34m\033[1m"
yellowColour="\e[0;33m\033[1m"
purpleColour="\e[0;35m\033[1m"
turquoiseColour="\e[0;36m\033[1m"
grayColour="\e[0;37m\033[1m"



function mkt(){
        mkdir {nmap,content,scripts,tmp,exploits}
}

function extractPorts(){

        echo -e "\n${yellowColor[*] Extracting information...${endColour}\n"
        ip_address=$(cat allPorts | grep -oP '\d{1,3}\.\d{1,3}\.\d{1,3}\-\d{1,3}' | sort -u)

        echo -e "\t${blueColour}[*] IP Address: ${endColour}${grayColour}$ip_address${endColour}"
        echo -e "\t${blueColour}[*] Open ports: ${endColour}${grayColour}$open_ports${endColour}\n"

        echo $open_ports | xclip -sel clip

        echo -e "${yellowColour}[*] Ports has been copied to clipboard!${endColour}\n" 
