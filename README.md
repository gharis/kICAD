# kICAD

## Getting Started
https://kicad-pcb.org/help/getting-started/

## Essential and concise guide to mastering KiCad for the successful development of sophisticated electronic printed circuit boards.
https://docs.kicad-pcb.org/5.1/en/getting_started_in_kicad/getting_started_in_kicad.html

## OTHER
https://docs.kicad-pcb.org/#_getting_started
https://docs.kicad-pcb.org/5.1/en/eeschema/eeschema.html


# Component Libs
Digi key kicad lib 
https://github.com/Digi-Key/digikey-kicad-library 

## Ultra librarian from Digi key open sorce 
https://app.ultralibrarian.com/search?queryText=ina293 

## Importing ultra librarian 
https://app.ultralibrarian.com/content/help/?kicad.htm 

## Importing to Ki Cad from ultralibrarian 
https://youtu.be/Wvwwmn0X-h8?list=PLkqC31nn-k7mujTz7vwejPDVVnKrZG4A4 

## Component Libs for ki cad 
https://componentsearchengine.com 

## SeeedStudio ki cad lib 
https://www.seeedstudio.com/opl.html 

# Fabrication files 
## Ki cad BOM inbuilt generator 
https://www.youtube.com/watch?v=b6PAW7GPuYs&ab_channel=ContextualElectronics 

## Output Files For Manufacturing 
https://www.youtube.com/watch?v=3oL6ZdCUZvA&ab_channel=ContextualElectronics 

## Extra 
KiCad STM32 Hardware Design and JLCPCB Assembly 
https://www.youtube.com/watch?v=t5phi3nT8OU&ab_channel=Phil%E2%80%99sLab 

# Practical Aspects on Design For Manufacturing
## PCB layout settings for PCBWay
    • clearance copper PAD to silkscreen = 0.1mm 
    • text silk height = 0.8mm 
    • text silk width = 0.8mm 
    • text silk thickness = 0.16mm 
    • text F.Fab height = 0.4mm 
    • text F.Fab width = 0.4mm 
    • text F.Fab thickness = 0.1mm 
    • track path witdh min = 0.13mm 
    • track path clearance min = 0.2mm 
    • via dril min = 0.3mm 
    • via diameter min = 0.45mm 
    • F.Fab = assembly drawing layer 
    • F.Crtyad = physical ic keep out  
## Important layers in footprint , these should be edited for DFM requirements
    • %R reference - f.b.SilkS 
    • component boundary - f.b.SilkS 
    • %R reference - f.Fab - assembly layer 
    • component boundary - f.Fab - assembly layer 
    • physical ic keep out - Crtyrd 
    • component direction (LED/diodes)- f.Fab - assembly layer 
    
### Foot print design tips 

    • Libs from snap eda or ultrabroad 
    • Edit foot prints 
    • Fab layer – ref designators %R 
         • Highet 0.5mm 
         • Width 0.5mm 
         • Thickness 0.15mm 
    • Fab layer outline of component 
    • Delete existing fab layer – hard to see in printed format 
    • Draw in fab layer on top of cortyad 
    • Keep fab layer designator inside the fab layer outline  
    • Fab layer important 
         • Led cathode 
         • Diode cathode 
         • 1st pin of IC
         • Pin header pin no 1 
         • Multi pin connecter pin no 1 
         • Electrolyte capacitor cathode 
         • Etc.. 
    • Silk screen designator is not must for mass production or for pcb house   
    
## PCB outer cut/ margin  
    • Edge.Cuts 
# Manufacturing file generation in Ki CAD 
    • https://docs.oshpark.com/design-tools/kicad/ 
## Manufacturing files  generation in Ki CAD 
    • Gerbers  
        • Pcbnew->File->Gerbers 
    • Drill file  
        • Pcbnew->File->Gerbers ->Drill file 
    • Assembly drawing (F.Fab)  
        • Pcbnew->File->Gerbers 
    • Pick and place (.pos), Centroid file   
        • Pcbnew->File->Fabrication Outputs -> Footprint position (.pos) 
    • BOM  
        • Easchema->Bill of materials 
## Manufacturing file list for PCB house 
    • Assembly drawing.pdf 
    • F_fab.gbr 
    • Drilfile.drl 
    • Pickandplac.pos 
    • Gerbers.rar 
    • BOM.xlxs 
## Gerbers files for PCB House
    • Top
    • Bottom
    • B.SilkS
    • F.SilkS
    • B.Mask
    • F.Mask
    • Edge.Cuts
## plot settings
    • tick Plot foot print values
    • tick Plot foot print referance
    • tick Exclude PCB Edgelayer from other layers
    • tick format 4.6(unit mm)
## drill files generation
    • tick Units - in
    • tick PostScript
    • tick Decimal format
    • tick Merge pth and npth
    • tick origin absolute
# BOM - Design For Manufacturing
## PCB assembly services expect BOM with the following fields  
Following values should be set in symbol properties

    • Designator 
    • Qty 
    • Manufacturer 
    • Manufacturer Part Number 
    • Description 
    • Case / Package 
    • Type - SMD ,BGA,LCC,OR TH 
    • Your Instructions / Notes/ Comments
    • Top/Bottom 
    • points (number of contacts the IC has in each board) 
    • Total points (number of contacts per BOM line has) 
## BOM Samples
    • Seed 
http://support.seeedstudio.com/knowledgebase/articles/1886734-how-do-i-prepare-the-bill-of-materials-bom-file

    • pcbway 
https://www.pcbway.com/blog/PCB_Assembly/How_to_Build_a_BOM__Bill_Of_Materials_.html
# Time estimations for PCB manufacturer 
    • Takes 2- 3 days to the finalized quotation from any PCB house for assembly service   
    • PCB board manufacturing 2 - 3 days   
    • PCB assemble 4 weeks or 12 - 30 days  
    • Shipping 5 days or 24 hours  
# PCB house cost comparison for sample 10x PCBs
With components assembly/ components by pcb house / 2 layer / single side components

    • SeeedStudio $485, production 24 days
    • PCBway  $330, production 35 days
    • 7PCB/BITTELE $770, production 14 days
    • AllPCB $480, production 25 days
    • PCBbee $530, production 12 days
    • STHL $580, production 28 days
    • PCBgogo $370, production 20 days
    • NextPCB $415, production 30 days
