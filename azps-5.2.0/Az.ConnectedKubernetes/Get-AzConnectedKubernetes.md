---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344738"
---
# <span data-ttu-id="1c861-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="1c861-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="1c861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c861-102">SYNOPSIS</span></span>
<span data-ttu-id="1c861-103">이름, ID, 속성 및 추가 클러스터 세부 정보를 포함하여 지정된 연결된 클러스터의 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="1c861-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c861-104">SYNTAX</span></span>

### <span data-ttu-id="1c861-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c861-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c861-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="1c861-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c861-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1c861-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c861-108">목록</span><span class="sxs-lookup"><span data-stu-id="1c861-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1c861-109">설명</span><span class="sxs-lookup"><span data-stu-id="1c861-109">DESCRIPTION</span></span>
<span data-ttu-id="1c861-110">이름, ID, 속성 및 추가 클러스터 세부 정보를 포함하여 지정된 연결된 클러스터의 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="1c861-111">예제</span><span class="sxs-lookup"><span data-stu-id="1c861-111">EXAMPLES</span></span>

### <span data-ttu-id="1c861-112">예제 1: 구독에서 연결된 모든 kubernetes를 얻게</span><span class="sxs-lookup"><span data-stu-id="1c861-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="1c861-113">이 명령은 구독에서 연결된 모든 kubernetes를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="1c861-114">예제 2: 리소스 그룹에서 연결된 모든 kubernetes를 얻게</span><span class="sxs-lookup"><span data-stu-id="1c861-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="1c861-115">이 명령은 리소스 그룹 아래에 연결된 모든 kubernetes를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="1c861-116">예제 3: 연결된 kubernetes를 얻게</span><span class="sxs-lookup"><span data-stu-id="1c861-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="1c861-117">이 명령은 연결된 kubernetes를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="1c861-118">예제 4: 개체로 연결된 kubernetes를 얻게</span><span class="sxs-lookup"><span data-stu-id="1c861-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="1c861-119">이 명령은 개체에 의해 연결된 kubernetes를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="1c861-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c861-120">PARAMETERS</span></span>

### <span data-ttu-id="1c861-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1c861-121">-ClusterName</span></span>
<span data-ttu-id="1c861-122">get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="1c861-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c861-123">-DefaultProfile</span></span>
<span data-ttu-id="1c861-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c861-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c861-125">-InputObject</span></span>
<span data-ttu-id="1c861-126">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1c861-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1c861-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c861-127">-ResourceGroupName</span></span>
<span data-ttu-id="1c861-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-128">The name of the resource group.</span></span>
<span data-ttu-id="1c861-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1c861-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c861-130">-SubscriptionId</span></span>
<span data-ttu-id="1c861-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1c861-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c861-132">CommonParameters</span></span>
<span data-ttu-id="1c861-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c861-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c861-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c861-135">입력</span><span class="sxs-lookup"><span data-stu-id="1c861-135">INPUTS</span></span>

### <span data-ttu-id="1c861-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="1c861-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="1c861-137">출력</span><span class="sxs-lookup"><span data-stu-id="1c861-137">OUTPUTS</span></span>

### <span data-ttu-id="1c861-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="1c861-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="1c861-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c861-139">NOTES</span></span>

<span data-ttu-id="1c861-140">별칭</span><span class="sxs-lookup"><span data-stu-id="1c861-140">ALIASES</span></span>

<span data-ttu-id="1c861-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1c861-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1c861-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c861-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c861-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1c861-144">INPUTOBJECT: <IConnectedKubernetesIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1c861-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c861-145">`[ClusterName <String>]`: get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="1c861-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1c861-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c861-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1c861-148">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="1c861-149">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c861-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1c861-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c861-150">RELATED LINKS</span></span>

