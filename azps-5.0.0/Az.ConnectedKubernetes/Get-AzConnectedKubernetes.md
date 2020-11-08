---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216753"
---
# <span data-ttu-id="800cc-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="800cc-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="800cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="800cc-102">SYNOPSIS</span></span>
<span data-ttu-id="800cc-103">이름, id, 속성, 추가 클러스터 세부 정보를 포함 하 여, 지정 된 연결 클러스터의 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="800cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="800cc-104">SYNTAX</span></span>

### <span data-ttu-id="800cc-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="800cc-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="800cc-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="800cc-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="800cc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="800cc-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="800cc-108">목록</span><span class="sxs-lookup"><span data-stu-id="800cc-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="800cc-109">설명은</span><span class="sxs-lookup"><span data-stu-id="800cc-109">DESCRIPTION</span></span>
<span data-ttu-id="800cc-110">이름, id, 속성, 추가 클러스터 세부 정보를 포함 하 여, 지정 된 연결 클러스터의 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="800cc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="800cc-111">EXAMPLES</span></span>

### <span data-ttu-id="800cc-112">예제 1: 구독 하에 모든 연결 된 kubernetes 가져오기</span><span class="sxs-lookup"><span data-stu-id="800cc-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="800cc-113">이 명령은 구독 하는 모든 연결 된 kubernetes를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="800cc-114">예제 2: 리소스 그룹 아래에 연결 된 모든 kubernetes 가져오기</span><span class="sxs-lookup"><span data-stu-id="800cc-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="800cc-115">이 명령은 리소스 그룹 아래에 연결 된 모든 kubernetes를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="800cc-116">예제 3: 연결 된 kubernetes 가져오기</span><span class="sxs-lookup"><span data-stu-id="800cc-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="800cc-117">이 명령은 연결 된 kubernetes를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="800cc-118">예제 4: kubernetes에 연결 된 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="800cc-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="800cc-119">이 명령은 연결 된 kubernetes 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="800cc-120">변수</span><span class="sxs-lookup"><span data-stu-id="800cc-120">PARAMETERS</span></span>

### <span data-ttu-id="800cc-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="800cc-121">-ClusterName</span></span>
<span data-ttu-id="800cc-122">Get이 호출 되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="800cc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800cc-123">-DefaultProfile</span></span>
<span data-ttu-id="800cc-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="800cc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="800cc-125">-InputObject</span></span>
<span data-ttu-id="800cc-126">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="800cc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="800cc-127">-ResourceGroupName</span></span>
<span data-ttu-id="800cc-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-128">The name of the resource group.</span></span>
<span data-ttu-id="800cc-129">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="800cc-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="800cc-130">-SubscriptionId</span></span>
<span data-ttu-id="800cc-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="800cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800cc-132">CommonParameters</span></span>
<span data-ttu-id="800cc-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800cc-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="800cc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800cc-135">입력</span><span class="sxs-lookup"><span data-stu-id="800cc-135">INPUTS</span></span>

### <span data-ttu-id="800cc-136">ConnectedKubernetes. IConnectedKubernetesIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="800cc-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="800cc-137">출력</span><span class="sxs-lookup"><span data-stu-id="800cc-137">OUTPUTS</span></span>

### <span data-ttu-id="800cc-138">ConnectedKubernetes. Api202001Preview. IConnectedCluster에 대 한</span><span class="sxs-lookup"><span data-stu-id="800cc-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="800cc-139">상속자</span><span class="sxs-lookup"><span data-stu-id="800cc-139">NOTES</span></span>

<span data-ttu-id="800cc-140">별칭과</span><span class="sxs-lookup"><span data-stu-id="800cc-140">ALIASES</span></span>

<span data-ttu-id="800cc-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="800cc-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="800cc-142">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="800cc-143">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="800cc-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="800cc-144">INPUTOBJECT <IConnectedKubernetesIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="800cc-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="800cc-145">`[ClusterName <String>]`: Get이 호출 되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="800cc-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="800cc-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="800cc-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="800cc-148">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="800cc-149">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="800cc-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="800cc-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="800cc-150">RELATED LINKS</span></span>

