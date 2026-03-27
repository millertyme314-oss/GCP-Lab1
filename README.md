# GCP-Lab1
Created a VM instance, performed health, metadata &amp; validity checks

## Generating a VM instance:
> Navigate to and login to GCP Console

> Create VM (search "VM" in search bar, "Create VM" from products,  or select "Hamburger" icon -> Compute engine -> VM Instances)
  
> [Machine Configuration] tab: Region is us-central1 (Iowa) or Sao Paolo --> DEFAULT!!

> [OS and storage] tab: Make sure Debian OS (Linux platform) is the image type
  
> [Data Protection] tab: No Backups (This is a Lab ONLY...this is NOT for production!)

> [Networking] tab: Check "Allow HTTP traffic" only
 
> [Observability] & [Security] tabs: Leave ALONE!!
  
> [Advanced] tab: Paste the copied user script into "Automation" field

> Click "Create"

> VM Homepage should generate 👈 Screenshot (Deliverable)

## Instance Health and Metadata checks:
> From the "VM Instances" screen, look for the "Connect" tab of the desired instance

> Under the Connect tab, click on the "SSH" option to ssh into the VM

> At the pop-up, select "Authorize"

> Once the ssh portal populates, type in "curl -s localhost/healthz" to check instance health [Output = "Ok" ]

> Next, type in "curl -s localhost/metadata | jq ." to check instance metadata [Output = Shows instance data ]

## Instance validation (HW deliverables):
> While the instance is running, open Gitbash/Terminal (Run as Administrator)

> Navigate to an empty folder and create a new file named "gate_gcp_vm_http_ok.sh"

> From this point in the terminal, type "code ." to open VSCode

> In VSCode, navigate to the "gate_gcp_vm_http_ok.sh" and paste the appropriate script & save the file

> In the Google Console, copy the "External IP" of your instance

> Next, type in "Ctrl + J" to open VSCode's terminal interface and type "VM_IP=[copied External IP] ./gate_gcp_vm_http_ok.sh" & press Enter

> Lab 1 Gate Result should = PASS, along with 5 other checks 👈 Screenshot 

> "badge.txt" & "gate_result.json" files should generate within the directory/folder

>  Next, select the "gate_result.json" file 👈 Screenshot (Deliverable)

> Lastly, type in "cat badge.txt" [Output = "GREEN" ] 👈 Screenshot (Deliverable)


 
![](https://miro.medium.com/1*NKN0Oh5-2MaR2q5XJZ1UYA.jpeg)
