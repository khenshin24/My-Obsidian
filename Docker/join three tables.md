
```c#
public async Task<IEnumerable<CrewViolationDTO>> ListByLandfillAsync(int id)
{
	 var res = await (from cv in _dataContext.CrewViolations
	 join g in _dataContext.GarbageTrucks on cv.GarbageTruckId equals g.Id
	 join gi in _dataContext.GarbageTruckInspections on g.GarbageTruckInspectionId equals gi.Id
	 where cv.LandFillId == id
	 select new CrewViolationDTO
	 {
	 Id = cv.Id,
	 LguId = cv.LguId,
	 GarbageTruckType = gi.C_TruckType
	 })
	 .AsNoTracking()
	 .ToListAsync();
var r = _mapper.Map<IEnumerable<CrewViolationDTO>>(res);

return r;

}

AutoMapperProfile
CreateMap<GarbageTruckInspection, CrewViolationDTO>()
.ForMember(dest => dest.GarbageTruckType, opt => opt.MapFrom(src => src.C_TruckType));

//short join three tables 
	//includes the tables you need to join
	  //lastly use ThenInclude to last entiry

public async Task<IEnumerable<CrewViolationDTO>> ListByLandfillAsync(int id)
{
	var res = await _dataContext.CrewViolations
	.Where(x => x.LandFillId == id)
	.Include(x => x.GarbageTruck)
	.ThenInclude(x => x.GarbageTruckInspection)
	.AsNoTracking()
	.ToListAsync();
	var r = _mapper.Map<IEnumerable<CrewViolationDTO>>(res);
	return r;
}

AutoMapperProfile
CreateMap<CrewViolation, CrewViolationDTO>()
.ForMember(dest => dest.D_LandFill, opt => opt.MapFrom(src => src.D_LandFill))
.ForMember(dest => dest.D_Contractor, opt => opt.MapFrom(src => src.D_Contractor))
.ForMember(dest => dest.D_GarbageTruck, opt => opt.MapFrom(src => src.D_GarbageTruck))
.ForMember(dest => dest.D_LGU, opt => opt.MapFrom(src => src.D_LGU))

//here you can access the prop of 3rd table which is  GarbageTruckInspection

.ForMember(dest => dest.GarbageTruckType, opt => opt.MapFrom(src => src.GarbageTruck.GarbageTruckInspection.C_TruckType));

//Note: add all the properties that you want to have 
	//in my case i created in  CrewViolationDTO  a GarbageTruckType prop
	//so i can put  the data of  C_TruckType prop in the CrewViolationDTO
c => src.D_LandFill))
            .ForMember(dest => dest.D_Contractor, opt => opt.MapFrom(src => src.D_Contractor))
            .ForMember(dest => dest.D_GarbageTruck, opt => opt.MapFrom(src => src.D_GarbageTruck))
            .ForMember(dest => dest.D_LGU, opt => opt.MapFrom(src => src.D_LGU))
```




















