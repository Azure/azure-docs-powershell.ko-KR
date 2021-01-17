---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337370"
---
# New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject

## SYNOPSIS
디바이스 보안 그룹에 대한 새 임계값 사용자 지정 경고 규칙 만들기(IoT 보안)

## 구문

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
이 New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet은 IoT 보안 솔루션의 디바이스 보안 그룹에 대한 임계값 사용자 지정 경고 규칙의 새 목록을 만듭니다.

## 예제

### 예제 1
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

최소 및 최대 임계값에 대해 상태가 설정된 ant 값을 사용하여 "SomeRuleType" 형식의 새 임계값 사용자 지정 경고 규칙 만들기

## PARAMETERS

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

### -Enabled
규칙이 사용하도록 설정되어 있습니다.

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

### -MaxThreshold
최대 임계값입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinThreshold
최소 임계값입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
규칙 유형입니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule

## 참고 사항

## 관련 링크
