---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216750"
---
# <span data-ttu-id="8872c-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="8872c-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="8872c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8872c-102">SYNOPSIS</span></span>
<span data-ttu-id="8872c-103">연결 된 클러스터 리소스의 특정 속성을 업데이트 하는 API</span><span class="sxs-lookup"><span data-stu-id="8872c-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="8872c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8872c-104">SYNTAX</span></span>

### <span data-ttu-id="8872c-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8872c-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8872c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8872c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8872c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8872c-107">DESCRIPTION</span></span>
<span data-ttu-id="8872c-108">연결 된 클러스터 리소스의 특정 속성을 업데이트 하는 API</span><span class="sxs-lookup"><span data-stu-id="8872c-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="8872c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8872c-109">EXAMPLES</span></span>

### <span data-ttu-id="8872c-110">예제 1: 연결 된 kubernetes 업데이트</span><span class="sxs-lookup"><span data-stu-id="8872c-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="8872c-111">이 명령은 연결 된 kubernetes를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="8872c-112">예제 2: 개체에의 한 연결 된 kubernetes 업데이트</span><span class="sxs-lookup"><span data-stu-id="8872c-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="8872c-113">이 명령은 연결 된 kubernetes 개체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="8872c-114">변수</span><span class="sxs-lookup"><span data-stu-id="8872c-114">PARAMETERS</span></span>

### <span data-ttu-id="8872c-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8872c-115">-ClusterName</span></span>
<span data-ttu-id="8872c-116">Get이 호출 되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-116">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="8872c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8872c-117">-DefaultProfile</span></span>
<span data-ttu-id="8872c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8872c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8872c-119">-InputObject</span></span>
<span data-ttu-id="8872c-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8872c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8872c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8872c-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-122">The name of the resource group.</span></span>
<span data-ttu-id="8872c-123">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8872c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8872c-124">-SubscriptionId</span></span>
<span data-ttu-id="8872c-125">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8872c-126">태그</span><span class="sxs-lookup"><span data-stu-id="8872c-126">-Tag</span></span>
<span data-ttu-id="8872c-127">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="8872c-127">Resource tags.</span></span>

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

### <span data-ttu-id="8872c-128">-확인</span><span class="sxs-lookup"><span data-stu-id="8872c-128">-Confirm</span></span>
<span data-ttu-id="8872c-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8872c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8872c-130">-WhatIf</span></span>
<span data-ttu-id="8872c-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8872c-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8872c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8872c-133">CommonParameters</span></span>
<span data-ttu-id="8872c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8872c-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8872c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8872c-136">입력</span><span class="sxs-lookup"><span data-stu-id="8872c-136">INPUTS</span></span>

### <span data-ttu-id="8872c-137">ConnectedKubernetes. IConnectedKubernetesIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="8872c-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="8872c-138">출력</span><span class="sxs-lookup"><span data-stu-id="8872c-138">OUTPUTS</span></span>

### <span data-ttu-id="8872c-139">ConnectedKubernetes. Api202001Preview. IConnectedCluster에 대 한</span><span class="sxs-lookup"><span data-stu-id="8872c-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="8872c-140">상속자</span><span class="sxs-lookup"><span data-stu-id="8872c-140">NOTES</span></span>

<span data-ttu-id="8872c-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="8872c-141">ALIASES</span></span>

<span data-ttu-id="8872c-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8872c-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8872c-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8872c-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8872c-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8872c-145">INPUTOBJECT <IConnectedKubernetesIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8872c-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8872c-146">`[ClusterName <String>]`: Get이 호출 되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="8872c-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="8872c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8872c-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8872c-149">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="8872c-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8872c-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="8872c-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8872c-151">RELATED LINKS</span></span>

