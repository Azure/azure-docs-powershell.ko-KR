---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
ms.openlocfilehash: 2433ffa7c1a016af4d3268162587d6b901b30ae9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987163"
---
# New-AzVMWareCluster

## SYNOPSIS
사설 클라우드에서 클러스터 만들기 또는 업데이트

## 구문

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## 설명
사설 클라우드에서 클러스터 만들기 또는 업데이트

## 예제

### 예제 1: 클러스터 만들기
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

클러스터 만들기

## 매개 변수

### -AsJob
작업으로 명령을 실행합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterSize
클러스터 크기

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

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
사설 클라우드의 클러스터 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
명령 비동기 실행

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateCloudName
사설 클라우드의 이름입니다.

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

### -ResourceGroupName
리소스 그룹의 이름입니다.
이름은 대소문자와 무관합니다.

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

### -SkuName
SKU의 이름입니다.

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

### -SubscriptionId
대상 구독의 ID입니다.

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

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster

## 참고 사항

별칭

## 관련 링크

