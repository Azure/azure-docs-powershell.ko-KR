---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047443"
---
# <span data-ttu-id="1e3f3-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="1e3f3-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="1e3f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3f3-103">사설 클라우드의 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="1e3f3-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="1e3f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e3f3-104">SYNTAX</span></span>

### <span data-ttu-id="1e3f3-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1e3f3-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e3f3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1e3f3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e3f3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1e3f3-107">DESCRIPTION</span></span>
<span data-ttu-id="1e3f3-108">사설 클라우드의 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="1e3f3-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="1e3f3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1e3f3-109">EXAMPLES</span></span>

### <span data-ttu-id="1e3f3-110">예제 1: 이름으로 클러스터 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="1e3f3-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="1e3f3-111">클러스터 크기를 이름으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1e3f3-111">Update cluster size by name</span></span>

### <span data-ttu-id="1e3f3-112">예제 2: 입력 개체 별로 클러스터 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="1e3f3-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="1e3f3-113">입력 개체 별로 클러스터 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="1e3f3-113">Update cluster size by input object</span></span>

## <span data-ttu-id="1e3f3-114">변수</span><span class="sxs-lookup"><span data-stu-id="1e3f3-114">PARAMETERS</span></span>

### <span data-ttu-id="1e3f3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e3f3-115">-AsJob</span></span>
<span data-ttu-id="1e3f3-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1e3f3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1e3f3-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="1e3f3-117">-ClusterSize</span></span>
<span data-ttu-id="1e3f3-118">클러스터 크기</span><span class="sxs-lookup"><span data-stu-id="1e3f3-118">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3f3-119">-DefaultProfile</span></span>
<span data-ttu-id="1e3f3-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e3f3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e3f3-121">-InputObject</span></span>
<span data-ttu-id="1e3f3-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e3f3-123">-이름</span><span class="sxs-lookup"><span data-stu-id="1e3f3-123">-Name</span></span>
<span data-ttu-id="1e3f3-124">사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="1e3f3-124">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3f3-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1e3f3-125">-NoWait</span></span>
<span data-ttu-id="1e3f3-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1e3f3-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1e3f3-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="1e3f3-127">-PrivateCloudName</span></span>
<span data-ttu-id="1e3f3-128">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="1e3f3-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3f3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3f3-129">-ResourceGroupName</span></span>
<span data-ttu-id="1e3f3-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-130">The name of the resource group.</span></span>
<span data-ttu-id="1e3f3-131">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3f3-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e3f3-132">-SubscriptionId</span></span>
<span data-ttu-id="1e3f3-133">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3f3-134">-확인</span><span class="sxs-lookup"><span data-stu-id="1e3f3-134">-Confirm</span></span>
<span data-ttu-id="1e3f3-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e3f3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e3f3-136">-WhatIf</span></span>
<span data-ttu-id="1e3f3-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e3f3-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e3f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3f3-139">CommonParameters</span></span>
<span data-ttu-id="1e3f3-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3f3-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3f3-142">입력</span><span class="sxs-lookup"><span data-stu-id="1e3f3-142">INPUTS</span></span>

### <span data-ttu-id="1e3f3-143">IVMWareIdentity (Microsoft. v.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="1e3f3-144">출력</span><span class="sxs-lookup"><span data-stu-id="1e3f3-144">OUTPUTS</span></span>

### <span data-ttu-id="1e3f3-145">Api20200320. ICluster에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="1e3f3-146">상속자</span><span class="sxs-lookup"><span data-stu-id="1e3f3-146">NOTES</span></span>

<span data-ttu-id="1e3f3-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="1e3f3-147">ALIASES</span></span>

<span data-ttu-id="1e3f3-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1e3f3-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1e3f3-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e3f3-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1e3f3-151">INPUTOBJECT <IVMWareIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1e3f3-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1e3f3-152">`[AuthorizationName <String>]`: 사설 클라우드의 Express 경로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="1e3f3-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="1e3f3-153">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="1e3f3-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="1e3f3-154">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="1e3f3-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="1e3f3-155">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="1e3f3-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1e3f3-156">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="1e3f3-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="1e3f3-157">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="1e3f3-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="1e3f3-158">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1e3f3-159">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="1e3f3-160">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1e3f3-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1e3f3-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e3f3-161">RELATED LINKS</span></span>

