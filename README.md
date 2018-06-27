# Authentication Server with IdentityServer4

## Installation
`brew doctor`
`brew update`
`brew install postgresql`
`brew services start postgresql`

## Create PostgreSQL Database and User
`psql`
    `CREATE DATABASE Authentication_Dev;`
    `CREATE USER Auth_Agent WITH PASSWORD '~Passw0rd!';`
    `GRANT ALL PRIVILEGES ON DATABASE Authentication_Dev TO Auth_Agent;`
`\l`
`\q`

## Generate tables
`dotnet ef database update --context ApplicationDbContext`
`dotnet ef database update --context ConfigurationDbContext`
`dotnet ef database update --context PersistedGrantDbContext`

## Errors
'psql: FATAL:  database <User> does not exist'
`createdb`
`psql`

Credits to [Wes Doyle](https://github.com/wesdoyle).
## [ASP.NET Core Full-Stack Architecture](https://www.youtube.com/playlist?list=PL3_YUnRN3Uhj3FpO6XM_2f5fIFIKnK8RO)