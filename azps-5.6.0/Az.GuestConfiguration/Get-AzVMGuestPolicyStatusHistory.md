---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 9161b3c9c55c1014b64419a3644bf7ec80af8648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990201"
---
# Get-AzVMGuestPolicyStatusHistory

## SYNOPSIS
VM에 할당된 "게스트 구성"의 이니셔티브에 대한 게스트 구성 정책 준수 상태 기록을 얻습니다.
이니셔티브는 정의 형식 "이니셔티브"의 정책입니다.

## 구문

### InitiativeNameScope(기본값)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
Get-AzVMGuestPolicyStatusHistory cmdlet은 VM에 할당된 "게스트 구성"의 이니셔티브에 대한 게스트 구성 정책의 준수 상태 기록을 얻습니다.
이니셔티브는 정의 형식 "이니셔티브"의 정책입니다.
Get-AzVMGuestPolicyStatus cmdlet을 사용하여 Get-AzVMGuestPolicyStatusHistory cmdlet의 출력에서 찾을 수 있는 ReportId를 사용하여 단일 규정 준수 상태에 대한 세부 정보를 얻을 수 있습니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

이니셔티브 ID에 따라 규정 준수 상태 기록을 얻습니다. ShowOnlyChange 스위치는 기록 상태 변경만 보여줍니다.
두 준수 검사 간에 변경되지 않은 상태를 건너뜁합니다.

### 예제 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

이니셔티브 이름으로 규정 준수 상태 기록을 얻습니다.
ShowOnlyChange 스위치는 기록 상태 변경만 보여줍니다.
두 준수 검사 간에 변경되지 않은 상태를 건너뜁합니다.

### 예제 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

VM에 할당된 모든 게스트 구성 정책에 대한 규정 준수 상태 기록을 얻습니다.
ShowOnlyChange 스위치는 기록 상태 변경만 보여줍니다.
두 준수 검사 간에 변경되지 않은 상태를 건너뜁합니다.

### 예제 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

이니셔티브 ID를 통해 규정 준수 상태 기록을 얻습니다.

### 예제 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

이니셔티브 이름으로 규정 준수 상태 기록을 얻습니다.

### 예제 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
VM에 할당된 모든 게스트 구성 정책에 대한 규정 준수 상태 기록을 얻습니다.

### 예제 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

ReportId를 통해 게스트 구성 정책 상태를 얻습니다.
ReportId는 Get-AzVMGuestPolicyStatusHistory의 결과에서 찾을 수 있는 ReportId 속성입니다. (다른 예제를 참조해 주세요)

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

Required: False
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

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowOnlyChange
게스트 구성 정책에 대한 기록 상태 변경 내용을 보여줍니다.
두 규정 준수 상태 감사 실행 간에 변경되지 않은 상태를 건너뜁합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
VM 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
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

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus
## 참고 사항

## 관련 링크
