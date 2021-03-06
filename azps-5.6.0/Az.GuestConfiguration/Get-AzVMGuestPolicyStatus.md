---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 3edb92ae8c46ab67e0e22ee808e38dad7101bfdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990206"
---
# Get-AzVMGuestPolicyStatus

## SYNOPSIS
VM에 할당된 "게스트 구성"의 이니셔티브에 대한 게스트 구성 정책 상태(세부 정보)를 얻습니다.
이니셔티브는 정의 형식 "이니셔티브"의 정책입니다.

## 구문

### VmScope(기본값)
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeNameScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ReportIdScope
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
Get-AzVMGuestPolicyStatus cmdlet은 VM에 할당된 "게스트 구성"의 이니셔티브에 대한 게스트 구성 정책 상태를 얻습니다.
이니셔티브는 정의 형식 "이니셔티브"의 정책입니다.
이 cmdlet은 VM의 규정 준수 상태와 이니셔티브의 개별 정책에 대해 규정을 준수하지 않는 이유를 제공합니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

VM에 대한 모든 최신 게스트 구성 정책 상태를 얻습니다.
상태는 "게스트 구성"형식의 모든 이니셔티브의 각 정책에 대한 VM의 준수 상태, 규정 준수 이유, 규정 준수 검사 시간, 규정 준수 확인을 위해 확인된 리소스 정보를 포함합니다.
결과에 최신 상태가 포함되고 이전 기록 상태가 포함되어 있지 않습니다.

### 예제 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

이니셔티브 ID를 통해 최신 게스트 구성 정책 상태를 얻습니다. 상태는 이니셔티브의 각 정책에 대한 VM의 준수 상태, 규정 준수 이유, 규정 준수 검사 시간, 규정 준수 확인을 위해 확인된 리소스 정보를 포함합니다.
결과에 생성된 이전 상태가 포함되어 있지 않습니다. 이니셔티브의 각 정책에 대한 최신 상태만 포함됩니다.

### 예제 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

이니셔티브 이름으로 최신 게스트 구성 정책 상태를 얻습니다.
상태는 이니셔티브의 각 정책에 대한 VM의 준수 상태, 규정 준수 이유, 규정 준수 검사 시간, 규정 준수 확인을 위해 확인된 리소스 정보를 포함합니다.
결과에 생성된 이전 상태가 포함되어 있지 않습니다. 이니셔티브의 각 정책에 대한 최신 상태만 포함됩니다.

### 예제 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

ReportId를 통해 게스트 구성 정책 상태를 얻습니다.
ReportId는 initiativeId 또는 Initiative 이름으로 Get-AzVMGuestPolicyStatus 결과에서 찾을 수 있는 ReportId 속성입니다(다른 예제 참조).

## 매개 변수

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

### -InitiativeId
정의 형식이 이니셔티브 및 범주인 정책의 정의 ID는 게스트 구성입니다.

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiativeName
정의 형식이 이니셔티브 및 범주인 정책의 이름은 게스트 구성입니다.

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportId
게스트 구성 정책 상태의 ID입니다.
정의 형식이 이니셔티브이고 범주가 게스트 구성인 정책은 상태를 얻기 위해 범위에 할당되어야 합니다.

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
VM 이름입니다.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### 없음
## 출력

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed
## 참고 사항

## 관련 링크
