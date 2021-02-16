---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 5a5450629024dbca8433bee79bfe9d2fa7119025
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398039"
---
# Get-AzKustoCluster

## SYNOPSIS
리소스 그룹의 모든 Kusto 클러스터를 나열하거나 특정 Kusto 클러스터를 얻습니다.

## 구문

### ByClusterOrResourceGroupOrSubscription(기본값)
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByResourceId
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
리소스 그룹의 모든 Kusto 클러스터를 나열하거나 특정 Kusto 클러스터를 얻습니다.

## 예제

### 예제 1 - 리소스 그룹의 모든 Kusto 클러스터 나열

형식 : Microsoft.Kusto/Clusters ID : /subscriptions/xxxxxxxxx-xxxx-xxxx-xxxx-xxx/resourceGroups/testrg/providers/Microsoft..Kusto/Clusters/mykustocluster1 ResourceGroup : testrg Name : mykustocluster1 Location : Central US Capacity : 3 Sku : D13_v2 ProvisioningState : Succeeded State : Running Tag : {} Uri : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri : `https://ingest-mykustocluster1.centralus.kusto.windows.net`

형식 : Microsoft.Kusto/Clusters ID : /subscriptions/xxxxxxxxx-xxxx-xxxx-xxxx-xxx/resourceGroups/testrg/providers/Microsoft..Kusto/Clusters/mykustocluster2 ResourceGroup : testrg Name : mykustocluster2 Location : Central US Capacity : 5 Sku : D13_v2 ProvisioningState : Succeeded State : Running Tag : {} Uri : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri : `https://ingest-mykustocluster2.centralus.kusto.windows.net`


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

위의 명령은 리소스 그룹 "testrg"의 모든 Kusto 클러스터를 나열합니다.

### 예제 2 - 이름으로 특정 Kusto 클러스터를 얻습니다.

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

위의 명령은 리소스 그룹 "testrg"에서 "mykustocluster"라는 Kusto 클러스터를 반환합니다.

### 예제 3 - 리소스 ID로 특정 Kusto 클러스터를 얻습니다.

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

위의 명령은 리소스 그룹 "testrg"에서 "mykustocluster"라는 Kusto 클러스터를 반환합니다.

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

### -Name
특정 클러스터의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
사용자가 클러스터를 검색하려는 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Kusto 클러스터 ResourceID.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster

## 참고 사항

## 관련 링크
