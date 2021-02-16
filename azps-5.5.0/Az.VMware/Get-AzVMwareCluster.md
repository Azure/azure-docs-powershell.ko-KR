---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 51a889abe0d1842f66a0ed9b17f3b07acd85a54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208901"
---
# <span data-ttu-id="89b3d-101">Get-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="89b3d-101">Get-AzVMwareCluster</span></span>

## <span data-ttu-id="89b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="89b3d-103">사설 클라우드에서 이름으로 클러스터를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="89b3d-104">구문</span><span class="sxs-lookup"><span data-stu-id="89b3d-104">SYNTAX</span></span>

### <span data-ttu-id="89b3d-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="89b3d-105">List (Default)</span></span>
```
Get-AzVMwareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="89b3d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="89b3d-106">Get</span></span>
```
Get-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="89b3d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="89b3d-107">GetViaIdentity</span></span>
```
Get-AzVMwareCluster -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="89b3d-108">설명</span><span class="sxs-lookup"><span data-stu-id="89b3d-108">DESCRIPTION</span></span>
<span data-ttu-id="89b3d-109">사설 클라우드에서 이름으로 클러스터를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="89b3d-110">예제</span><span class="sxs-lookup"><span data-stu-id="89b3d-110">EXAMPLES</span></span>

### <span data-ttu-id="89b3d-111">예제 1: 클러스터를 얻게</span><span class="sxs-lookup"><span data-stu-id="89b3d-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="89b3d-112">클러스터를 얻게</span><span class="sxs-lookup"><span data-stu-id="89b3d-112">Get cluster</span></span>

### <span data-ttu-id="89b3d-113">예제 2: 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="89b3d-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="89b3d-114">클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="89b3d-114">List clusters</span></span>

## <span data-ttu-id="89b3d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89b3d-115">PARAMETERS</span></span>

### <span data-ttu-id="89b3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b3d-116">-DefaultProfile</span></span>
<span data-ttu-id="89b3d-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89b3d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89b3d-118">-InputObject</span></span>
<span data-ttu-id="89b3d-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="89b3d-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89b3d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="89b3d-120">-Name</span></span>
<span data-ttu-id="89b3d-121">사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="89b3d-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="89b3d-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="89b3d-122">-PrivateCloudName</span></span>
<span data-ttu-id="89b3d-123">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="89b3d-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="89b3d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b3d-124">-ResourceGroupName</span></span>
<span data-ttu-id="89b3d-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-125">The name of the resource group.</span></span>
<span data-ttu-id="89b3d-126">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="89b3d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89b3d-127">-SubscriptionId</span></span>
<span data-ttu-id="89b3d-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="89b3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b3d-129">CommonParameters</span></span>
<span data-ttu-id="89b3d-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b3d-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="89b3d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b3d-132">입력</span><span class="sxs-lookup"><span data-stu-id="89b3d-132">INPUTS</span></span>

### <span data-ttu-id="89b3d-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="89b3d-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="89b3d-134">출력</span><span class="sxs-lookup"><span data-stu-id="89b3d-134">OUTPUTS</span></span>

### <span data-ttu-id="89b3d-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="89b3d-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="89b3d-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="89b3d-136">NOTES</span></span>

<span data-ttu-id="89b3d-137">별칭</span><span class="sxs-lookup"><span data-stu-id="89b3d-137">ALIASES</span></span>

<span data-ttu-id="89b3d-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="89b3d-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89b3d-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89b3d-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89b3d-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89b3d-141">INPUTOBJECT: <IVMwareIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="89b3d-141">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89b3d-142">`[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름</span><span class="sxs-lookup"><span data-stu-id="89b3d-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="89b3d-143">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="89b3d-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="89b3d-144">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="89b3d-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="89b3d-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="89b3d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89b3d-146">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="89b3d-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="89b3d-147">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="89b3d-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="89b3d-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="89b3d-149">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="89b3d-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="89b3d-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="89b3d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89b3d-151">RELATED LINKS</span></span>

