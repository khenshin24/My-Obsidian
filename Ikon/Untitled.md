Accomodation in database just update the migration using the 

dotnet ef database update --project IKON.Core/IKON.Core.csproj --startup-project IKON.WebApi/IKON.WebApi.csproj


// for medical
selectedapp = ListApplications
                                        .Where(x => (x.PrincipalId == itemPrin.Id || x.DirectEmployerId == itemPrin.Id)
                                            && x.Position.Specialization.IndustryId == item.Id
                                            && x.ApplicationStatuses.Any(s => s.StatusId == 21 || s.StatusId == 26)
                                        ).ToList();