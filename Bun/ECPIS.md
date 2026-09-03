clr_request_cases populated data

deromast table copy then move to clr_request_cases


 - create applicant
	{{domain}}/api/tests/applicants/create/hit
- get the profile details
	profile
	       "fname": "Jmizi",
  	       "lname": "Flores",
 	       "mname": "Perez",
- Dero-create

- update profile of the applicant
	Applicant Collection
		Upload,Update,Attach

- Create Clearance
	First time job seeker

- run API 
	Get Clearance to get the TRN

- check db.clr_request.trn = 'TRN-NUMBER'
	get the clr_request_id

- check db.clr_request_cases.crl_request_id = clr_request_id
	
		process clr request cases populated












