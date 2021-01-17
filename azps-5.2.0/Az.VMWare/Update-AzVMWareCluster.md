---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWareCluster.md
ms.openlocfilehash: b8e1f819c01edac24ff23c629de130036442c9e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326619"
---
# <span data-ttu-id="88f6e-101">Update-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="88f6e-101">Update-AzVMWareCluster</span></span>

## <span data-ttu-id="88f6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="88f6e-103">사설 클라우드에서 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="88f6e-103">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="88f6e-104">구문</span><span class="sxs-lookup"><span data-stu-id="88f6e-104">SYNTAX</span></span>

### <span data-ttu-id="88f6e-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="88f6e-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="88f6e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="88f6e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWareCluster -InputObject <IVMWareIdentity> [-ClusterSize <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88f6e-107">설명</span><span class="sxs-lookup"><span data-stu-id="88f6e-107">DESCRIPTION</span></span>
<span data-ttu-id="88f6e-108">사설 클라우드에서 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="88f6e-108">Update a cluster in a private cloud</span></span>

## <span data-ttu-id="88f6e-109">예제</span><span class="sxs-lookup"><span data-stu-id="88f6e-109">EXAMPLES</span></span>

### <span data-ttu-id="88f6e-110">예제 1: 이름에 따라 클러스터 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="88f6e-110">Example 1: Update cluster size by name</span></span>
```powershell
PS C:\> Update-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="88f6e-111">이름에 따라 클러스터 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="88f6e-111">Update cluster size by name</span></span>

### <span data-ttu-id="88f6e-112">예제 2: 입력 개체로 클러스터 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="88f6e-112">Example 2: Update cluster size by input object</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group | Update-AzVMWareCluster -ClusterSize 4

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="88f6e-113">입력 개체로 클러스터 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="88f6e-113">Update cluster size by input object</span></span>

## <span data-ttu-id="88f6e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88f6e-114">PARAMETERS</span></span>

### <span data-ttu-id="88f6e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88f6e-115">-AsJob</span></span>
<span data-ttu-id="88f6e-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="88f6e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="88f6e-117">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="88f6e-117">-ClusterSize</span></span>
<span data-ttu-id="88f6e-118">클러스터 크기</span><span class="sxs-lookup"><span data-stu-id="88f6e-118">The cluster size</span></span>

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

### <span data-ttu-id="88f6e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f6e-119">-DefaultProfile</span></span>
<span data-ttu-id="88f6e-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88f6e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88f6e-121">-InputObject</span></span>
<span data-ttu-id="88f6e-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="88f6e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="88f6e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="88f6e-123">-Name</span></span>
<span data-ttu-id="88f6e-124">사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="88f6e-124">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="88f6e-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="88f6e-125">-NoWait</span></span>
<span data-ttu-id="88f6e-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="88f6e-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="88f6e-127">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="88f6e-127">-PrivateCloudName</span></span>
<span data-ttu-id="88f6e-128">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="88f6e-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="88f6e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88f6e-129">-ResourceGroupName</span></span>
<span data-ttu-id="88f6e-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-130">The name of the resource group.</span></span>
<span data-ttu-id="88f6e-131">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="88f6e-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88f6e-132">-SubscriptionId</span></span>
<span data-ttu-id="88f6e-133">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="88f6e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88f6e-134">-Confirm</span></span>
<span data-ttu-id="88f6e-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88f6e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88f6e-136">-WhatIf</span></span>
<span data-ttu-id="88f6e-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="88f6e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88f6e-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88f6e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f6e-139">CommonParameters</span></span>
<span data-ttu-id="88f6e-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f6e-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88f6e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f6e-142">입력</span><span class="sxs-lookup"><span data-stu-id="88f6e-142">INPUTS</span></span>

### <span data-ttu-id="88f6e-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="88f6e-143">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="88f6e-144">출력</span><span class="sxs-lookup"><span data-stu-id="88f6e-144">OUTPUTS</span></span>

### <span data-ttu-id="88f6e-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="88f6e-145">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="88f6e-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88f6e-146">NOTES</span></span>

<span data-ttu-id="88f6e-147">별칭</span><span class="sxs-lookup"><span data-stu-id="88f6e-147">ALIASES</span></span>

<span data-ttu-id="88f6e-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="88f6e-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88f6e-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88f6e-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88f6e-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88f6e-151">INPUTOBJECT: <IVMWareIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="88f6e-151">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88f6e-152">`[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름</span><span class="sxs-lookup"><span data-stu-id="88f6e-152">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="88f6e-153">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="88f6e-153">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="88f6e-154">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="88f6e-154">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="88f6e-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="88f6e-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88f6e-156">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="88f6e-156">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="88f6e-157">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="88f6e-157">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="88f6e-158">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="88f6e-159">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="88f6e-160">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="88f6e-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="88f6e-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88f6e-161">RELATED LINKS</span></span>

