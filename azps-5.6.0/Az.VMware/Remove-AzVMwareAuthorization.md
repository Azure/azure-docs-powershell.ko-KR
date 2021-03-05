---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
ms.openlocfilehash: b45e06bd6d70e2c5e0999ce3f9be678580f07048
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987154"
---
# <span data-ttu-id="0bbc8-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="0bbc8-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="0bbc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bbc8-102">SYNOPSIS</span></span>
<span data-ttu-id="0bbc8-103">개인 클라우드에서 ExpressRoute 회로 권한 부여 삭제</span><span class="sxs-lookup"><span data-stu-id="0bbc8-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="0bbc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="0bbc8-104">SYNTAX</span></span>

### <span data-ttu-id="0bbc8-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="0bbc8-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0bbc8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0bbc8-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0bbc8-107">설명</span><span class="sxs-lookup"><span data-stu-id="0bbc8-107">DESCRIPTION</span></span>
<span data-ttu-id="0bbc8-108">개인 클라우드에서 ExpressRoute 회로 권한 부여 삭제</span><span class="sxs-lookup"><span data-stu-id="0bbc8-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="0bbc8-109">예제</span><span class="sxs-lookup"><span data-stu-id="0bbc8-109">EXAMPLES</span></span>

### <span data-ttu-id="0bbc8-110">예제 1: 사설 클라우드에 대한 권한 삭제</span><span class="sxs-lookup"><span data-stu-id="0bbc8-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="0bbc8-111">사설 클라우드에 대한 권한 삭제</span><span class="sxs-lookup"><span data-stu-id="0bbc8-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="0bbc8-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0bbc8-112">PARAMETERS</span></span>

### <span data-ttu-id="0bbc8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bbc8-113">-AsJob</span></span>
<span data-ttu-id="0bbc8-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0bbc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bbc8-115">-DefaultProfile</span></span>
<span data-ttu-id="0bbc8-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bbc8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bbc8-117">-InputObject</span></span>
<span data-ttu-id="0bbc8-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bbc8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0bbc8-119">-Name</span></span>
<span data-ttu-id="0bbc8-120">개인 클라우드의 ExpressRoute 회로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="0bbc8-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bbc8-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0bbc8-121">-NoWait</span></span>
<span data-ttu-id="0bbc8-122">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="0bbc8-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0bbc8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bbc8-123">-PassThru</span></span>
<span data-ttu-id="0bbc8-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0bbc8-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0bbc8-125">-PrivateCloudName</span></span>
<span data-ttu-id="0bbc8-126">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="0bbc8-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="0bbc8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bbc8-127">-ResourceGroupName</span></span>
<span data-ttu-id="0bbc8-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-128">The name of the resource group.</span></span>
<span data-ttu-id="0bbc8-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0bbc8-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0bbc8-130">-SubscriptionId</span></span>
<span data-ttu-id="0bbc8-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0bbc8-132">-확인</span><span class="sxs-lookup"><span data-stu-id="0bbc8-132">-Confirm</span></span>
<span data-ttu-id="0bbc8-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bbc8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bbc8-134">-WhatIf</span></span>
<span data-ttu-id="0bbc8-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bbc8-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bbc8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bbc8-137">CommonParameters</span></span>
<span data-ttu-id="0bbc8-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bbc8-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bbc8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bbc8-140">입력</span><span class="sxs-lookup"><span data-stu-id="0bbc8-140">INPUTS</span></span>

### <span data-ttu-id="0bbc8-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="0bbc8-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="0bbc8-142">출력</span><span class="sxs-lookup"><span data-stu-id="0bbc8-142">OUTPUTS</span></span>

### <span data-ttu-id="0bbc8-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0bbc8-143">System.Boolean</span></span>

## <span data-ttu-id="0bbc8-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0bbc8-144">NOTES</span></span>

<span data-ttu-id="0bbc8-145">별칭</span><span class="sxs-lookup"><span data-stu-id="0bbc8-145">ALIASES</span></span>

<span data-ttu-id="0bbc8-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0bbc8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0bbc8-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0bbc8-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0bbc8-149">INPUTOBJECT <IVMWareIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0bbc8-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0bbc8-150">`[AuthorizationName <String>]`: 사설 클라우드의 ExpressRoute 회로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="0bbc8-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="0bbc8-151">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="0bbc8-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="0bbc8-152">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise Site 이름</span><span class="sxs-lookup"><span data-stu-id="0bbc8-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="0bbc8-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="0bbc8-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0bbc8-154">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="0bbc8-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="0bbc8-155">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="0bbc8-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="0bbc8-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0bbc8-157">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="0bbc8-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0bbc8-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="0bbc8-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bbc8-159">RELATED LINKS</span></span>

