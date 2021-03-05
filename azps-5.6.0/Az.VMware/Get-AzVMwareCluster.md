---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 842d0c26d4034a8c07415dfe8524b32623c07e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987196"
---
# <span data-ttu-id="0535f-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="0535f-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="0535f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0535f-102">SYNOPSIS</span></span>
<span data-ttu-id="0535f-103">사설 클라우드에서 클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="0535f-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="0535f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0535f-104">SYNTAX</span></span>

### <span data-ttu-id="0535f-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="0535f-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0535f-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="0535f-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0535f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0535f-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0535f-108">설명</span><span class="sxs-lookup"><span data-stu-id="0535f-108">DESCRIPTION</span></span>
<span data-ttu-id="0535f-109">사설 클라우드에서 클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="0535f-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="0535f-110">예제</span><span class="sxs-lookup"><span data-stu-id="0535f-110">EXAMPLES</span></span>

### <span data-ttu-id="0535f-111">예제 1: 클러스터를 얻다</span><span class="sxs-lookup"><span data-stu-id="0535f-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="0535f-112">클러스터를 얻다</span><span class="sxs-lookup"><span data-stu-id="0535f-112">Get cluster</span></span>

### <span data-ttu-id="0535f-113">예제 2: 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="0535f-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="0535f-114">클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="0535f-114">List clusters</span></span>

## <span data-ttu-id="0535f-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0535f-115">PARAMETERS</span></span>

### <span data-ttu-id="0535f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0535f-116">-DefaultProfile</span></span>
<span data-ttu-id="0535f-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0535f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0535f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0535f-118">-InputObject</span></span>
<span data-ttu-id="0535f-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0535f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0535f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0535f-120">-Name</span></span>
<span data-ttu-id="0535f-121">사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="0535f-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0535f-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0535f-122">-PrivateCloudName</span></span>
<span data-ttu-id="0535f-123">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="0535f-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="0535f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0535f-124">-ResourceGroupName</span></span>
<span data-ttu-id="0535f-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0535f-125">The name of the resource group.</span></span>
<span data-ttu-id="0535f-126">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0535f-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0535f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0535f-127">-SubscriptionId</span></span>
<span data-ttu-id="0535f-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0535f-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0535f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0535f-129">CommonParameters</span></span>
<span data-ttu-id="0535f-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0535f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0535f-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0535f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0535f-132">입력</span><span class="sxs-lookup"><span data-stu-id="0535f-132">INPUTS</span></span>

### <span data-ttu-id="0535f-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="0535f-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="0535f-134">출력</span><span class="sxs-lookup"><span data-stu-id="0535f-134">OUTPUTS</span></span>

### <span data-ttu-id="0535f-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="0535f-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="0535f-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0535f-136">NOTES</span></span>

<span data-ttu-id="0535f-137">별칭</span><span class="sxs-lookup"><span data-stu-id="0535f-137">ALIASES</span></span>

<span data-ttu-id="0535f-138">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0535f-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0535f-139">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0535f-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0535f-140">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0535f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0535f-141">INPUTOBJECT <IVMWareIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0535f-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0535f-142">`[AuthorizationName <String>]`: 사설 클라우드의 ExpressRoute 회로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="0535f-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="0535f-143">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="0535f-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="0535f-144">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise Site 이름</span><span class="sxs-lookup"><span data-stu-id="0535f-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="0535f-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="0535f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0535f-146">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="0535f-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="0535f-147">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="0535f-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="0535f-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0535f-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0535f-149">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0535f-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="0535f-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0535f-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="0535f-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0535f-151">RELATED LINKS</span></span>

