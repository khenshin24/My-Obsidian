git submodule init


hrmis
git submodule update --init

file : appsettings.json
"DefaultConnection": "server=localhost;database=ikon_dev;user=root;password=P@ssw0rd"

dotnet restore

dotnet ef database update --project IKON.Core/IKON.Core.csproj --startup-project IKON.WebApi/IKON.WebApi.csproj

dotnet ef migrations add candidatesite-column-change-to-nullable --project IKON.Core/IKON.Core.csproj --startup-project IKON.WebApi/IKON.WebApi.csproj


dotnet ef migrations add update-inspected-date-to-nullable-pmad-forms --project MMDA.Backend.Core/MMDA.Backend.Core.csproj --startup-project MMDA.Backend.WebApi/MMDA.Backend.WebApi.csproj


branch  : develop

Run IKON
	cd IKON.WebApi
	dotnet run IKON.WebApi.csproj


importing database
ikon
	-->docker exec -i mariadb mysql -uroot -pP@ssw0rd ikon_dev< /home/ken/ikon_base.sql
	-->dotnet ef database update --project IKON.Core/IKON.Core.csproj --startup-project IKON.WebApi/IKON.WebApi.csproj
mmda

dotnet ef database update --project MMDA.Backend.Core/MMDA.Backend.Core.csproj --startup-project MMDA.Backend.WebApi/MMDA.Backend.WebApi.csproj

	-->docker exec -i mariadb mysql -uroot -pP@ssw0rd mmda< /home/ken/mmda_obdg.sql


	


// add columns in existing table 
		-->dotnet ef migrations add disable_at --project IKON.Core/IKON.Core.csproj --startup-project IKON.WebApi/IKON.WebApi.csproj


  MMDA
-->
	folder: IKON.core/data/migrations
		file disable_at.cs


run the project
	open integraded temila located in IKON.WebApi



smtp password
nbuufidrajlipmoa


Not  running becase of conflict

![[Pasted image 20230424121756.png]]
then git pull



Merge!
	
	target branch - develop
	git pull origin IKON-4
	
![[Pasted image 20230424134440.png]]
	
	![[Pasted image 20230511111729.png]]
	
	
	{\"i\":3,\"n\":\"Navotas Sanitary Landfill\",\"d\":null}
	
	"d_Barangay": "{\"i\":101,\"n\":\"Barangay 101\",\"d\":\"Caloocan\"}",
	
{\"i\":101,\"n\":\"Barangay 101\",\"d\":Caloocan}



	
		








