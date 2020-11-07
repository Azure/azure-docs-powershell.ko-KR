---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877197"
---
# New-AzsComputeQuota

## SYNOPSIS
제공 된 할당량 매개 변수를 사용 하 여 계산 할당량을 만들거나 업데이트 합니다.

## 구문과

### CreateExpanded (기본값)
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### 만드는
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명은
제공 된 할당량 매개 변수를 사용 하 여 계산 할당량을 만들거나 업데이트 합니다.

## 예제의

### 예제 1: 기본 매개 변수를 사용 하 여 계산 할당량 만들기
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

지정 되지 않은 매개 변수는 위와 같이 기본 매개 변수로 설정 됩니다.

### 예제 2: 사용자 지정 매개 변수를 사용 하 여 계산 할당량 만들기
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

매개 변수를 사용 하 여 할당량을 사용자 지정 합니다. 지정 되지 않은 모든 매개 변수는 default 값을 갖습니다.

## 변수

### -AvailabilitySetCount
허용 되는 최대 가용성 집합 수

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### -CoresCount
허용 되는 최대 코어 수.

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -위치
리소스의 위치입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Location1
리소스의 위치입니다.

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -이름
할당량의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -새 할당량
리소스 할당을 제어 하는 데 사용 되는 계산 할당량 정보를 보유 합니다.
생성 하려면 새 할당량 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -PremiumManagedDiskAndSnapshotSize
허용 되는 premium 유형의 최대 관리 디스크 및 스냅숏 수입니다.

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### -StandardManagedDiskAndSnapshotSize
허용 되는 표준 유형의 관리 되는 디스크와 스냅샷의 수 있습니다.

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.
구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -VirtualMachineCount
허용 되는 최대 가상 머신 수입니다.

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### -VMScaleSetCount
허용 되는 최대 크기 조정 집합 수입니다.

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Api20180209 (Microsoft. PowerShell. a t t.

## 출력

### Api20180209 (Microsoft. PowerShell. a t t.



## 상속자

복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.

새 할당량 <IQuota> : 리소스 할당을 제어 하는 데 사용 되는 계산 할당량 정보를 보유 합니다.
  - `[Location <String>]`: 리소스의 위치입니다.
  - `[AvailabilitySetCount <Int32?>]`: 허용 되는 최대 가용성 집합 수입니다.
  - `[CoresLimit <Int32?>]`: 최대 코어 수를 허용 합니다.
  - `[PremiumManagedDiskAndSnapshotSize <Int32?>]`: 관리 되는 디스크의 최대 수 및 premium 유형의 스냅숏에 허용 됩니다.
  - `[StandardManagedDiskAndSnapshotSize <Int32?>]`: 관리 되는 최대 디스크 수 및 standard 유형의 스냅숏을 사용할 수 있습니다.
  - `[VMScaleSetCount <Int32?>]`: 최대 크기 조정 집합을 사용할 수 있습니다.
  - `[VirtualMachineCount <Int32?>]`: 허용 되는 최대 가상 머신 수입니다.

## 관련 링크

