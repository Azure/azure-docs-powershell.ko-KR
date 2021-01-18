---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493780"
---
# <span data-ttu-id="2e2c1-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="2e2c1-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="2e2c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e2c1-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2c1-103">연결된 클러스터 리소스의 특정 속성을 업데이트하는 API</span><span class="sxs-lookup"><span data-stu-id="2e2c1-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="2e2c1-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e2c1-104">SYNTAX</span></span>

### <span data-ttu-id="2e2c1-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="2e2c1-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2e2c1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2e2c1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2e2c1-107">설명</span><span class="sxs-lookup"><span data-stu-id="2e2c1-107">DESCRIPTION</span></span>
<span data-ttu-id="2e2c1-108">연결된 클러스터 리소스의 특정 속성을 업데이트하는 API</span><span class="sxs-lookup"><span data-stu-id="2e2c1-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="2e2c1-109">예제</span><span class="sxs-lookup"><span data-stu-id="2e2c1-109">EXAMPLES</span></span>

### <span data-ttu-id="2e2c1-110">예제 1: 연결된 kubernetes 업데이트</span><span class="sxs-lookup"><span data-stu-id="2e2c1-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="2e2c1-111">이 명령은 연결된 kubernetes를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="2e2c1-112">예제 2: 개체에 따라 연결된 kubernetes 업데이트</span><span class="sxs-lookup"><span data-stu-id="2e2c1-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="2e2c1-113">이 명령은 개체에 따라 연결된 kubernetes를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="2e2c1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e2c1-114">PARAMETERS</span></span>

### <span data-ttu-id="2e2c1-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2e2c1-115">-ClusterName</span></span>
<span data-ttu-id="2e2c1-116">get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-116">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e2c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e2c1-117">-DefaultProfile</span></span>
<span data-ttu-id="2e2c1-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e2c1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e2c1-119">-InputObject</span></span>
<span data-ttu-id="2e2c1-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e2c1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e2c1-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e2c1-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-122">The name of the resource group.</span></span>
<span data-ttu-id="2e2c1-123">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e2c1-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e2c1-124">-SubscriptionId</span></span>
<span data-ttu-id="2e2c1-125">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e2c1-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e2c1-126">-Tag</span></span>
<span data-ttu-id="2e2c1-127">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-127">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e2c1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e2c1-128">-Confirm</span></span>
<span data-ttu-id="2e2c1-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e2c1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e2c1-130">-WhatIf</span></span>
<span data-ttu-id="2e2c1-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2e2c1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e2c1-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e2c1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2c1-133">CommonParameters</span></span>
<span data-ttu-id="2e2c1-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2c1-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2c1-136">입력</span><span class="sxs-lookup"><span data-stu-id="2e2c1-136">INPUTS</span></span>

### <span data-ttu-id="2e2c1-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="2e2c1-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="2e2c1-138">출력</span><span class="sxs-lookup"><span data-stu-id="2e2c1-138">OUTPUTS</span></span>

### <span data-ttu-id="2e2c1-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="2e2c1-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="2e2c1-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2e2c1-140">NOTES</span></span>

<span data-ttu-id="2e2c1-141">별칭</span><span class="sxs-lookup"><span data-stu-id="2e2c1-141">ALIASES</span></span>

<span data-ttu-id="2e2c1-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2e2c1-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2e2c1-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e2c1-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2e2c1-145">INPUTOBJECT: <IConnectedKubernetesIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2e2c1-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e2c1-146">`[ClusterName <String>]`: get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="2e2c1-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="2e2c1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e2c1-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2e2c1-149">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="2e2c1-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2c1-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="2e2c1-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e2c1-151">RELATED LINKS</span></span>

