---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204623"
---
# <span data-ttu-id="4d4ab-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="4d4ab-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="4d4ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d4ab-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4ab-103">연결 된 클러스터를 삭제 하 고 (ARM (Azure Resource Manager)에서 추적 된 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="4d4ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d4ab-104">SYNTAX</span></span>

### <span data-ttu-id="4d4ab-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d4ab-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4d4ab-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d4ab-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4d4ab-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4d4ab-107">DESCRIPTION</span></span>
<span data-ttu-id="4d4ab-108">연결 된 클러스터를 삭제 하 고 (ARM (Azure Resource Manager)에서 추적 된 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="4d4ab-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4d4ab-109">EXAMPLES</span></span>

### <span data-ttu-id="4d4ab-110">예제 1: 연결 된 kubernetes 제거</span><span class="sxs-lookup"><span data-stu-id="4d4ab-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="4d4ab-111">이 명령은 연결 된 kubernetes를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="4d4ab-112">예제 2: 개체에 연결 된 kubernetes 제거</span><span class="sxs-lookup"><span data-stu-id="4d4ab-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="4d4ab-113">이 명령은 연결 된 kubernetes 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="4d4ab-114">변수</span><span class="sxs-lookup"><span data-stu-id="4d4ab-114">PARAMETERS</span></span>

### <span data-ttu-id="4d4ab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d4ab-115">-AsJob</span></span>
<span data-ttu-id="4d4ab-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="4d4ab-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4d4ab-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4d4ab-117">-ClusterName</span></span>
<span data-ttu-id="4d4ab-118">Get이 호출 되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="4d4ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4ab-119">-DefaultProfile</span></span>
<span data-ttu-id="4d4ab-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d4ab-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d4ab-121">-InputObject</span></span>
<span data-ttu-id="4d4ab-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d4ab-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="4d4ab-123">-KubeConfig</span></span>
<span data-ttu-id="4d4ab-124">Kube config 파일 경로</span><span class="sxs-lookup"><span data-stu-id="4d4ab-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="4d4ab-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="4d4ab-125">-KubeContext</span></span>
<span data-ttu-id="4d4ab-126">현재 컴퓨터의 kubconfig 컨텍스트</span><span class="sxs-lookup"><span data-stu-id="4d4ab-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="4d4ab-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4d4ab-127">-NoWait</span></span>
<span data-ttu-id="4d4ab-128">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="4d4ab-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4d4ab-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d4ab-129">-PassThru</span></span>
<span data-ttu-id="4d4ab-130">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4d4ab-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d4ab-131">-ResourceGroupName</span></span>
<span data-ttu-id="4d4ab-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-132">The name of the resource group.</span></span>
<span data-ttu-id="4d4ab-133">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4d4ab-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d4ab-134">-SubscriptionId</span></span>
<span data-ttu-id="4d4ab-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4d4ab-136">-확인</span><span class="sxs-lookup"><span data-stu-id="4d4ab-136">-Confirm</span></span>
<span data-ttu-id="4d4ab-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d4ab-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d4ab-138">-WhatIf</span></span>
<span data-ttu-id="4d4ab-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d4ab-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d4ab-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4ab-141">CommonParameters</span></span>
<span data-ttu-id="4d4ab-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4ab-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4ab-144">입력</span><span class="sxs-lookup"><span data-stu-id="4d4ab-144">INPUTS</span></span>

### <span data-ttu-id="4d4ab-145">ConnectedKubernetes. IConnectedKubernetesIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="4d4ab-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="4d4ab-146">출력</span><span class="sxs-lookup"><span data-stu-id="4d4ab-146">OUTPUTS</span></span>

### <span data-ttu-id="4d4ab-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4d4ab-147">System.Boolean</span></span>

## <span data-ttu-id="4d4ab-148">상속자</span><span class="sxs-lookup"><span data-stu-id="4d4ab-148">NOTES</span></span>

<span data-ttu-id="4d4ab-149">별칭과</span><span class="sxs-lookup"><span data-stu-id="4d4ab-149">ALIASES</span></span>

<span data-ttu-id="4d4ab-150">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4d4ab-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d4ab-151">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d4ab-152">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d4ab-153">INPUTOBJECT <IConnectedKubernetesIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4d4ab-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d4ab-154">`[ClusterName <String>]`: Get이 호출 되는 Kubernetes 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="4d4ab-155">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="4d4ab-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d4ab-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4d4ab-157">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="4d4ab-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4ab-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="4d4ab-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d4ab-159">RELATED LINKS</span></span>

