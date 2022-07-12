FROM mcr.microsoft.com/dotnet/aspnet:6.0
LABEL author=Rajanikanth
ADD https://github.com/nopSolutions/nopCommerce/releases/download/release-4.50.3/nopCommerce_4.50.3_NoSource_linux_x64.zip
WORKDIR /nop
RUN  apt update && apt install unzip wget -y && mkdir /nop/bin && mkdir /nop/logs
RUN unzip /nopCommerce_4.50.3_NoSource_linux_x64.zip  /nop
EXPOSE 80
CMD ["/usr/bin/dotnet" ,"/nop/Nop.Web.dll"]