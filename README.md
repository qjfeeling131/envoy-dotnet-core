# envoy-dotnet-core


How to genereate the certificate for the HTTPS 2 in Windows

Step 1: Generate certs
dotnet dev-certs https -ep ${env:USERPROFILE}\.aspnet\https\TeaAPI.pfx -p {Password}
and input 
dotnet dev-certs https --trust
eg:
dotnet dev-certs https -ep $env:USERPROFILE\.aspnet\https\TeaAPI.pfx -p passWORD!23

Step 2: Use the certificate
A. Go to the project's folder
B. Run this command:  dotnet user-secrets set "Kestrel:Certificates:Development:Password" "passWORD!23"
