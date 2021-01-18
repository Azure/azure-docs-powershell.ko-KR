---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493233"
---
# <span data-ttu-id="0a3cc-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="0a3cc-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="0a3cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="0a3cc-103">사설 클라우드에서 이름으로 클러스터를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="0a3cc-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a3cc-104">SYNTAX</span></span>

### <span data-ttu-id="0a3cc-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="0a3cc-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0a3cc-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="0a3cc-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0a3cc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0a3cc-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0a3cc-108">설명</span><span class="sxs-lookup"><span data-stu-id="0a3cc-108">DESCRIPTION</span></span>
<span data-ttu-id="0a3cc-109">사설 클라우드에서 이름으로 클러스터를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="0a3cc-110">예제</span><span class="sxs-lookup"><span data-stu-id="0a3cc-110">EXAMPLES</span></span>

### <span data-ttu-id="0a3cc-111">예제 1: 클러스터를 얻게</span><span class="sxs-lookup"><span data-stu-id="0a3cc-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="0a3cc-112">클러스터를 얻게</span><span class="sxs-lookup"><span data-stu-id="0a3cc-112">Get cluster</span></span>

### <span data-ttu-id="0a3cc-113">예제 2: 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="0a3cc-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="0a3cc-114">클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="0a3cc-114">List clusters</span></span>

## <span data-ttu-id="0a3cc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a3cc-115">PARAMETERS</span></span>

### <span data-ttu-id="0a3cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a3cc-116">-DefaultProfile</span></span>
<span data-ttu-id="0a3cc-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a3cc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a3cc-118">-InputObject</span></span>
<span data-ttu-id="0a3cc-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0a3cc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0a3cc-120">-Name</span></span>
<span data-ttu-id="0a3cc-121">사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="0a3cc-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="0a3cc-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="0a3cc-122">-PrivateCloudName</span></span>
<span data-ttu-id="0a3cc-123">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="0a3cc-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="0a3cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a3cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a3cc-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-125">The name of the resource group.</span></span>
<span data-ttu-id="0a3cc-126">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0a3cc-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a3cc-127">-SubscriptionId</span></span>
<span data-ttu-id="0a3cc-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0a3cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a3cc-129">CommonParameters</span></span>
<span data-ttu-id="0a3cc-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a3cc-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a3cc-132">입력</span><span class="sxs-lookup"><span data-stu-id="0a3cc-132">INPUTS</span></span>

### <span data-ttu-id="0a3cc-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="0a3cc-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="0a3cc-134">출력</span><span class="sxs-lookup"><span data-stu-id="0a3cc-134">OUTPUTS</span></span>

### <span data-ttu-id="0a3cc-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="0a3cc-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="0a3cc-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a3cc-136">NOTES</span></span>

<span data-ttu-id="0a3cc-137">별칭</span><span class="sxs-lookup"><span data-stu-id="0a3cc-137">ALIASES</span></span>

<span data-ttu-id="0a3cc-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0a3cc-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a3cc-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a3cc-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a3cc-141">INPUTOBJECT: <IVMWareIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0a3cc-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a3cc-142">`[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름</span><span class="sxs-lookup"><span data-stu-id="0a3cc-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="0a3cc-143">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="0a3cc-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="0a3cc-144">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="0a3cc-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="0a3cc-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="0a3cc-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a3cc-146">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="0a3cc-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="0a3cc-147">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="0a3cc-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="0a3cc-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0a3cc-149">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="0a3cc-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0a3cc-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="0a3cc-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a3cc-151">RELATED LINKS</span></span>

