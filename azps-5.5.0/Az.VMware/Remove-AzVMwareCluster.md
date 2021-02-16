---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareCluster.md
ms.openlocfilehash: 3b47213cab20abdee5d87e721f3c9a19a10f042c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195505"
---
# <span data-ttu-id="fb294-101">Remove-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="fb294-101">Remove-AzVMwareCluster</span></span>

## <span data-ttu-id="fb294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb294-102">SYNOPSIS</span></span>
<span data-ttu-id="fb294-103">사설 클라우드에서 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="fb294-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="fb294-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb294-104">SYNTAX</span></span>

### <span data-ttu-id="fb294-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb294-105">Delete (Default)</span></span>
```
Remove-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fb294-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fb294-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwareCluster -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb294-107">설명</span><span class="sxs-lookup"><span data-stu-id="fb294-107">DESCRIPTION</span></span>
<span data-ttu-id="fb294-108">사설 클라우드에서 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="fb294-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="fb294-109">예제</span><span class="sxs-lookup"><span data-stu-id="fb294-109">EXAMPLES</span></span>

### <span data-ttu-id="fb294-110">예제 1: 사설 클라우드에서 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="fb294-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="fb294-111">사설 클라우드에서 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="fb294-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="fb294-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb294-112">PARAMETERS</span></span>

### <span data-ttu-id="fb294-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb294-113">-AsJob</span></span>
<span data-ttu-id="fb294-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="fb294-114">Run the command as a job</span></span>

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

### <span data-ttu-id="fb294-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb294-115">-DefaultProfile</span></span>
<span data-ttu-id="fb294-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb294-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb294-117">-InputObject</span></span>
<span data-ttu-id="fb294-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="fb294-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb294-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fb294-119">-Name</span></span>
<span data-ttu-id="fb294-120">사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="fb294-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb294-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fb294-121">-NoWait</span></span>
<span data-ttu-id="fb294-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="fb294-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fb294-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb294-123">-PassThru</span></span>
<span data-ttu-id="fb294-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fb294-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="fb294-125">-PrivateCloudName</span></span>
<span data-ttu-id="fb294-126">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="fb294-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="fb294-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb294-127">-ResourceGroupName</span></span>
<span data-ttu-id="fb294-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-128">The name of the resource group.</span></span>
<span data-ttu-id="fb294-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fb294-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb294-130">-SubscriptionId</span></span>
<span data-ttu-id="fb294-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fb294-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb294-132">-Confirm</span></span>
<span data-ttu-id="fb294-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb294-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb294-134">-WhatIf</span></span>
<span data-ttu-id="fb294-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fb294-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb294-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb294-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb294-137">CommonParameters</span></span>
<span data-ttu-id="fb294-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb294-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb294-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb294-140">입력</span><span class="sxs-lookup"><span data-stu-id="fb294-140">INPUTS</span></span>

### <span data-ttu-id="fb294-141">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="fb294-141">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="fb294-142">출력</span><span class="sxs-lookup"><span data-stu-id="fb294-142">OUTPUTS</span></span>

### <span data-ttu-id="fb294-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb294-143">System.Boolean</span></span>

## <span data-ttu-id="fb294-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb294-144">NOTES</span></span>

<span data-ttu-id="fb294-145">별칭</span><span class="sxs-lookup"><span data-stu-id="fb294-145">ALIASES</span></span>

<span data-ttu-id="fb294-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="fb294-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fb294-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb294-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fb294-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fb294-149">INPUTOBJECT: <IVMwareIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="fb294-149">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fb294-150">`[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름</span><span class="sxs-lookup"><span data-stu-id="fb294-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="fb294-151">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="fb294-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="fb294-152">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="fb294-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="fb294-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="fb294-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fb294-154">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="fb294-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="fb294-155">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="fb294-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="fb294-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fb294-157">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="fb294-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fb294-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="fb294-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb294-159">RELATED LINKS</span></span>

