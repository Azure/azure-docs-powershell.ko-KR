---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373059"
---
# Set-AzAutomationModule

## SYNOPSIS
Automation에서 모듈을 업데이트합니다.

## 구문

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Set-AzAutomationModule** cmdlet은 Azure Automation에서 모듈을 업데이트합니다.
이 명령은 .zip 파일 이름 확장명을 사용하는 압축 파일을 허용합니다.
파일에는 다음 형식 중 하나인 파일이 포함된 폴더가 포함되어 있습니다. 
- wps_2 .psm1 또는 .dll 파일 이름 확장명이 있는 모듈 
- wps_2 .psd1 파일 이름 확장명을 품은 모듈 매니페스트는 .zip 파일의 이름, 폴더의 이름 및 폴더의 파일 이름이 같아야 합니다.
.zip 파일을 Automation 서비스에서 액세스할 수 있는 URL로 지정합니다.
이 cmdlet 또는 wps_2 cmdlet을 사용하여 Automation에 New-AzAutomationModule 모듈을 가져오는 경우 작업은 비동기적입니다.
이 명령은 가져오기 성공 또는 실패 여부를 완료합니다.
성공 여부를 확인하기 위해 다음 명령을 실행합니다. `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName은 **ProvisioningState** 속성을 확인하여 Succeeded 값입니다.

## 예제

### 예제 1: 모듈 업데이트
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

이 명령은 ContosoModule이라는 기존 모듈의 업데이트된 버전을 Contoso17이라는 Automation 계정으로 가져올 수 있습니다.  모듈은 contosostorage라는 스토리지 계정 및 모듈이라는 컨테이너의 Azure Blob에 저장됩니다.

## PARAMETERS

### -AutomationAccountName
이 cmdlet이 모듈을 업데이트하는 Automation 계정의 이름을 지정합니다.

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
이 cmdlet에서 가져오는 모듈의 새 버전을 포함하는 .zip 파일의 URL을 지정합니다.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
이 cmdlet이 Automation을 업데이트하는 모듈의 버전을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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
이 cmdlet에서 가져오는 모듈의 이름을 지정합니다.

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
이 cmdlet이 모듈을 업데이트하는 리소스 그룹의 이름을 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

### System.Uri

## 출력

### Microsoft.Azure.Commands.Automation.Model.Module

## 참고 사항

## 관련 링크

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[New-AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

