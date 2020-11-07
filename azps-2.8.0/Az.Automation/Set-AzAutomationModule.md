---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: d9c036c7047ee0d568f5e1451bce46dfe2903e29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697737"
---
# Set-AzAutomationModule

## SYNOPSIS
자동화에서 모듈을 업데이트 합니다.

## 구문과

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**Set-AzAutomationModule** Cmdlet은 Azure Automation의 모듈을 업데이트 합니다.
이 명령은 .zip 확장명을 가진 압축 파일을 받습니다.
파일에는 다음 형식 중 하나인 파일이 포함 된 폴더가 포함 되어 있습니다. 
- 파일 이름 확장명이 psm1 또는 .dll 인 wps_2 모듈 
- 확장명이 psd1 인 모듈 매니페스트는 .zip 파일 이름, 폴더 이름, 폴더에 있는 파일의 이름 등이 동일 해야 합니다 wps_2.
.Zip 파일을 자동화 서비스에서 액세스할 수 있는 URL로 지정 합니다.
이 cmdlet 또는 New-AzAutomationModule cmdlet을 사용 하 여 wps_2 모듈을 자동화로 가져오는 경우 작업이 비동기 작업입니다.
명령이 성공적으로 가져오기에 성공 또는 실패 하는지 여부를 완료 합니다.
성공 여부를 확인 하려면 다음 명령을 실행 합니다. `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName의 값에 대해 **ProvisioningState** 속성을 확인 합니다.

## 예제의

### 예제 1: 모듈 업데이트
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

이 명령은 ContosoModule 이라는 기존 모듈의 업데이트 된 버전을 Contoso17 라는 Automation 계정으로 가져옵니다.  이 모듈은 contosostorage 이라는 저장소 계정의 Azure blob에 저장 되며, 명명 된 컨테이너인 container입니다.

## 변수

### -AutomationAccountName
이 cmdlet이 모듈을 업데이트 하는 Automation 계정의 이름을 지정 합니다.

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
이 cmdlet이 가져오는 새 모듈 버전을 포함 하는 .zip 파일의 URL을 지정 합니다.

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
이 cmdlet이 자동화를 업데이트 하는 모듈의 버전을 지정 합니다.

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
이 cmdlet이 모듈을 업데이트 하는 리소스 그룹의 이름을 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### 시스템 Uri

## 출력

### Microsoft Azure. 모듈별. 모듈

## 상속자

## 관련 링크

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[새로운 AzAutomationModule](./New-AzAutomationModule.md)

[제거-AzAutomationModule](./Remove-AzAutomationModule.md)


