---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225980"
---
# Publish-AzWebApp

## SYNOPSIS
Zipdeploy를 사용 하 여 ZIP, JAR 또는 WAR 파일에서 Azure 웹 앱을 배포 합니다. 

## 구문과

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

## 설명은
**AzWebApp** cmdlet은 콘텐츠를 기존 Azure Web App에 업로드 합니다. .NET, Python 또는 Node와 같은 스택을 사용 하거나, Java를 사용 하는 경우 WAR 또는 JAR 파일의 경우 콘텐츠는 ZIP 파일에 패키지 되어야 합니다. 배포 중에 추가 빌드 단계 없이 콘텐츠를 미리 빌드하고 실행할 준비가 되어 있어야 합니다. 이 cmdlet은 Kudu zipdeploy 및 워 하는 배포 기능을 사용 하 여 콘텐츠를 배포 합니다. Zipdeploy 및 Kudu에서 작업을 배포 하는 방법과 배포를 위해 웹 앱을 올바르게 패키지 하는 방법에 대 한 자세한 내용은 wiki를 참조 하세요. https://aka.ms/kuduzipdeployhttps://aka.ms/kuduwardeployzipdeploy 및 워 배포에 대 한 유용한 정보를 포함 합니다.

## 예제의

### 예제 1
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

리소스 그룹 Default-WestUS에 속하는 MyApp 라는 웹 앱에 app.zip의 내용을 업로드 합니다.

### 예제 2
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

리소스 그룹 ContosoRG에 속한 ContosoApp 이라는 웹 앱의 스테이징 슬롯에 javaproject의 내용을 업로드 합니다.

### 예제 3
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

app.zip의 콘텐츠를 리소스 그룹 ContosoRG에 속한 ContosoApp 이라는 웹 앱에 업로드 합니다. Cmdlet은 백그라운드 작업에서 실행 됩니다.

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

리소스 그룹 ContosoRG에 속한 ContosoApp 이라는 웹 앱에 .jar java_app의 콘텐츠를 업로드 합니다.

## 변수

### -ArchivePath
보관 파일의 경로입니다. ZIP, 전쟁, JAR를 지원 합니다.

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -이름
웹 앱의 이름입니다.

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

### -슬롯
웹 앱 슬롯의 이름입니다.

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

### -Web app
Web app 개체

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft Azure. *. m a i m Apps.

## 출력

### Microsoft Azure. *. m a i m Apps.

## 상속자

## 관련 링크
