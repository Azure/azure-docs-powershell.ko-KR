---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213190"
---
# Unregister-AzStackHCI

## SYNOPSIS
Unregister-AzStackHCI 온-프레미스 클러스터를 나타내는 Microsoft AzureStackHCI cloud 리소스를 삭제 하 고 Azure를 사용 하 여 온-프레미스 클러스터의 등록을 취소 합니다.
클러스터에서 사용 가능한 등록 된 정보는 매개 변수가 전달 되지 않은 경우 클러스터의 등록을 취소 하는 데 사용 됩니다.

## 구문과

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Unregister-AzStackHCI 온-프레미스 클러스터를 나타내는 Microsoft AzureStackHCI cloud 리소스를 삭제 하 고 Azure를 사용 하 여 온-프레미스 클러스터의 등록을 취소 합니다.
클러스터에서 사용 가능한 등록 된 정보는 매개 변수가 전달 되지 않은 경우 클러스터의 등록을 취소 하는 데 사용 됩니다.

## 예제의

### 예제 1
```
Invoking on one of the cluster node
```

C:\PS \> 등록 취소-AzStackHCI 결과: 성공

### 예제 2
```
Invoking from the management node
```

C:\PS \> 등록 취소-AzStackHCI-ComputerName ClusterNode1 Result: 성공

### 예제 3
```
Invoking from WAC
```

C:\PS \> 등록 취소-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -Context.resourcename DemoHCICluster3-ResourceGroupName DemoHCIRG-확인: $False 결과: 성공

### 예제 4
```
Invoking with all the parameters
```

C:\PS \> 등록 취소-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Context.resourcename HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer. ere =-GraphAccessToken acee. rerrer-AccountId user1@corp1.com -환경 이름 AzureCloud-ComputerName node1hci-자격 증명 Get-Credential 결과: 성공

## 변수

### -SubscriptionId
리소스를 만들기 위한 Azure 구독을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context.resourcename
Azure에서 만든 자원의 리소스 이름을 지정 합니다.
지정 하지 않은 경우 온-프레미스 클러스터 이름을 사용 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Azure TenantId를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Azure 리소스 그룹 이름을 지정 합니다.
지정 하지 않으면 \<LocalClusterName\> rg가 리소스 그룹 이름으로 사용 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
ARM 액세스 토큰을 지정 합니다.
GraphAccessToken 및 AccountId와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
그래프 액세스 토큰을 지정 합니다.
ArmAccessToken 및 AccountId와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
ARM 액세스 토큰을 지정 합니다.
ArmAccessToken 및 GraphAccessToken와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -환경 이름
Azure 환경을 지정 합니다.
기본값은 AzureCloud입니다.
유효한 값은 AzureCloud, AzureChinaCloud, Azureus정부, AzureGermanCloud, AzurePPE입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Azure에 등록 되는 온-프레미스 클러스터의 클러스터 노드 중 하나를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
ComputerName에 대 한 자격 증명을 지정 합니다.
기본값은 Cmdlet을 실행 하는 현재 사용자입니다.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

## 출력

### PSCustomObject. PSCustomObject의 다음 속성을 반환 합니다.
### 결과: 성공 또는 실패 또는 취소 됨.
## 상속자

## 관련 링크
