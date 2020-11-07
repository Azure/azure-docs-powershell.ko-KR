---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876022"
---
# Set-AzsNetworkQuota

## SYNOPSIS
할당량을 만들거나 업데이트 합니다.

## 구문과

### UpdateExpanded 됨 (기본값)
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Update
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명은
할당량을 만들거나 업데이트 합니다.

## 예제의

### --------------------------예제 1--------------------------
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

이름으로 네트워크 할당량을 업데이트 합니다.

### --------------------------예제 2--------------------------
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

이름으로 네트워크 할당량을 업데이트 합니다.

## 변수

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
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxLoadBalancersPerSubscription
테 넌 트 구독이 프로 비전 할 수 있는 최대 부하 분산 장치 수입니다.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxNicsPerSubscription
테 넌 트 구독이 프로 비전 할 수 있는 최대 Nic 수입니다.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxPublicIpsPerSubscription
테 넌 트 구독이 프로 비전 할 수 있는 최대 공용 IP 주소 수입니다.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Maxsecurity그룹 Persubscription
테 넌 트 구독이 프로 비전 할 수 있는 최대 보안 그룹 수입니다.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVirtualNetworkGatewayConnectionsPerSubscription
테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이 연결의 최대 수입니다.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVirtualNetworkGatewaysPerSubscription
테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이의 최대 수입니다.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVnetsPerSubscription
테 넌 트 구독이 프로 비전 할 수 있는 최대 가상 네트워크 수입니다.

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -이름
리소스의 이름입니다.

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

### -할당량
네트워크 할당량 리소스.
생성 하려면 할당량 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### 태그
키 값 쌍의 목록입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
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

### Api20150615 (Microsoft. PowerShell. i N.exe 할당량

## 출력

### Api20150615 (Microsoft. PowerShell. i N.exe 할당량



## 상속자

복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.

할당량 <IQuota> : 네트워크 할당량 리소스.
  - `[Tag <IResourceTags>]`: 키 값 쌍의 목록입니다.
    - `[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.
  - `[MaxLoadBalancersPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 최대 부하 분산 장치 수입니다.
  - `[MaxNicsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 최대 Nic 수입니다.
  - `[MaxPublicIpsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 공용 IP 주소의 최대 수입니다.
  - `[MaxSecurityGroupsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 최대 보안 그룹 수입니다.
  - `[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이 연결의 최대 수입니다.
  - `[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이의 최대 수입니다.
  - `[MaxVnetsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크의 최대 수입니다.

## 관련 링크

