---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491503"
---
# <span data-ttu-id="b34de-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="b34de-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="b34de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b34de-102">SYNOPSIS</span></span>
<span data-ttu-id="b34de-103">사설 클라우드 삭제</span><span class="sxs-lookup"><span data-stu-id="b34de-103">Delete a private cloud</span></span>

## <span data-ttu-id="b34de-104">구문</span><span class="sxs-lookup"><span data-stu-id="b34de-104">SYNTAX</span></span>

### <span data-ttu-id="b34de-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="b34de-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b34de-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b34de-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b34de-107">설명</span><span class="sxs-lookup"><span data-stu-id="b34de-107">DESCRIPTION</span></span>
<span data-ttu-id="b34de-108">사설 클라우드 삭제</span><span class="sxs-lookup"><span data-stu-id="b34de-108">Delete a private cloud</span></span>

## <span data-ttu-id="b34de-109">예제</span><span class="sxs-lookup"><span data-stu-id="b34de-109">EXAMPLES</span></span>

### <span data-ttu-id="b34de-110">예제 1: 사설 클라우드 삭제</span><span class="sxs-lookup"><span data-stu-id="b34de-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="b34de-111">사설 클라우드 삭제</span><span class="sxs-lookup"><span data-stu-id="b34de-111">Delete private cloud</span></span>

## <span data-ttu-id="b34de-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b34de-112">PARAMETERS</span></span>

### <span data-ttu-id="b34de-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b34de-113">-AsJob</span></span>
<span data-ttu-id="b34de-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b34de-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b34de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34de-115">-DefaultProfile</span></span>
<span data-ttu-id="b34de-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b34de-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b34de-117">-InputObject</span></span>
<span data-ttu-id="b34de-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b34de-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b34de-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b34de-119">-Name</span></span>
<span data-ttu-id="b34de-120">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="b34de-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34de-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b34de-121">-NoWait</span></span>
<span data-ttu-id="b34de-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="b34de-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b34de-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b34de-123">-PassThru</span></span>
<span data-ttu-id="b34de-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b34de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34de-125">-ResourceGroupName</span></span>
<span data-ttu-id="b34de-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-126">The name of the resource group.</span></span>
<span data-ttu-id="b34de-127">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b34de-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b34de-128">-SubscriptionId</span></span>
<span data-ttu-id="b34de-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b34de-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b34de-130">-Confirm</span></span>
<span data-ttu-id="b34de-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b34de-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b34de-132">-WhatIf</span></span>
<span data-ttu-id="b34de-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b34de-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b34de-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b34de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34de-135">CommonParameters</span></span>
<span data-ttu-id="b34de-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34de-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b34de-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34de-138">입력</span><span class="sxs-lookup"><span data-stu-id="b34de-138">INPUTS</span></span>

### <span data-ttu-id="b34de-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="b34de-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="b34de-140">출력</span><span class="sxs-lookup"><span data-stu-id="b34de-140">OUTPUTS</span></span>

### <span data-ttu-id="b34de-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b34de-141">System.Boolean</span></span>

## <span data-ttu-id="b34de-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b34de-142">NOTES</span></span>

<span data-ttu-id="b34de-143">별칭</span><span class="sxs-lookup"><span data-stu-id="b34de-143">ALIASES</span></span>

<span data-ttu-id="b34de-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b34de-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b34de-145">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b34de-146">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b34de-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b34de-147">INPUTOBJECT: <IVMWareIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b34de-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b34de-148">`[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름</span><span class="sxs-lookup"><span data-stu-id="b34de-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="b34de-149">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="b34de-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="b34de-150">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="b34de-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="b34de-151">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b34de-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b34de-152">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="b34de-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="b34de-153">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="b34de-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="b34de-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b34de-155">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="b34de-156">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b34de-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="b34de-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b34de-157">RELATED LINKS</span></span>

