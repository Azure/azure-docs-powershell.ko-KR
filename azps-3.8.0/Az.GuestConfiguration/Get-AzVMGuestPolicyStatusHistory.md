---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034614"
---
# Get-AzVMGuestPolicyStatusHistory

## SYNOPSIS
VM에 할당 된 "게스트 구성" 유형의 이니셔티브에 대 한 게스트 구성 정책 준수 상태 기록을 가져옵니다.
이니셔티브는 정의 유형 "이니셔티브"의 정책입니다.

## 구문과

### InitiativeNameScope (기본값)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
Get-AzVMGuestPolicyStatusHistory cmdlet은 VM에 할당 된 "게스트 구성" 유형의 이니셔티브에 대 한 게스트 구성 정책의 준수 상태 기록을 가져옵니다.
이니셔티브는 정의 유형 "이니셔티브"의 정책입니다.
Get-AzVMGuestPolicyStatus cmdlet을 사용 하 여 Get-AzVMGuestPolicyStatusHistory cmdlet의 출력에서 찾을 수 있는 ReportId를 사용 하 여 단일 준수 상태의 세부 정보를 가져옵니다.

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

ShowOnlyChange 스위치는 기준 상태 변경만 표시 합니다.
두 준수 검사 간에 변경 되지 않은 상태를 건너뜁니다.

### 예제 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

이니셔티브 이름에 따라 준수 상태 기록을 가져옵니다.
ShowOnlyChange 스위치는 기록 상태 변경 내용만 표시 합니다.
두 준수 검사 간에 변경 되지 않은 상태를 건너뜁니다.

### 예제 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

VM에 할당 된 모든 게스트 구성 정책에 대 한 준수 상태 기록을 가져옵니다.
ShowOnlyChange 스위치는 기록 상태 변경 내용만 표시 합니다.
두 준수 검사 간에 변경 되지 않은 상태를 건너뜁니다.

### 예제 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

이니셔티브 Id에 따라 준수 상태 기록을 가져옵니다.

### 예제 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

이니셔티브 이름에 따라 준수 상태 기록을 가져옵니다.

### 예제 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
VM에 할당 된 모든 게스트 구성 정책에 대 한 준수 상태 기록을 가져옵니다.

### 예제 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

ReportId를 기준으로 게스트 구성 정책 상태를 가져옵니다.
ReportId는 Get-AzVMGuestPolicyStatusHistory의 결과에서 찾을 수 있는 ReportId 속성입니다. (다른 예제를 참조 하세요.)

## 변수

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

### -InitiativeId
정의 형식이 이니셔티브이 고 범주가 게스트 구성 인 정책의 정의 Id

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
정의 형식이 이니셔티브이 고 범주가 게스트 구성 인 정책의 이름

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
게스트 구성 정책에 대해서만 기록 상태 변경을 표시 합니다.
두 준수 상태 감사 실행 간에 변경 되지 않은 상태를 건너뜁니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
## 출력

### GuestConfiguration의 PolicyStatus (Microsoft.
## 상속자

## 관련 링크
