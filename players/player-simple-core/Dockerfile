FROM microsoft/dotnet:sdk

# Create app directory
WORKDIR /usr/src/app

COPY *.csproj ./
RUN dotnet restore

# copy everything else and build
COPY . ./
RUN dotnet build

ENV ASPNETCORE_URLS http://+:5000
EXPOSE 5000
ENV ASPNETCORE_URLS=http://*:5000
CMD [ "dotnet", "run" ]