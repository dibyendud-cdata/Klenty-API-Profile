# SQL Queries:

These document consists of all the queries needed to retrieve necessary data from the existing tables in **Klenty**

1. **Get Company Cadences** >>> Select * from CompanyCadences

2. **Get User Cadences >>> Select * from UserCadences where owner = 'bobb@cdata.com'

3. **Get Lists** >>> Select * from Lists

4. **Get Prospect Details with Custom Fields** >>> Select * from ProspectDetailswithCustomFields where Email = 'davidl@cdata.com'

5. **Get Prospects by Lists (input)** >>> Select * from ProspectByList where List = 'OCC Prospecting'

6. **Get Prospects by Lists (dynamic)** >>> Select * from ProspectByList where List IN (Select name from Lists)

7. **Get Prospect Details by Email** >>> Select * from ProspectDetailsByEmail where Email = 'davidl@cdata.com'

8. **Get Prospect Status by Email** >>> select * from ProspectStatusByEmail where Email = 'davidl@cdata.com'

9. **Get Prospect Status by ID** >>> select * from ProspectStatusByID where id = 'davidl@cdata.com'

10. **Get Prospects by Prospect Creation Date** >>> Select * from ProspectByCreationDate where startDate='2020/01/01' AND endDate = '2023/03/20'

11. **Get Prospects by the Last Updated Date** >>> Select * from ProspectByLastUpdatedDate where startdate ='2020/01/01' AND enddate = '2023/03/20'