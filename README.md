# UKParliamentEndPointsAIChat

An ASP.NET Core MVC application that provides an AI chat interface for exploring UK Parliament endpoint data.

The app uses .NET 8 and the OpenAI .NET package, with supporting code for parsing model responses and describing callable functions.

## Project structure

- `Controllers/` - MVC controllers.
- `Models/` - application configuration and view models.
- `OpenAi.Api/` - OpenAI integration, response parsing, and function metadata.
- `Views/` - Razor views.
- `wwwroot/` - static web assets.
- `UKParliamentEndPointsAIChat.Ui.csproj` - project file.

## Configuration

The app binds configuration from the `Config` section and also reads these environment variables:

- `CoachAndFocusLLMEndpoint`
- `CoachAndFocusLLMEndpoint2`

Set local values through user secrets, environment variables, or `appsettings.Development.json`. Do not commit production secrets.

## Restore

```bash
dotnet restore UKParliamentEndPointsAIChat.Ui.csproj
```

## Run

```bash
dotnet run --project UKParliamentEndPointsAIChat.Ui.csproj
```

## Build

```bash
dotnet build UKParliamentEndPointsAIChat.Ui.csproj
```

## Related repositories

- [UKParliamentEndpoints](https://github.com/ChrisBrooksbank/UKParliamentEndpoints) - endpoint API and storage.
- [UKParliamentEndPointsAdmin](https://github.com/ChrisBrooksbank/UKParliamentEndPointsAdmin) - admin UI.
- [UKParlyEndPointsFuncApp](https://github.com/ChrisBrooksbank/UKParlyEndPointsFuncApp) - scheduled endpoint checks.
