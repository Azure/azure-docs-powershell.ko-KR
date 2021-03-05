---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: da4cd54b9865cdf30487a7e49e5581474ebb2a35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012528"
---
# <span data-ttu-id="7c757-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="7c757-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="7c757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c757-102">SYNOPSIS</span></span>
<span data-ttu-id="7c757-103">이름, ID, 속성 및 추가 클러스터 세부 정보를 포함하여 지정된 연결된 클러스터의 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="7c757-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c757-104">SYNTAX</span></span>

### <span data-ttu-id="7c757-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="7c757-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7c757-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="7c757-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7c757-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7c757-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c757-108">목록</span><span class="sxs-lookup"><span data-stu-id="7c757-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7c757-109">설명</span><span class="sxs-lookup"><span data-stu-id="7c757-109">DESCRIPTION</span></span>
<span data-ttu-id="7c757-110">이름, ID, 속성 및 추가 클러스터 세부 정보를 포함하여 지정된 연결된 클러스터의 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="7c757-111">예제</span><span class="sxs-lookup"><span data-stu-id="7c757-111">EXAMPLES</span></span>

### <span data-ttu-id="7c757-112">예제 1: 구독에서 연결된 모든 kubernetes를 얻다</span><span class="sxs-lookup"><span data-stu-id="7c757-112">Example 1: Get all connected kubernetes under a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="7c757-113">이 명령은 구독 아래에 연결된 모든 kubernetes를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="7c757-114">예제 2: 리소스 그룹 아래에서 연결된 모든 kubernetes를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-114">Example 2: Get all connected kubernetes under the resource group</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="7c757-115">이 명령은 리소스 그룹 아래에 연결된 모든 kubernetes를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="7c757-116">예제 3: 연결된 kubernetes를 얻다</span><span class="sxs-lookup"><span data-stu-id="7c757-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="7c757-117">이 명령은 연결된 kubernetes를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="7c757-118">예제 4: 개체에 따라 연결된 kubernetes를 얻다</span><span class="sxs-lookup"><span data-stu-id="7c757-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="7c757-119">이 명령은 개체에 따라 연결된 kubernetes를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="7c757-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c757-120">PARAMETERS</span></span>

### <span data-ttu-id="7c757-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7c757-121">-ClusterName</span></span>
<span data-ttu-id="7c757-122">get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-122">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c757-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c757-123">-DefaultProfile</span></span>
<span data-ttu-id="7c757-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c757-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c757-125">-InputObject</span></span>
<span data-ttu-id="7c757-126">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7c757-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c757-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c757-127">-ResourceGroupName</span></span>
<span data-ttu-id="7c757-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-128">The name of the resource group.</span></span>
<span data-ttu-id="7c757-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c757-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c757-130">-SubscriptionId</span></span>
<span data-ttu-id="7c757-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c757-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c757-132">CommonParameters</span></span>
<span data-ttu-id="7c757-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c757-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c757-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c757-135">입력</span><span class="sxs-lookup"><span data-stu-id="7c757-135">INPUTS</span></span>

### <span data-ttu-id="7c757-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="7c757-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="7c757-137">출력</span><span class="sxs-lookup"><span data-stu-id="7c757-137">OUTPUTS</span></span>

### <span data-ttu-id="7c757-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="7c757-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="7c757-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c757-139">NOTES</span></span>

<span data-ttu-id="7c757-140">별칭</span><span class="sxs-lookup"><span data-stu-id="7c757-140">ALIASES</span></span>

<span data-ttu-id="7c757-141">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7c757-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7c757-142">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c757-143">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7c757-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7c757-144">INPUTOBJECT <IConnectedKubernetesIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c757-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7c757-145">`[ClusterName <String>]`: get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="7c757-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="7c757-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7c757-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7c757-148">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="7c757-149">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7c757-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="7c757-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c757-150">RELATED LINKS</span></span>

