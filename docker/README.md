# Docker Setup for Knowledge Palace

This folder contains the Docker setup for the Knowledge Palace project.

## Services

- **sql**: Azure SQL Edge

## Usage

1. Ensure you have Docker installed on your machine.
2. Navigate to this directory in your terminal.
3. Run the following command to start the services:

    ```sh
    docker-compose up -d
    ```

4. To stop the services, run:

    ```sh
    docker-compose down
    ```

## Configuration

- The SQL service is configured to use the `mcr.microsoft.com/azure-sql-edge` image.
- The default SA password is set to `MyStrongPass123`. You can change this in the `docker-compose.yaml` file.

## Ports

- SQL service is exposed on port `1433`.

## Environment Variables

- `ACCEPT_EULA`: Must be set to "1" to accept the SQL Server EULA.
- `MSSQL_SA_PASSWORD`: The password for the SA user.
- `MSSQL_PID`: The edition of SQL Server to use.
- `MSSQL_USER`: The SQL Server user.

