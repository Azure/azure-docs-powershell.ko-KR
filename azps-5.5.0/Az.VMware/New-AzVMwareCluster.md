---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
ms.openlocfilehash: d654b2fa012a793ce48dff2cc5bfb9ade4f99d34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182545"
---
# <span data-ttu-id="534b5-101">New-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="534b5-101">New-AzVMwareCluster</span></span>

## <span data-ttu-id="534b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="534b5-102">SYNOPSIS</span></span>
<span data-ttu-id="534b5-103">사설 클라우드에서 클러스터 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="534b5-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="534b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="534b5-104">SYNTAX</span></span>

```
New-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -SkuName <String>
 [-SubscriptionId <String>] [-ClusterSize <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="534b5-105">설명</span><span class="sxs-lookup"><span data-stu-id="534b5-105">DESCRIPTION</span></span>
<span data-ttu-id="534b5-106">사설 클라우드에서 클러스터 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="534b5-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="534b5-107">예제</span><span class="sxs-lookup"><span data-stu-id="534b5-107">EXAMPLES</span></span>

### <span data-ttu-id="534b5-108">예제 1: 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="534b5-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="534b5-109">클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="534b5-109">Create cluster</span></span>

## <span data-ttu-id="534b5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="534b5-110">PARAMETERS</span></span>

### <span data-ttu-id="534b5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="534b5-111">-AsJob</span></span>
<span data-ttu-id="534b5-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="534b5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="534b5-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="534b5-113">-ClusterSize</span></span>
<span data-ttu-id="534b5-114">클러스터 크기</span><span class="sxs-lookup"><span data-stu-id="534b5-114">The cluster size</span></span>

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

### <span data-ttu-id="534b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534b5-115">-DefaultProfile</span></span>
<span data-ttu-id="534b5-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="534b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="534b5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="534b5-117">-Name</span></span>
<span data-ttu-id="534b5-118">사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="534b5-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="534b5-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="534b5-119">-NoWait</span></span>
<span data-ttu-id="534b5-120">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="534b5-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="534b5-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="534b5-121">-PrivateCloudName</span></span>
<span data-ttu-id="534b5-122">사설 클라우드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="534b5-122">The name of the private cloud.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="534b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="534b5-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="534b5-124">The name of the resource group.</span></span>
<span data-ttu-id="534b5-125">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="534b5-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="534b5-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="534b5-126">-SkuName</span></span>
<span data-ttu-id="534b5-127">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="534b5-127">The name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="534b5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="534b5-128">-SubscriptionId</span></span>
<span data-ttu-id="534b5-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="534b5-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="534b5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="534b5-130">-Confirm</span></span>
<span data-ttu-id="534b5-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="534b5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="534b5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="534b5-132">-WhatIf</span></span>
<span data-ttu-id="534b5-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="534b5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="534b5-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="534b5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="534b5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534b5-135">CommonParameters</span></span>
<span data-ttu-id="534b5-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="534b5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534b5-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="534b5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534b5-138">입력</span><span class="sxs-lookup"><span data-stu-id="534b5-138">INPUTS</span></span>

## <span data-ttu-id="534b5-139">출력</span><span class="sxs-lookup"><span data-stu-id="534b5-139">OUTPUTS</span></span>

### <span data-ttu-id="534b5-140">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="534b5-140">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="534b5-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="534b5-141">NOTES</span></span>

<span data-ttu-id="534b5-142">별칭</span><span class="sxs-lookup"><span data-stu-id="534b5-142">ALIASES</span></span>

## <span data-ttu-id="534b5-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="534b5-143">RELATED LINKS</span></span>

