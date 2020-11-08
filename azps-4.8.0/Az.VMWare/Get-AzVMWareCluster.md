---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047441"
---
# <span data-ttu-id="a7b37-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="a7b37-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="a7b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7b37-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b37-103">사설 클라우드에서 이름으로 클러스터 가져오기</span><span class="sxs-lookup"><span data-stu-id="a7b37-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="a7b37-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7b37-104">SYNTAX</span></span>

### <span data-ttu-id="a7b37-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a7b37-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7b37-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="a7b37-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7b37-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a7b37-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a7b37-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a7b37-108">DESCRIPTION</span></span>
<span data-ttu-id="a7b37-109">사설 클라우드에서 이름으로 클러스터 가져오기</span><span class="sxs-lookup"><span data-stu-id="a7b37-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="a7b37-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a7b37-110">EXAMPLES</span></span>

### <span data-ttu-id="a7b37-111">예제 1: 클러스터 가져오기</span><span class="sxs-lookup"><span data-stu-id="a7b37-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="a7b37-112">클러스터 가져오기</span><span class="sxs-lookup"><span data-stu-id="a7b37-112">Get cluster</span></span>

### <span data-ttu-id="a7b37-113">예제 2: 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="a7b37-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="a7b37-114">클러스터 목록</span><span class="sxs-lookup"><span data-stu-id="a7b37-114">List clusters</span></span>

## <span data-ttu-id="a7b37-115">변수</span><span class="sxs-lookup"><span data-stu-id="a7b37-115">PARAMETERS</span></span>

### <span data-ttu-id="a7b37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b37-116">-DefaultProfile</span></span>
<span data-ttu-id="a7b37-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7b37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7b37-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7b37-118">-InputObject</span></span>
<span data-ttu-id="a7b37-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7b37-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7b37-120">-이름</span><span class="sxs-lookup"><span data-stu-id="a7b37-120">-Name</span></span>
<span data-ttu-id="a7b37-121">사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="a7b37-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="a7b37-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="a7b37-122">-PrivateCloudName</span></span>
<span data-ttu-id="a7b37-123">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="a7b37-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="a7b37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7b37-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7b37-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7b37-125">The name of the resource group.</span></span>
<span data-ttu-id="a7b37-126">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b37-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a7b37-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7b37-127">-SubscriptionId</span></span>
<span data-ttu-id="a7b37-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a7b37-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a7b37-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b37-129">CommonParameters</span></span>
<span data-ttu-id="a7b37-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b37-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b37-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7b37-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b37-132">입력</span><span class="sxs-lookup"><span data-stu-id="a7b37-132">INPUTS</span></span>

### <span data-ttu-id="a7b37-133">IVMWareIdentity (Microsoft. v.</span><span class="sxs-lookup"><span data-stu-id="a7b37-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="a7b37-134">출력</span><span class="sxs-lookup"><span data-stu-id="a7b37-134">OUTPUTS</span></span>

### <span data-ttu-id="a7b37-135">Api20200320. ICluster에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a7b37-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="a7b37-136">상속자</span><span class="sxs-lookup"><span data-stu-id="a7b37-136">NOTES</span></span>

<span data-ttu-id="a7b37-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="a7b37-137">ALIASES</span></span>

<span data-ttu-id="a7b37-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a7b37-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7b37-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b37-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7b37-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7b37-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7b37-141">INPUTOBJECT <IVMWareIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a7b37-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7b37-142">`[AuthorizationName <String>]`: 사설 클라우드의 Express 경로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="a7b37-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="a7b37-143">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="a7b37-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="a7b37-144">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="a7b37-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="a7b37-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="a7b37-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7b37-146">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="a7b37-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="a7b37-147">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="a7b37-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="a7b37-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7b37-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a7b37-149">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7b37-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="a7b37-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a7b37-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="a7b37-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7b37-151">RELATED LINKS</span></span>

