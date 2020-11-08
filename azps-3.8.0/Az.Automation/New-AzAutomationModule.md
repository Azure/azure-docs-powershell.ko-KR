---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044968"
---
# New-AzAutomationModule

## SYNOPSIS
모듈을 자동화로 가져옵니다.

## 구문과

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**새 AzAutomationModule** cmdlet은 모듈을 Azure 자동화로 가져옵니다.
이 명령은 .zip 확장명을 가진 압축 파일을 받습니다.
파일에는 다음 형식 중 하나인 파일이 포함 된 폴더가 포함 되어 있습니다. 
- 파일 이름 확장명이 psm1 또는 .dll 인 Windows PowerShell 모듈 
- 파일 이름 확장명이 psd1 인 Windows PowerShell 모듈 매니페스트는 .zip 파일의 이름과 폴더 이름, 폴더에 있는 파일의 이름이 동일 해야 합니다.
.Zip 파일을 자동화 서비스에서 액세스할 수 있는 URL로 지정 합니다.
이 cmdlet 또는 Set-AzAutomationModule cmdlet을 사용 하 여 Windows PowerShell 모듈을 자동화로 가져오는 경우 작업이 비동기 작업입니다.
명령이 성공적으로 가져오기에 성공 또는 실패 하는지 여부를 완료 합니다.
성공 여부를 확인 하려면 다음 명령을 실행 합니다. `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName의 값에 대해 **ProvisioningState** 속성을 확인 합니다.

## 예제의

### 예제 1: 모듈 가져오기
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

이 명령은 ContosoModule 이라는 모듈을 Contoso17 이라는 Automation 계정으로 가져옵니다.
이 모듈은 contosostorage 이라는 저장소 계정의 Azure blob에 저장 되며, 명명 된 컨테이너인 container입니다.

## 변수

### -AutomationAccountName
이 cmdlet이 모듈을 가져오는 Automation 계정의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkUri
모듈 zip 패키지에 대 한 url입니다.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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
이 cmdlet이 가져오는 모듈의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet가 모듈을 가져올 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### 시스템 Uri

## 출력

### Microsoft Azure. 모듈별. 모듈

## 상속자

## 관련 링크

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[제거-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


