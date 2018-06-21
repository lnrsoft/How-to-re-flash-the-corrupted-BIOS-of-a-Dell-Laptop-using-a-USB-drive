This is the latest version of the How re-flash the corrupted BIOS of a Dell Inspiron Laptop article.

<center><a href="https://lnrsoft.com/wp-content/uploads/2017/07/Repair-Corrupted-BIOS-Firmware.jpg"><img class="aligncenter" src="https://lnrsoft.com/wp-content/uploads/2017/07/Repair-Corrupted-BIOS-Firmware-768x512.jpg" alt="Repair-Corrupted-BIOS-Firmware" width="700" height="467" /></a></center>

<span style="color: #ff0000;">There is, however, no guarantee that the following method will also work for you, as reading this sentence you agree that I am taking no responsibility of any damage caused by the following procedure. </span>

CORRUPTED BIOS AND HOW TO FLASH IT?
How to Recover from a disastrous BIOS update?
How to Flash a Corrupted Dell Inspiron Laptop BIOS?

Simply follow this procedure to re-flash failed BIOS update on a Dell Inspiron (n5010 model in my case) laptop. Presumably the following method also works on almost all other Dell models.
<h3>Phase 1.</h3>
<ul>
 	<li>First of all you have to download the correct firmware from Dell Official Website:
<a href="http://downloads.dell.com/bios/N5010A15.EXE" target="_blank" rel="noopener nofollow">http://downloads.dell.com/bios/N5010A15.EXE</a>
</li>
 	<li>Use Windows Command Prompt (run as administrator) to extract the required firmware files.</li>
 	<li>C:\&gt;cd /Downloads</li>
 	<li>C:\&gt;N5010A15.EXE /writehdrfile</li>
 	<li>C:\&gt;N5010A15.EXE /writeromfile</li>
</ul>
<center><a href="https://lnrsoft.com/wp-content/uploads/2016/12/writehdrfile-e1499528716158.png"><img class="aligncenter" src="https://lnrsoft.com/wp-content/uploads/2016/12/writehdrfile-e1499528716158.png" alt="" width="680" height="397" /></a></center>
<ul>
 	<li>Rename the newly created N5010A15.HDR and N5010A15.ROM files to N5010.HDR and N5010.ROM.</li>
 	<li>Format an USB thumb-drive to FAT and copy the N5010.HDR, N5010.ROM files on it. You do not need to create bootable USB drive.
<span style="color: #ff0000;">*UPDATE: most of the time I hear feedback about this method people add a comment that they formatted their USB thumb-drive to FAT16 as the FAT32 file system did NOT work.</span></li>
</ul>
<h3>Phase 2.</h3>
<ul>
 	<li>Shutdown your faulty laptop if is is still running with the black screen.</li>
 	<li>Remove the battery</li>
 	<li>Remove the CMOS battery</li>
 	<li>Disconnect the power supply.</li>
 	<li>Insert the USB drive in the USB port.
<span style="color: #ff0000;">*UPDATE: According to the feedback on this method most people use the left USB socket, as the rest of the USB sockets might not functioning at this state.</span></li>
</ul>

<span style="color: #ff0000;">*Note: There are few cases reported about not active USB ports. Simply try to use other USB port if you notice or suspect that the system cannot read the USB drive from the port you plugged it. Use USB drive with activity LED if you have one, the blinking LED will confirm that the system reads data from your USB drive.</span>

<h3>Phase 3.</h3>
<ul>
 	<li>Press and keep hold the END key on the keyboard for your faulty laptop.</li>
 	<li>Plug the DC power connectors (power plug) into the laptop.</li>
 	<li>After a few seconds your faulty laptop will start itself and will re-flash its corrupted BIOS and automatically reboot.</li>
 	<li>You can release the END key after the flashing process started. A USB drive with an activity LED can confirm that the BIOS flashing process started. The complete re-flashing process will take no longer than 60 maximum 90 seconds.</li>
</ul>
<article id="post-1318" class="post-1318 post type-post status-publish format-standard hentry category-hardware tag-bios-recovery tag-dell tag-dell-inspiron-n5010 tag-hardware tag-inspiron tag-inspiron-n5010 tag-inspiron-n5010-bios tag-n5010 tag-n5010-rom tag-roland-ihasz ast-article-single">
<div class="ast-post-format- ast-no-thumb single-layout-1">
<div class="entry-content clear">

<em>Your comments and suggestions would be greatly appreciated.</em>

&nbsp;

<strong>
<span style="color: #ff0000;">WARNING! </span></strong><span style="color: #ff0000;"><em>I am taking no responsibility of any damage caused by the following NOT TESTED procedure. Try this PhoenixTool method when the /writeromfile and /writehdrfile commands are not give you any result.</em></span>

This procedure never been tested by myself, however quite a few people were asked me about how to extract ROM files from other system BIOS files without the /writeromfile and /writehdrfile commands mentioned above in my step by step guide. <em>
</em>

Let’s take an example of Inspiron N7010 BIOS. In this case the usual /writeromfile and /writehdrfile commands will not work.
You’ll need <a href="https://www.7-zip.org/">7-Zip</a> or<a href="https://www.legroom.net/software/uniextract"> Universal Extractor</a> and <a href="https://forums.mydigitallife.net/threads/tool-to-insert-replace-slic-in-phoenix-insyde-dell-efi-bioses.13194/">PhoenixTool</a> to extract/create rom files from the <a href="https://downloads.dell.com/bios/R301250.exe">R301250.exe</a> System BIOS file.
<h3>Phase 1.</h3>
<ul>
 	<li>Download the<a href="https://downloads.dell.com/bios/R301250.exe"> R301250.exe</a> (2969 KB) file from the official source ( http://www.dell.com/support/home/uk/en/ukbsdt1/drivers/driversdetails?driverId=R301250 )</li>
</ul>
<h3>Phase 2.</h3>
<ul>
 	<li>Extracting the <a href="https://lnrsoft.com/files/7010_A11.EXE.zip">7010_A11.EXE</a> (7944 KB) file from the original <a href="https://downloads.dell.com/bios/R301250.exe">R301250.exe</a> (2969 KB) file using <a href="https://www.legroom.net/software/uniextract">Universal Extractor</a> (source: https://www.legroom.net/software/uniextract ). In numerous cases <a href="https://www.7-zip.org/">7-Zip</a> able extract exe files as well.
&nbsp;
 <br>
  <center><a href="https://lnrsoft.com/wp-content/uploads/2018/06/universal-extractor.png" rel="lightbox[1318]"><img class="aligncenter wp-image-4433 size-medium" src="https://lnrsoft.com/wp-content/uploads/2018/06/universal-extractor-300x164.png" sizes="(max-width: 300px) 100vw, 300px" srcset="https://lnrsoft.com/wp-content/uploads/2018/06/universal-extractor-300x164.png 300w, https://lnrsoft.com/wp-content/uploads/2018/06/universal-extractor.png 307w" alt="" width="300" height="164" /></a><center>extracting</center>
 
 &nbsp;

<h3>Phase 3.</h3>
<ul>
 	<li>
<ul>
 	<li>Extracting *.rom , *.bin files using <a href="https://forums.mydigitallife.net/threads/tool-to-insert-replace-slic-in-phoenix-insyde-dell-efi-bioses.13194/">PhoenixTool 2.73</a> (Phoenix/Dell/EFI SLIC Mod v2.73 , source: <a href="https://forums.mydigitallife.net/threads/tool-to-insert-replace-slic-in-phoenix-insyde-dell-efi-bioses.13194/">https://forums.mydigitallife.net</a> )</li>
 	<li>In the <a href="https://forums.mydigitallife.net/threads/tool-to-insert-replace-slic-in-phoenix-insyde-dell-efi-bioses.13194/">PhoenixTool</a> select and add your<a href="https://lnrsoft.com/files/7010_A11.EXE.zip"> 7010_A11.EXE</a> file as the Original BIOS, then set Manufacturer to Dell and add the DELL.BIN SLIC file (this can be found in PhoenixTool273/SLIC21 folder)</li>
 	<li><strong>Note!</strong> In order to extract rom files, you’ll need to tick/select from Advanced options under control options “Extract modules when verifying” then press done and verify. It will then create a DUMP folder next to your <a href="https://lnrsoft.com/files/7010_A11.EXE.zip">7010_A11.EXE</a> file. <a href="https://www.microsoft.com/en-us/download/details.aspx?id=21"> Microsoft .NET Framework 3.5</a> required for <a href="https://forums.mydigitallife.net/threads/tool-to-insert-replace-slic-in-phoenix-insyde-dell-efi-bioses.13194/">PhoenixTool 2.73</a>.
  <center><a href="https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool.png" rel="lightbox[1318]"><img class="aligncenter wp-image-4430 size-medium" src="https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool-300x129.png" sizes="(max-width: 300px) 100vw, 300px" srcset="https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool-300x129.png 300w, https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool-768x330.png 768w, https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool-1024x440.png 1024w, https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool.png 1347w" alt="" width="300" height="129" /></a></center>
   <br> &nbsp;
   <center><a href="https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool_results.png" rel="lightbox[1318]"><img class="aligncenter wp-image-4429 size-medium" src="https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool_results-300x149.png" sizes="(max-width: 300px) 100vw, 300px" srcset="https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool_results-300x149.png 300w, https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool_results-768x381.png 768w, https://lnrsoft.com/wp-content/uploads/2018/06/PhoenixTool_results-1024x508.png 1024w" alt="" width="300" height="149" /></a><center></center></li></center>
</ul>
</li>
</ul>
Useful resources:
<ol>
 	<li><a href="http://www.atmel.com/images/doc0180.pdf" target="_blank" rel="noopener nofollow">AT24C01A EEPROM datasheet</a></li>
 	<li><a href="http://linux.dell.com/repo/hardware/dsu/" target="_blank" rel="noopener nofollow">DELL EMC System Update for Windows and Linux</a></li>
 	<li><a href="https://www.flashrom.org/Flashrom" target="_blank" rel="noopener nofollow">Flashrom</a> or <a href="https://www.flashrom.org/Qflashrom" target="_blank" rel="noopener nofollow">Qflashrom</a></li>
 	<li><a href="https://www.coreboot.org/Superiotool" target="_blank" rel="noopener nofollow">Superiotool – Detect which Super I/O you have on your mainboard</a></li>
 	<li><a href="https://www.dell.com/support/article/us/en/04/SLN300716/bios-recovery-options-on-a-dell-pc-or-tablet?lang=EN" target="_blank" rel="noopener nofollow">Official Dell BIOS Recovery options</a></li>
 	<li><a href="https://www.dell.com/support/article/uk/en/ukbsdt1/SLN129956/what-is-bios-and-how-to-download-and-install-the-latest-bios-?lang=EN" target="_blank" rel="noopener nofollow">Dell: What is BIOS and How to Download and Install the latest BIOS?</a></li>
 	<li><a href="http://en.community.dell.com/techcenter/enterprise-client/w/wiki/12237.64-bit-bios-installation-utility" target="_blank" rel="noopener nofollow">Dell: 64-bit BIOS Installation Utility</a></li>
 	<li><a href="http://rweverything.com/">RW-Everything</a></li>
 	<li><a href="https://forums.mydigitallife.net/threads/tool-to-insert-replace-slic-in-phoenix-insyde-dell-efi-bioses.13194/">PhoenixTool 2.73</a></li>
 	<li>
<div class="row">
<div>

<a href="http://www.dell.com/support/home/uk/en/ukbsdt1/Drivers/DriversDetails?driverId=K33TK"><span class="h2">Dell Client Configuration Utility</span></a>

</div>
</div></li>
</ol>
The reason behind writing this BIOS recovery article is provide some helpful info/advice/starting point to everyone facing with the same issue. I hope this procedure helped you to save time / money as you were able to successfully recover your corrupted BIOS.
    &nbsp;

If you'd like to support me please make a donation to my BTC address 15JmQsaxyaxsEZf5WJVDxibLkLJFWtz83y 
<br>Your support is greatly appreciated.
    &nbsp;

<a href="bitcoin:15JmQsaxyaxsEZf5WJVDxibLkLJFWtz83y"><img class="aligncenter wp-image-4436 size-full" src="https://lnrsoft.com/wp-content/uploads/2017/06/15JmQsaxyaxsEZf5WJVDxibLkLJFWtz83y-1.png" sizes="(max-width: 175px) 100vw, 175px" srcset="https://lnrsoft.com/wp-content/uploads/2017/06/15JmQsaxyaxsEZf5WJVDxibLkLJFWtz83y-1.png 175w, https://lnrsoft.com/wp-content/uploads/2017/06/15JmQsaxyaxsEZf5WJVDxibLkLJFWtz83y-1-150x150.png 150w" alt="" width="175" height="175" /></a><br>
This work (How to re-flash the corrupted BIOS of a Dell Laptop using only a USB drive, by Roland Ihasz) is free of known copyright restrictions.

</div>
</div>
</nav>
