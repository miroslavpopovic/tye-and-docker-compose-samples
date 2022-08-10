FROM mcr.microsoft.com/mssql/server:2022-latest

ENV ACCEPT_EULA y
ENV SA_PASSWORD Password123
ENV MSSQL_PID Developer

COPY ./init.sql .
COPY ./entrypoint.sh .

EXPOSE 1433

ENTRYPOINT ["/bin/bash", "./entrypoint.sh"]
CMD ["/opt/mssql/bin/sqlservr"]
