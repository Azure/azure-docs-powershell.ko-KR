---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213191"
---
# Register-AzStackHCI

## SYNOPSIS
Register-AzStackHCI는 온-프레미스 클러스터를 나타내는 Microsoft AzureStackHCI cloud 리소스를 만들고 Azure를 사용 하 여 온-프레미스 클러스터를 등록 합니다.

## 구문과

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## 설명은
Register-AzStackHCI는 온-프레미스 클러스터를 나타내는 Microsoft AzureStackHCI cloud 리소스를 만들고 Azure를 사용 하 여 온-프레미스 클러스터를 등록 합니다.

## 예제의

### 예제 1
```
Invoking on one of the cluster node.
```

C:\PS \> 레지스터-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" 결과: 성공 ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/

### 예제 2
```
Invoking from the management node
```

C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ComputerName ClusterNode1 결과: 성공 ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

### 예제 3
```
Invoking from WAC
```

C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -지역 westus-Context.resourcename DemoHCICluster3-ResourceGroupName DemoHCIRG Result: Pendingforadminforresourceid:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

### 예제 4
```
Invoking with all the parameters
```

C:\PS \> 레지스터-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Region westus-Context.resourcename HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer. ere =-GraphAccessToken acee. rerrer-AccountId user1@corp1.com -환경 이름 AzureCloud-ComputerName node1hci-자격 증명 Get-Credential 결과: 성공 ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

## 변수

### -SubscriptionId
리소스를 만들기 위한 Azure 구독을 지정 합니다.
이것은 유일한 필수 매개 변수입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -지역
리소스를 만들 지역을 지정 합니다.
기본값은 미국입니다.

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

### -Context.resourcename
Azure에서 만든 자원의 리소스 이름을 지정 합니다.
지정 하지 않은 경우 온-프레미스 클러스터 이름을 사용 합니다.

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

### -TenantId
Azure TenantId를 지정 합니다.

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

### -ResourceGroupName
Azure 리소스 그룹 이름을 지정 합니다.
지정 하지 않으면 \<LocalClusterName\> rg가 리소스 그룹 이름으로 사용 됩니다.

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

### -ArmAccessToken
ARM 액세스 토큰을 지정 합니다.
GraphAccessToken 및 AccountId와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.

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

### -GraphAccessToken
그래프 액세스 토큰을 지정 합니다.
ArmAccessToken 및 AccountId와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.

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

### -AccountId
ARM 액세스 토큰을 지정 합니다.
ArmAccessToken 및 GraphAccessToken와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
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
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
클러스터 이름 또는 Azure에 등록 되는 온-프레미스 클러스터의 클러스터 노드 중 하나를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
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
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

## 출력

### PSCustomObject. PSCustomObject의 다음 속성을 반환 합니다.
### 결과: 성공 또는 실패 또는 PendingForAdminConsent 또는 취소 됨.
### ResourceId: Azure에서 만든 자원의 리소스 ID입니다.
### PortalResourceURL: Azure 포털 리소스 URL입니다.
### PortalAADAppPermissionsURL: AAD 앱 사용 권한 페이지의 Azure 포털 URL입니다.
## 상속자

## 관련 링크
