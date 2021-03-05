---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
ms.openlocfilehash: ae53ac56d60d61340e2592233901556a0e1d6b62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988652"
---
# <span data-ttu-id="cfec1-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="cfec1-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="cfec1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfec1-102">SYNOPSIS</span></span>
<span data-ttu-id="cfec1-103">사설 클라우드 사용</span><span class="sxs-lookup"><span data-stu-id="cfec1-103">Get a private cloud</span></span>

## <span data-ttu-id="cfec1-104">구문</span><span class="sxs-lookup"><span data-stu-id="cfec1-104">SYNTAX</span></span>

### <span data-ttu-id="cfec1-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="cfec1-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cfec1-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="cfec1-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cfec1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cfec1-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cfec1-108">목록</span><span class="sxs-lookup"><span data-stu-id="cfec1-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfec1-109">설명</span><span class="sxs-lookup"><span data-stu-id="cfec1-109">DESCRIPTION</span></span>
<span data-ttu-id="cfec1-110">사설 클라우드 사용</span><span class="sxs-lookup"><span data-stu-id="cfec1-110">Get a private cloud</span></span>

## <span data-ttu-id="cfec1-111">예제</span><span class="sxs-lookup"><span data-stu-id="cfec1-111">EXAMPLES</span></span>

### <span data-ttu-id="cfec1-112">예제 1: 구독 아래에 사설 클라우드 나열</span><span class="sxs-lookup"><span data-stu-id="cfec1-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="cfec1-113">구독 아래에 사설 클라우드 나열</span><span class="sxs-lookup"><span data-stu-id="cfec1-113">List private cloud under subscription</span></span>

### <span data-ttu-id="cfec1-114">예제 2: 리소스 그룹 아래에 사설 클라우드 나열</span><span class="sxs-lookup"><span data-stu-id="cfec1-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="cfec1-115">리소스 그룹 아래에 사설 클라우드 나열</span><span class="sxs-lookup"><span data-stu-id="cfec1-115">List private cloud under resource group</span></span>

### <span data-ttu-id="cfec1-116">예제 3: 사설 클라우드 사용</span><span class="sxs-lookup"><span data-stu-id="cfec1-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="cfec1-117">사설 클라우드 사용</span><span class="sxs-lookup"><span data-stu-id="cfec1-117">Get private cloud</span></span>

## <span data-ttu-id="cfec1-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cfec1-118">PARAMETERS</span></span>

### <span data-ttu-id="cfec1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfec1-119">-DefaultProfile</span></span>
<span data-ttu-id="cfec1-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfec1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfec1-121">-InputObject</span></span>
<span data-ttu-id="cfec1-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="cfec1-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfec1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cfec1-123">-Name</span></span>
<span data-ttu-id="cfec1-124">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="cfec1-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfec1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfec1-125">-ResourceGroupName</span></span>
<span data-ttu-id="cfec1-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec1-126">The name of the resource group.</span></span>
<span data-ttu-id="cfec1-127">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="cfec1-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cfec1-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cfec1-128">-SubscriptionId</span></span>
<span data-ttu-id="cfec1-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec1-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cfec1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfec1-130">CommonParameters</span></span>
<span data-ttu-id="cfec1-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cfec1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfec1-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfec1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfec1-133">입력</span><span class="sxs-lookup"><span data-stu-id="cfec1-133">INPUTS</span></span>

### <span data-ttu-id="cfec1-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="cfec1-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="cfec1-135">출력</span><span class="sxs-lookup"><span data-stu-id="cfec1-135">OUTPUTS</span></span>

### <span data-ttu-id="cfec1-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="cfec1-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="cfec1-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cfec1-137">NOTES</span></span>

<span data-ttu-id="cfec1-138">별칭</span><span class="sxs-lookup"><span data-stu-id="cfec1-138">ALIASES</span></span>

<span data-ttu-id="cfec1-139">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="cfec1-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cfec1-140">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cfec1-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cfec1-141">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cfec1-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cfec1-142">INPUTOBJECT <IVMWareIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cfec1-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cfec1-143">`[AuthorizationName <String>]`: 사설 클라우드의 ExpressRoute 회로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="cfec1-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="cfec1-144">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="cfec1-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="cfec1-145">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise Site 이름</span><span class="sxs-lookup"><span data-stu-id="cfec1-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="cfec1-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="cfec1-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cfec1-147">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="cfec1-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="cfec1-148">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="cfec1-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="cfec1-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec1-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cfec1-150">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="cfec1-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="cfec1-151">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cfec1-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="cfec1-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cfec1-152">RELATED LINKS</span></span>

