
Iservice ---> Service ----> controller

dotet run IKON.WebApi/IKON.WebApi.csproj

Process

Model 
folder : contracts
            create IUserTempService
folder : DTO
            UserTempDto
            UserTempCreateDTO -- INPUT FIELDS
            UserTempUpdateDTO -- INPUT FIELDS

IUserTempService.cs
			public interface IUserTempService : ICRUDService<UsersTempDto,UserTempCreateDTO,UserTempUpdateDTO>

create 
		   Service :  UserTempService
		
			private readonly UserManager<ApplicationUser> _userManager;
			public UserTempService(
                           UserManager<ApplicationUser> userManager
                           )
                           _userManager = userManager;
                           
		   var res2 = _mapper.Map<ApplicationUser>(resource);
            res2.Id = Guid.NewGuid();
            var res = await _userManager.CreateAsync(res2);
            return _mapper.Map<UsersTempDto>(res2);

dataContext.cs

folder : controller
		   create UserTempController
AutoMapperProfile
program.cs

Required Fields
Id
BrokerId
UserFullName
EmailConfirmed
PhoneNumberConfirmed
TwoFactorEnabled
LockoutEnabled
AccessFailedCount



TLP battery
           



join table 
positionService
![[Pasted image 20230512131908.png]]
position DTO
![[Pasted image 20230512131948.png]]

positionModel
![[Pasted image 20230512132024.png]]

automapper
![[Pasted image 20230512132050.png]]
Ui
positionDTO
![[Pasted image 20230512132124.png]]
position-list-item.html
![[Pasted image 20230512132137.png]]




Add table
1.create Model
2.define to the dataContext
![[Pasted image 20230512141142.png]]
3.![[Pasted image 20230512141222.png]]=
4. ![[Pasted image 20230512141248.png]]
double check the migrate may theres a function can add column
