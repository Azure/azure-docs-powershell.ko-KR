---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 7abbe244e702c80f18d2c9e97236f74d60f094bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012480"
---
# <span data-ttu-id="bf793-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="bf793-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="bf793-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf793-102">SYNOPSIS</span></span>
<span data-ttu-id="bf793-103">연결된 클러스터를 삭제하고 Azure Resource Manager에서 추적된 리소스를 제거합니다(ARM.</span><span class="sxs-lookup"><span data-stu-id="bf793-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="bf793-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf793-104">SYNTAX</span></span>

### <span data-ttu-id="bf793-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="bf793-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bf793-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bf793-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bf793-107">설명</span><span class="sxs-lookup"><span data-stu-id="bf793-107">DESCRIPTION</span></span>
<span data-ttu-id="bf793-108">연결된 클러스터를 삭제하고 Azure Resource Manager에서 추적된 리소스를 제거합니다(ARM.</span><span class="sxs-lookup"><span data-stu-id="bf793-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="bf793-109">예제</span><span class="sxs-lookup"><span data-stu-id="bf793-109">EXAMPLES</span></span>

### <span data-ttu-id="bf793-110">예제 1: 연결된 kubernetes 제거</span><span class="sxs-lookup"><span data-stu-id="bf793-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="bf793-111">이 명령은 연결된 kubernetes를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="bf793-112">예제 2: 개체에 따라 연결된 kubernetes 제거</span><span class="sxs-lookup"><span data-stu-id="bf793-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="bf793-113">이 명령은 개체에 따라 연결된 kubernetes를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="bf793-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bf793-114">PARAMETERS</span></span>

### <span data-ttu-id="bf793-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf793-115">-AsJob</span></span>
<span data-ttu-id="bf793-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bf793-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bf793-117">-ClusterName</span></span>
<span data-ttu-id="bf793-118">get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="bf793-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf793-119">-DefaultProfile</span></span>
<span data-ttu-id="bf793-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf793-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf793-121">-InputObject</span></span>
<span data-ttu-id="bf793-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="bf793-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bf793-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="bf793-123">-KubeConfig</span></span>
<span data-ttu-id="bf793-124">kube 구성 파일의 경로</span><span class="sxs-lookup"><span data-stu-id="bf793-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="bf793-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="bf793-125">-KubeContext</span></span>
<span data-ttu-id="bf793-126">현재 컴퓨터의 Kubconfig 컨텍스트</span><span class="sxs-lookup"><span data-stu-id="bf793-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="bf793-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bf793-127">-NoWait</span></span>
<span data-ttu-id="bf793-128">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="bf793-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bf793-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf793-129">-PassThru</span></span>
<span data-ttu-id="bf793-130">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bf793-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf793-131">-ResourceGroupName</span></span>
<span data-ttu-id="bf793-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-132">The name of the resource group.</span></span>
<span data-ttu-id="bf793-133">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bf793-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf793-134">-SubscriptionId</span></span>
<span data-ttu-id="bf793-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bf793-136">-확인</span><span class="sxs-lookup"><span data-stu-id="bf793-136">-Confirm</span></span>
<span data-ttu-id="bf793-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf793-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf793-138">-WhatIf</span></span>
<span data-ttu-id="bf793-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf793-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf793-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf793-141">CommonParameters</span></span>
<span data-ttu-id="bf793-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf793-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf793-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf793-144">입력</span><span class="sxs-lookup"><span data-stu-id="bf793-144">INPUTS</span></span>

### <span data-ttu-id="bf793-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="bf793-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="bf793-146">출력</span><span class="sxs-lookup"><span data-stu-id="bf793-146">OUTPUTS</span></span>

### <span data-ttu-id="bf793-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf793-147">System.Boolean</span></span>

## <span data-ttu-id="bf793-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf793-148">NOTES</span></span>

<span data-ttu-id="bf793-149">별칭</span><span class="sxs-lookup"><span data-stu-id="bf793-149">ALIASES</span></span>

<span data-ttu-id="bf793-150">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="bf793-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bf793-151">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf793-152">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf793-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bf793-153">INPUTOBJECT <IConnectedKubernetesIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bf793-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bf793-154">`[ClusterName <String>]`: get이 호출되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="bf793-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="bf793-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bf793-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bf793-157">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="bf793-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bf793-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="bf793-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf793-159">RELATED LINKS</span></span>

