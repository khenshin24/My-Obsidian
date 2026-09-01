
wireguard to access the production


identityprod user related
registryprod registry related

more on request i


payments table
*in address current and permanent change same


*Acccount deletion req
	username email and tin add _ at the last 
is_approved remove

*Payment
	  Payment pay_receipt table if exist
	 notices table  check if exist 
	 check in billling payment if used
	billing table if exist 


CERT use override payment

if Receipt number didn't exist
	Billing_payment table -> trans_num = 'PAY-251111000160' get the id 
        Billings table -> billing_payment_id = '269604e0-4afb-4df3-a4f5-c89925f9418f' //id of the billing_payment data
		check the ref_trans_num if same the ppsr-number
		if the data is sync run the seeder/markaspaid

	if the billing table didn't exist the data the user retry to paid again then ask press to link the the billing





payment Request
	check the notice if nag eexist
	check the payment if nag eexist
	 then run the api to bruno




Generate Notice Registration Report
	Branch
		sprint 13-3
	notice table 
		crtd_trans_num = 'PPSR-250904000158'
	notice_reports
	    notice_id = '7d72424c-043d-434f-a10f-71f5b51713da'
	    
	  in report type 
	  missing is 'NOTICE_REG_CREATE'
	  then 
	  
	  copy the id go to seed replace the id 
	  then run the seed in Bruno
	  http://localhost:8002/seeder/notice-creation-report
  

remark change request 
		un check the is_for_approval then say to client to re update the remarks


Multiple data ing payment receipt
"NOTE"
		if wala sa billing go goods pag wala sa billing na data proceed to payment transaction

	check the null data in remarks column
	copy the id 
	table billing payment check 
	then check the billing copy morph_id
	then paste to the notice id = morph_id
	check the crtd_trans_num sya ung may kapit ng pay_reciept na yan




How to activate the venv
	check the file path
![[Pasted image 20250918100318.png]]


For assistance PPSR-250909000085. Kindly revert from Default to "Registered"
cc Sir @⁨Unknown⁩
		Notice Table
		search mo to PPSR-250909000085, pag nakita mong default. gawin mong approved
		pag nd naka default, sabhin mo sa knila na nd naman naka default
		then click the  is_searchable to search the data


to check the grantor and criditor of the PPSR-250909000085
in notice table get the notice id
then in the notice_users  search the notice_id 
get the creditor and grantor

account individual
		kenken123
		 P@ssw0rd123


Account Deletion
	Account Number : 
	Email :
	
Change Address 
	Account Number :
	Email : 
	Old Address :
	New Address : 

Change Username:
		Account Number :
		 Email :
		 Old Username :
		 New Username :

Change Email Address 
       Account Number :
       Old Email Address :
       New Email Address :

Payment Request 
		PPSR number : 
		 Receipt Number :

change Company name
    get the get the userid 
   then go to user_groups copy the id then go to notices find in the group_id if no data change it  in the users_groups , if data exist dont change anything







Case
   PPSR number: PPSR-251114000153
	Receipt Number: 8771-11172025-612840 / 
	PAY-251114000103
	
	 Incorrect PAY 
	  Correct PAY PAY-251114000118

Case if The pay is not match in the Receipt number given in the GC
revers 
check the 
 Billings Table 
  Ref_trans_num then get the billing_payment_Id
  Billing_payment table 
   paste id = "billing_payment_id"

get the PAY number and run markaspaid becase pay of the gc is wrong





pag Na clear na ung PPSR number
 check muna sa payment kung nag eexist pag hindi 
 run the MarkAsPaid to have a payment then check if the payment have data 
 then run the PaymentOverride
 

Override if the payment table the payment exist 
Markaspaid if the payment didnt exist in the payment table



Same PAY number or No PAY number
get the id of the PPSR in notices
Billing Table 
		Paste the id in morph_id
		 then get the Billing_payment_id
		 
Billing_payments
		 id = "Billing_payment_id"
		 
get the PAY then Run mark as paid




cant find public search 

Ung is approved at is email verified dapat may check at 
Ung is approved automatic yan mag ccheck pag individual after nya mag email verified (since walang approval ung indivifual)



Bulk payment 
us markaspaid



Bulk payment 
	   clear notice
			   get the old PAY NUMBER 
			   to linked the new notice to the payment



pag walang data sa billing 
		possible nag double click ng continue 
		run as markaspaid then override 

no billing and clear notice and ni create ng bagong notice
continue payment  tas wag lang babayaran para mag karoon ng data ang billing 


may bagong create na notice number then 

nung ni mark as paid ko na sya ang error code nya is 

00|0225||PAY-260105000442||| meaning unable to locate record  

hehehe

example

 ppsr-00001 = pay-00001 ppsr-00001 deleted na ung pay-00001 bayad nba?
 
 paid na ung old pay number then 

use the override gamit ung old pay number and new notice number 



bulk payment error code 0225 unable to locate record
		record not found pa confirm kung bayad na  
		 kung bayad na saka i manual payment
		 branch(payment retry)
		 notices - file
			 @blp.route("/api/notices/payments/manual")




bulk payment no error code payment exist and di linked ung billing_payment_id sa billings
	all PPSR number , Billing_payments copy replace the billing_payment_id in billing table
	 after that
	 Markaspaid add True
	 ![[Pasted image 20260116144417.png]]

 then run

		
 