---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495876"
---
# <span data-ttu-id="d74ea-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="d74ea-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="d74ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d74ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d74ea-103">연결된 클러스터를 삭제하고 Azure Resource Manager에서 추적된 리소스를 제거합니다(ARM.</span><span class="sxs-lookup"><span data-stu-id="d74ea-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="d74ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="d74ea-104">SYNTAX</span></span>

### <span data-ttu-id="d74ea-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="d74ea-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d74ea-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d74ea-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d74ea-107">설명</span><span class="sxs-lookup"><span data-stu-id="d74ea-107">DESCRIPTION</span></span>
<span data-ttu-id="d74ea-108">연결된 클러스터를 삭제하고 Azure Resource Manager에서 추적된 리소스를 제거합니다(ARM.</span><span class="sxs-lookup"><span data-stu-id="d74ea-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="d74ea-109">예제</span><span class="sxs-lookup"><span data-stu-id="d74ea-109">EXAMPLES</span></span>

### <span data-ttu-id="d74ea-110">예제 1: 연결된 kubernetes 제거</span><span class="sxs-lookup"><span data-stu-id="d74ea-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="d74ea-111">이 명령은 연결된 kubernetes를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="d74ea-112">예제 2: 개체에 의해 연결된 kubernetes 제거</span><span class="sxs-lookup"><span data-stu-id="d74ea-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="d74ea-113">이 명령은 개체에 의해 연결된 kubernetes를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="d74ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d74ea-114">PARAMETERS</span></span>

### <span data-ttu-id="d74ea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d74ea-115">-AsJob</span></span>
<span data-ttu-id="d74ea-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d74ea-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d74ea-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d74ea-117">-ClusterName</span></span>
<span data-ttu-id="d74ea-118">get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74ea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74ea-119">-DefaultProfile</span></span>
<span data-ttu-id="d74ea-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d74ea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d74ea-121">-InputObject</span></span>
<span data-ttu-id="d74ea-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d74ea-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d74ea-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="d74ea-123">-KubeConfig</span></span>
<span data-ttu-id="d74ea-124">kube 구성 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="d74ea-124">Path to the kube config file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74ea-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="d74ea-125">-KubeContext</span></span>
<span data-ttu-id="d74ea-126">현재 컴퓨터의 Kubconfig 컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d74ea-126">Kubconfig context from current machine</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74ea-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d74ea-127">-NoWait</span></span>
<span data-ttu-id="d74ea-128">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="d74ea-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d74ea-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d74ea-129">-PassThru</span></span>
<span data-ttu-id="d74ea-130">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d74ea-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d74ea-131">-ResourceGroupName</span></span>
<span data-ttu-id="d74ea-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-132">The name of the resource group.</span></span>
<span data-ttu-id="d74ea-133">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74ea-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d74ea-134">-SubscriptionId</span></span>
<span data-ttu-id="d74ea-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74ea-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d74ea-136">-Confirm</span></span>
<span data-ttu-id="d74ea-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d74ea-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74ea-138">-WhatIf</span></span>
<span data-ttu-id="d74ea-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d74ea-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d74ea-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d74ea-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74ea-141">CommonParameters</span></span>
<span data-ttu-id="d74ea-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74ea-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d74ea-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74ea-144">입력</span><span class="sxs-lookup"><span data-stu-id="d74ea-144">INPUTS</span></span>

### <span data-ttu-id="d74ea-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="d74ea-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="d74ea-146">출력</span><span class="sxs-lookup"><span data-stu-id="d74ea-146">OUTPUTS</span></span>

### <span data-ttu-id="d74ea-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d74ea-147">System.Boolean</span></span>

## <span data-ttu-id="d74ea-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d74ea-148">NOTES</span></span>

<span data-ttu-id="d74ea-149">별칭</span><span class="sxs-lookup"><span data-stu-id="d74ea-149">ALIASES</span></span>

<span data-ttu-id="d74ea-150">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d74ea-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d74ea-151">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d74ea-152">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d74ea-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d74ea-153">INPUTOBJECT: <IConnectedKubernetesIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d74ea-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d74ea-154">`[ClusterName <String>]`: get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="d74ea-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d74ea-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d74ea-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d74ea-157">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="d74ea-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ea-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d74ea-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d74ea-159">RELATED LINKS</span></span>

