---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491493"
---
# <span data-ttu-id="1de3f-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="1de3f-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="1de3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1de3f-102">SYNOPSIS</span></span>
<span data-ttu-id="1de3f-103">지역별로 구독에 대한 평가판 상태 반환</span><span class="sxs-lookup"><span data-stu-id="1de3f-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="1de3f-104">구문</span><span class="sxs-lookup"><span data-stu-id="1de3f-104">SYNTAX</span></span>

### <span data-ttu-id="1de3f-105">확인(기본값)</span><span class="sxs-lookup"><span data-stu-id="1de3f-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1de3f-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1de3f-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1de3f-107">설명</span><span class="sxs-lookup"><span data-stu-id="1de3f-107">DESCRIPTION</span></span>
<span data-ttu-id="1de3f-108">지역별로 구독에 대한 평가판 상태 반환</span><span class="sxs-lookup"><span data-stu-id="1de3f-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="1de3f-109">예제</span><span class="sxs-lookup"><span data-stu-id="1de3f-109">EXAMPLES</span></span>

### <span data-ttu-id="1de3f-110">예제 1: 평가판 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="1de3f-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="1de3f-111">평가판 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="1de3f-111">Check trial availability</span></span>

## <span data-ttu-id="1de3f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1de3f-112">PARAMETERS</span></span>

### <span data-ttu-id="1de3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de3f-113">-DefaultProfile</span></span>
<span data-ttu-id="1de3f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1de3f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1de3f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1de3f-115">-InputObject</span></span>
<span data-ttu-id="1de3f-116">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1de3f-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1de3f-117">-Location</span><span class="sxs-lookup"><span data-stu-id="1de3f-117">-Location</span></span>
<span data-ttu-id="1de3f-118">Azure 지역</span><span class="sxs-lookup"><span data-stu-id="1de3f-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de3f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1de3f-119">-SubscriptionId</span></span>
<span data-ttu-id="1de3f-120">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1de3f-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de3f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1de3f-121">-Confirm</span></span>
<span data-ttu-id="1de3f-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1de3f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1de3f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1de3f-123">-WhatIf</span></span>
<span data-ttu-id="1de3f-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1de3f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1de3f-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1de3f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1de3f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de3f-126">CommonParameters</span></span>
<span data-ttu-id="1de3f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1de3f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de3f-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1de3f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de3f-129">입력</span><span class="sxs-lookup"><span data-stu-id="1de3f-129">INPUTS</span></span>

### <span data-ttu-id="1de3f-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="1de3f-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="1de3f-131">출력</span><span class="sxs-lookup"><span data-stu-id="1de3f-131">OUTPUTS</span></span>

### <span data-ttu-id="1de3f-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="1de3f-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="1de3f-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1de3f-133">NOTES</span></span>

<span data-ttu-id="1de3f-134">별칭</span><span class="sxs-lookup"><span data-stu-id="1de3f-134">ALIASES</span></span>

<span data-ttu-id="1de3f-135">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1de3f-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1de3f-136">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1de3f-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1de3f-137">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1de3f-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1de3f-138">INPUTOBJECT: <IVMWareIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1de3f-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1de3f-139">`[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름</span><span class="sxs-lookup"><span data-stu-id="1de3f-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="1de3f-140">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="1de3f-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="1de3f-141">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="1de3f-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="1de3f-142">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1de3f-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1de3f-143">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="1de3f-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="1de3f-144">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="1de3f-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="1de3f-145">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1de3f-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1de3f-146">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="1de3f-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="1de3f-147">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1de3f-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1de3f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1de3f-148">RELATED LINKS</span></span>

