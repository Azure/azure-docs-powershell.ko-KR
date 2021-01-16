---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367074"
---
# Publish-AzWebApp

## SYNOPSIS
zipdeploy를 사용하여 ZIP, JAR 또는 WAR 파일에서 Azure 웹앱을 배포합니다. 

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
**Publish-AzWebApp** cmdlet은 기존 Azure Web App에 콘텐츠를 업로드합니다. .NET, Python 또는 Node와 같은 스택을 사용하는 경우 ZIP 파일 또는 WAR 또는 JAR 파일을 사용하는 경우 콘텐츠를 ZIP 파일로 Java. 배포하는 동안 추가 빌드 단계 없이 콘텐츠를 미리 빌드하고 즉시 실행해야 합니다. 이 cmdlet은 Kudu zipdeploy 및 wardeploy 기능을 사용하여 콘텐츠를 배포합니다. zipdeploy 및 wardeploy가 어떻게 작동하고, 배포를 위해 웹앱을 올바르게 패키지하는 방법에 대한 자세한 내용은 Kudu 위키를 참조하세요. https://aka.ms/kuduzipdeployhttps://aka.ms/kuduwardeployzipdeploy 및 wardeploy에 대한 유용한 세부 정보가 포함되어 있습니다.

## 예제

### 예제 1
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

리소스 그룹의 app.zip Web-WestUS에 속하는 MyApp이라는 웹앱에 웹앱의 콘텐츠를 업로드합니다.

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

리소스 그룹 contosoRG에 app.zip ContosoApp이라는 웹앱에 웹앱에 업로드합니다. cmdlet은 백그라운드 작업에서 실행됩니다.

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

java_app.jar의 콘텐츠를 리소스 그룹 ContosoRG에 속하는 ContosoApp이라는 웹앱에 업로드합니다.

## PARAMETERS

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
강제로 제거 옵션

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## 출력

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## 참고 사항

## 관련 링크
