# iis-sinica-report
The research topic is **The Enhancement on Anti-Evasion Techniques in Cuckoo Monitor**.\
This research was under the internship at **Institute of Information Science, Academia Sinica** from Jul 2022 to Aug 2022.\
Full version report is uploaded as [The_enhancement_on_Anti_Evasion_Techniques_in_Cuckoo_Monitor.pdf].(The_enhancement_on_Anti_Evasion_Techniques_in_Cuckoo_Monitor.pdf)\
If there is a need to retrieve codes or details mentioned in the report, please contact me.

# Introduction
Some malware programs have techniques to prevent themselves from being analyzed, so as to make not only static but dynamic analyzer tools become useless.\
For example, malware program designer uses some tools, like ConfuserEx, to obfuscate their code. Therefore, when analysts are trying to perform reverse engineering to these malware programs, they have to spend a lot of efforts on deobfuscating the obfuscated code.\
As for dynamic analysis, malware programs have other techniques to make themselves invisible. If malware programs are inside virtual machines or sandboxes, they may alter their behavior to be benign or conceal core functions, which is called sandbox/VME evasion. Commonly, malware programs check whether System Information, Registry, Hardware and etc. contain some special values, to confirm that they are inside or outside virtual machines or sandboxes.\
If malware programs behave like benign programs when they are inside virtual machines or sandboxes, it is difficult for dynamic analysis tools (Cuckoo Sandbox) to record their behaviors. Therefore, I have to figure out how to prevent these malware programs from evading from being recorded.\
I first not only performed reverse engineering to a malware program, but also reviewed related websites, in order to understand what kind of evasion techniques were commonly used. Then, I attempted to delve into how Cuckoo Sandbox worked, and found a way to prevent malware programs from being recorded, which enhanced the analysis ability of Cuckoo Monitor. Finally, I proposed a framework to simplify the redundant procedures that, when finding new evasion techniques, analysts appended these techniques into the source code and compiled.\
