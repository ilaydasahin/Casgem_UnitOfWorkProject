# Unit of Work Pattern Implementation

An ASP.NET Core application showcasing the Repository and Unit of Work design patterns for transactional database operations.

## Overview

This project ensures data consistency during complex database transactions (e.g., banking transfers). The Unit of Work pattern coordinates multiple repository operations, committing them as a single atomic transaction.

## Architecture

- N-Tier Structure: Presentation, Business, Data Access, and Entity layers.
- Unit of Work: Manages `DbContext` state and handles transaction Commit/Rollback.
- Generic Repository: Reusable CRUD operations for all entities.

## Technology Stack

- ASP.NET Core 6.0
- Entity Framework Core
- Dependency Injection

## Execution

1. Restore dependencies:
   `dotnet restore`
2. Apply Database Migrations:
   `dotnet ef database update --project CasgemUow.DataAccessLayer`
3. Run the application:
   `dotnet run --project CasgemUow.PresentationLayer`
