# Cisco-Switch-Upgrade-Toolkit
usage:
./switch-toolkit input_config_file [-c primary_switch_num secondary_switch_num] [-m primary_switch_num secondary_switch_num]

options:
-c: combine
  This flag takes 2 24-port switches and makes them into 1 48-port
  switch.  If the optional switch num arguments are not provided, the
  lowest numbered 24-port switches will becombined.
  
  Ex. ./switch-toolkit input_file_config -c 1 3
  This will take switch 1 and switch 3 and make them into 1 48-port switch
  if they are both 24-port switches.
  
  Ex. ./switch-toolkit input_file_config -c
  This will take the two lowest numbered 24-port swtiches (say 1 and 2)
  and merge them into 1 48-port switch



-m: merge
  This flag takes 2 switches of any kind and tries to fit them both into
  1 switch of the same size as the primay switch.
  
  Ex. if primary_switch is a 24 port and secondary_switch is a 48 port
  switch, -m will try and merge both switches into a 24 port config.
