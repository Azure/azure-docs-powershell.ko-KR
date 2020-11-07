---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: c1bf608c76c547360d9d7a48f4ba74c1713ee049
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689850"
---
# Get-AzVMGuestPolicyStatus

## SYNOPSIS
VM에 할당 된 "게스트 구성" 유형의 이니셔티브에 대 한 게스트 구성 정책 상태 (상세)를 가져옵니다.
이니셔티브는 정의 유형 "이니셔티브"의 정책입니다.

## 구문과

### VmScope (기본값)
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

## 설명은
Get-AzVMGuestPolicyStatus cmdlet는 VM에 할당 된 "게스트 구성" 유형의 이니셔티브에 대 한 게스트 구성 정책 상태를 가져옵니다.
이니셔티브는 정의 유형 "이니셔티브"의 정책입니다.
이 cmdlet은 VM의 준수 상태와 이니셔티브의 개별 정책에 대해 비규격 이유가 아닌 이유를 가져옵니다.

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

VM에 대 한 최신 게스트 구성 정책 상태를 모두 가져옵니다.
상태에는 "게스트 구성" 형식의 모든 이니셔티브의 각 정책에 대 한 VM의 준수 상태, 준수 이유, 준수 검사 시간, 준수 여부를 확인 한 리소스 정보 등이 포함 됩니다.
결과에는 최신 상태가 포함 되며 이전 기록 상태가 포함 되지 않습니다.

### 예제 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

이니셔티브 Id를 기준으로 최신 게스트 구성 정책 상태를 가져옵니다. 상태에는 이니셔티브의 각 정책에 대 한 VM의 준수 상태, 준수 이유, 준수 검사 시간, 준수 여부를 확인 한 리소스 정보 등이 포함 됩니다.
결과에는 생성 된 이전 상태가 포함 되지 않으며, 여기에는 이니셔티브의 각 정책에 대 한 최신 상태만 포함 됩니다.

### 예제 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

이니셔티브 이름으로 최신 게스트 구성 정책 상태를 가져옵니다.
상태에는 이니셔티브의 각 정책에 대 한 VM의 준수 상태, 준수 이유, 준수 검사 시간, 준수 여부를 확인 한 리소스 정보 등이 포함 됩니다.
결과에는 생성 된 이전 상태가 포함 되지 않으며, 여기에는 이니셔티브의 각 정책에 대 한 최신 상태만 포함 됩니다.

### 예제 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

ReportId를 기준으로 게스트 구성 정책 상태를 가져옵니다.
ReportId는 initiativeId 또는 이니셔티브 이름으로 Get-AzVMGuestPolicyStatus 결과에서 찾을 수 있는 ReportId 속성으로, 다른 예를 참조 하세요.

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

Required: True
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

### -ReportId
게스트 구성 정책 상태의 Id입니다.
정의 형식이 이니셔티브이 고 category는 상태를 가져오려면 범위에 게스트 구성을 할당 해야 하는 정책입니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
## 출력

### GuestConfiguration. PolicyStatusDetailed.
## 상속자

## 관련 링크
