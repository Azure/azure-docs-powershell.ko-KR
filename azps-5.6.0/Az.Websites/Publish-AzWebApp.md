---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 726f991f5e51b6196b61a6e977ba1c5d4a1debf0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014459"
---
# Publish-AzWebApp

## SYNOPSIS
zipdeploy를 사용하여 ZIP, JAR 또는 WAR 파일에서 Azure Web App을 배포합니다. 

## 구문

### FromResourceName
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromWebApp
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## 설명
**Publish-AzWebApp** cmdlet은 기존 Azure Web App에 콘텐츠를 업로드합니다. .NET, Python 또는 Node와 같은 스택을 사용하는 경우 ZIP 파일 또는 WAR 또는 JAR 파일을 사용하는 경우 콘텐츠를 ZIP 파일로 Java. 배포하는 동안 추가 빌드 단계 없이 콘텐츠를 미리 빌드하고 바로 실행할 수 있습니다. 이 cmdlet은 Kudu zipdeploy 및 wardeploy 기능을 사용하여 콘텐츠를 배포합니다. zipdeploy 및 wardeploy가 어떻게 작동하고 배포를 위해 웹앱을 올바르게 패키지하는 방법에 대한 자세한 내용은 Kudu wiki를 참조하세요. https://aka.ms/kuduzipdeploy 및 https://aka.ms/kuduwardeploy zipdeploy 및 wardeploy에 대한 유용한 세부 정보가 포함되어 있습니다.

## 예제

### 예제 1
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

리소스 그룹 default-web-WestUS에 app.zip MyApp이라는 웹앱에 콘텐츠를 업로드합니다.

### 예제 2
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

리소스 그룹 ContosoRG에 속하는 ContosoApp이라는 웹앱의 스테이징 슬롯에 javaproject.war의 콘텐츠를 업로드합니다.

### 예제 3
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

리소스 그룹 contosoRG에 app.zip ContosoApp이라는 웹앱에 콘텐츠를 업로드합니다. cmdlet은 백그라운드 작업에서 실행됩니다.

### 예제 4
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### 예제 5
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

리소스 그룹 ContosoRG에 java_app ContosoApp이라는 웹앱에 java_app.jar의 콘텐츠를 업로드합니다.

### 예제 6
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Timeout 300000 -Force
```

리소스 그룹 ContosoRG에 java_app ContosoApp이라는 웹앱에 java_app.jar의 콘텐츠를 업로드합니다. 사용자는 요청 시간이 되기 전에 대기하도록 밀리초에서 시간의 시간을 설정할 수 있습니다.

## 매개 변수

### -ArchivePath
보관 파일의 경로입니다. ZIP, WAR 및 JAR이 지원됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
백그라운드에서 cmdlet 실행

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
강제 제거 옵션

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
웹앱의 이름입니다.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
웹앱 슬롯의 이름입니다.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Timeout
요청 시간이 되기 전에 기다릴 시간(밀리초)을 설정합니다.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
웹앱 개체

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## 출력

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## 참고 사항

## 관련 링크
