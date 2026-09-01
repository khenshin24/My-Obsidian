
DirectEmployer and Principal in one table 

in Principal table 

DirectEmployer DataType 2 
Principal DataType 1

how to get the principal

```
	 var principals = await _context.Applications.AsNoTracking()
	
	                             .Include(x => x.Country)
	
	                             .Include(x => x.DirectEmployer)
	
	                             .Where(x=> x.LatestStatusId == 37)
	
	                             .Select(x=> new
	
	                             {
	
	                                 CountryId = x.Country.Id,
	
	                                 CountryName = x.Country.Name,
	
	                                 PrincipalId = x.DirectEmployerId,
	
	                                 DirectEmployerName = x.DirectEmployer.Name,
	
	                                 PrincipalName = x.PrincipalId != null ? _context.Principals.Where(p => p.Id == x.PrincipalId).Select(p => p.Name).FirstOrDefault() : null
	
	                                 }).Distinct().OrderBy(x=>x.CountryName).ThenBy(x=>x.PrincipalName).ToListAsync();
```


IKON - i fixed the orderby the header of Summary of on-process candidates
and the color of sub total and total in IKON-620-temp then i pull the branch in IKON-620




change the query of Industries
change the query of Preselected
add code in selectedapp 