---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareCluster.md
ms.openlocfilehash: 2433ffa7c1a016af4d3268162587d6b901b30ae9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987163"
---
# <span data-ttu-id="8b3e0-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="8b3e0-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="8b3e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b3e0-102">SYNOPSIS</span></span>
<span data-ttu-id="8b3e0-103">사설 클라우드에서 클러스터 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="8b3e0-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="8b3e0-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b3e0-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b3e0-105">설명</span><span class="sxs-lookup"><span data-stu-id="8b3e0-105">DESCRIPTION</span></span>
<span data-ttu-id="8b3e0-106">사설 클라우드에서 클러스터 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="8b3e0-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="8b3e0-107">예제</span><span class="sxs-lookup"><span data-stu-id="8b3e0-107">EXAMPLES</span></span>

### <span data-ttu-id="8b3e0-108">예제 1: 클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="8b3e0-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="8b3e0-109">클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="8b3e0-109">Create cluster</span></span>

## <span data-ttu-id="8b3e0-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8b3e0-110">PARAMETERS</span></span>

### <span data-ttu-id="8b3e0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b3e0-111">-AsJob</span></span>
<span data-ttu-id="8b3e0-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8b3e0-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="8b3e0-113">-ClusterSize</span></span>
<span data-ttu-id="8b3e0-114">클러스터 크기</span><span class="sxs-lookup"><span data-stu-id="8b3e0-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b3e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b3e0-115">-DefaultProfile</span></span>
<span data-ttu-id="8b3e0-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b3e0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8b3e0-117">-Name</span></span>
<span data-ttu-id="8b3e0-118">사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="8b3e0-118">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="8b3e0-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8b3e0-119">-NoWait</span></span>
<span data-ttu-id="8b3e0-120">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="8b3e0-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8b3e0-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="8b3e0-121">-PrivateCloudName</span></span>
<span data-ttu-id="8b3e0-122">사설 클라우드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="8b3e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b3e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b3e0-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-124">The name of the resource group.</span></span>
<span data-ttu-id="8b3e0-125">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8b3e0-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8b3e0-126">-SkuName</span></span>
<span data-ttu-id="8b3e0-127">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="8b3e0-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b3e0-128">-SubscriptionId</span></span>
<span data-ttu-id="8b3e0-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8b3e0-130">-확인</span><span class="sxs-lookup"><span data-stu-id="8b3e0-130">-Confirm</span></span>
<span data-ttu-id="8b3e0-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b3e0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b3e0-132">-WhatIf</span></span>
<span data-ttu-id="8b3e0-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b3e0-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b3e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b3e0-135">CommonParameters</span></span>
<span data-ttu-id="8b3e0-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b3e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b3e0-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b3e0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b3e0-138">입력</span><span class="sxs-lookup"><span data-stu-id="8b3e0-138">INPUTS</span></span>

## <span data-ttu-id="8b3e0-139">출력</span><span class="sxs-lookup"><span data-stu-id="8b3e0-139">OUTPUTS</span></span>

### <span data-ttu-id="8b3e0-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="8b3e0-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="8b3e0-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b3e0-141">NOTES</span></span>

<span data-ttu-id="8b3e0-142">별칭</span><span class="sxs-lookup"><span data-stu-id="8b3e0-142">ALIASES</span></span>

## <span data-ttu-id="8b3e0-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b3e0-143">RELATED LINKS</span></span>

