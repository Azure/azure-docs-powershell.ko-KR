---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 076679499cf64100bcded5a29e7bc158a81423ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968928"
---
# Set-AzIntegrationAccountReceivedIcn

## SYNOPSIS
Azure 리소스 그룹의 ICN(통합 계정 교환 제어 번호)을 업데이트합니다.

## 구문

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
Set-AzIntegrationAccountGeneratedIcn cmdlet은 ICN(교환 제어 번호)을 받은 기존 통합 계정이 업데이트하고, 받은 통합 계정 교환 제어 번호를 나타내는 개체를 반환합니다.
이 cmdlet을 사용하여 교환 제어 번호의 메시지 처리 상태를 받은 통합 계정을 업데이트합니다.
통합 계정 이름, 리소스 그룹 이름, 계약 이름, 제어 번호 값 및 메시지 처리 상태를 지정하여 통합 계정이 받은 교환 제어 번호를 업데이트할 수 있습니다.
이 명령과 함께 받은 새 통합 계정 교환 제어 번호를 만들 수 없습니다.
동적 매개 변수를 사용하기 위해 명령에 입력하거나 하이픈 기호(-)를 입력하여 매개 변수 이름을 나타내고 TAB 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.
필요한 템플릿 매개 변수가 누락된 경우 cmdlet에서 값을 묻는 메시지가 표시됩니다.
명령줄에서 지정한 템플릿 매개 변수 파일 값은 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.
반환할 X12 또는 Edifact 제어 번호 여부를 지정하기 위해 "-AgreementType" 매개 변수를 제공해야 합니다.

## 예제

### 예제 1
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

이 명령은 특정 통합 계정 계약에 대한 X12 교환 제어 번호를 받은 통합 계정과 메시지 처리 상태가 실패한 값을 업데이트합니다.

### 예제 2
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

이 명령은 특정 통합 계정 계약에 대한 Edifact 교환 제어 번호를 받은 통합 계정과 메시지 처리 상태가 실패한 값을 업데이트합니다.

## 매개 변수

### -AgreementName
통합 계정 계약 이름입니다.

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

### -AgreementType
통합 계정 계약 유형(X12 또는 Edifact)입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControlNumberValue
통합 계정 제어 번호 값입니다.

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

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -IsMessageProcessingFailed
받은 메시지 처리 상태입니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
통합 계정 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
통합 계정 리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber

## 참고 사항

## 관련 링크

[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)
