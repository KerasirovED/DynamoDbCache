# Idea
The idea of the project to create an ASP.NET Core REST application for managing cache stored in DynamoDB.

# Why?
I already have two projects: TurkeySteamBot, and MusicAggreagatorBot. These two projects needed in some temporary storage, which will keep stuff like tokens, or predownloaded data from some API. I used to store such data directly in memory, but it is impossible to do so in AWS because of lambda: the instance is completely deleted in 15 mins of inactivity. I could create a separate table in each repository, and read out of those table, and store some temporary data there, but then I came up with an idea to create a separate servise for such thing. I thought it is amazing reason to learn ASP.NET, which I wanted to try over a year, and create a pet project.

# What in the scope?
## Authentication, and autharization
In order to distingish different applications, I am thinking about implementation some sort of authentication. The app will return some token to access to other endpoints.

## Cache CRUD
Once user authenticated: 
- the user must be able to create a cache entry with some invalidation date, I would even say invalidation period, which will be passed along with a value. If the date is not provided, the cash will be infinite. 
- the usermust be able to read the cached value
- once the cache invalidated, an error must be returned
- the user must be able to delete a cached value
- the user must be able to update a cached value
- the invalidation date must be reset in case of update
- the user must be able to read expired value
- the user must be able to refresh invalidation date
- the user must be able to change invalidation period

## Autotesting
Using GitHub

## Deploying
Using GitHub

## Hosting
In AWS

# Progress
- [ ] Authentication, and autharization
- [ ] Cache CRUD
- [ ] Autotesting
- [ ] Deploying
- [ ] Hosting