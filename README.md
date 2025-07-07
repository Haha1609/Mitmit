Mitmit 84 keys layout include Ano switch (5 buttons + rotary encoder) on both side. 

#ZMK STUDIO auto enable, no lock key needed.

#Split keyboard

#Wireless

#Super Mini Nrf52840 Pro Micro - #Nice! Nano v2 compatible

#Pointing key on navigation switch - #Mouse key

#5 way Navigation switch

#Composite driver - #ZMK composite driver to merge the matrix and the direct wired key

#Custom layout - #Custom shields - #Custom design




   
![Mitmit Keymap](keymap-drawer/Mitmit.svg)


***Direct Key must be placed on a separate row or column beside the main matrix.

***Each side's .overlay file must define the direct key separately.

***This overlay is based on the arrangement of &default_transform map.

Left Side overlay:

  -Choose the desired row using 
  
    row-offset = <target row>;
  
  -Set the col-offset based on how many columns the key is shifted on that row.

Right Side overlay:

  Depends on the direct key's position relative to the right shield:
  
  -If the direct key is on the left of the right shield, use:
  
    row-offset = <target row - 1>;
    
  -If it's not on the left (same or right), use:
  
    row-offset = <target row>;
    
  -On the selected row, start counting columns from (&default_transform { col-offset = <shifted RC>; }) to Adjust the col-offset to reach the target position.
