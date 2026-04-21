# Linux Boot Process

   - Everything needs litle kind of push to get pumped up or to start. Like that Linux based OS as well as other Operating Systems also needs a
     push to start.

   - In this artical we are goind to know who and how OS get a push to pumped up.

   # Overview 
      
        Step 1: Power On.

        Step 2: Firmware Basic Input Output System(BIOS in old systems)/Unifide Extensible Firmware Interface(UEFI in moder systems)
                starts it loads Bootloader from disk.

        Step 3: Well known bootloader is GRUB(Grand Unified Boot Loader) which loads the kernal.

        Step 4: Kernla loads Operating System 

        Step 5: Then system manager handle further operations like to start process and all.

    # Detail

        1. Power On: when power supply starts within the hardware cpu starts, but cpu memory is blanck it does not no what to do.
                     The Code Segment and Instruction Pointer are set to address 0XFFFF0h. It has jum instruction which is map with 
                     address on ROM (BIOS ROM). Now BIOS/UEFI works starts.

        2. Firmware: There are two firmware but they perform task but UEFI is upgraded versio of BIOS we wil understand one by one.

                # BIOS:

                    - Stands for Basic Input Output System
                    
                    - Firstly it performs POST(Power-On Self Test):

                          - which is kind of dignostic test which sure that all hardware componets are good to go.

                          - It checks HDD'a, peripheral devices like keyboard, mouse, and ports as well.

                          - If something error occurs it warns by beeping the code.

                    - 
                    
       