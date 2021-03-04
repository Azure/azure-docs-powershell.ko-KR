---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 738f0d4b4033dd7cccdc0fbabe94d2dfde9779c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959547"
---
# <span data-ttu-id="ef7c9-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="ef7c9-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="ef7c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7c9-103">Kusto 클러스터 보안 주체 만들기Assignment.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="ef7c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef7c9-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef7c9-105">설명</span><span class="sxs-lookup"><span data-stu-id="ef7c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7c9-106">Kusto 클러스터 보안 주체 만들기Assignment.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="ef7c9-107">예제</span><span class="sxs-lookup"><span data-stu-id="ef7c9-107">EXAMPLES</span></span>

### <span data-ttu-id="ef7c9-108">예제 1: Kusto 클러스터 주체 만들기Assignment</span><span class="sxs-lookup"><span data-stu-id="ef7c9-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="ef7c9-109">위의 명령은 Kusto 클러스터 주체Assignment를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="ef7c9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ef7c9-110">PARAMETERS</span></span>

### <span data-ttu-id="ef7c9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef7c9-111">-AsJob</span></span>
<span data-ttu-id="ef7c9-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ef7c9-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ef7c9-113">-ClusterName</span></span>
<span data-ttu-id="ef7c9-114">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ef7c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7c9-115">-DefaultProfile</span></span>
<span data-ttu-id="ef7c9-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef7c9-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ef7c9-117">-NoWait</span></span>
<span data-ttu-id="ef7c9-118">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="ef7c9-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ef7c9-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="ef7c9-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="ef7c9-120">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="ef7c9-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="ef7c9-121">-PrincipalId</span></span>
<span data-ttu-id="ef7c9-122">클러스터 주체에 할당된 주체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="ef7c9-123">사용자 전자 메일, 애플리케이션 ID 또는 보안 그룹 이름일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-123">It can be a user email, application ID, or security group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c9-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="ef7c9-124">-PrincipalType</span></span>
<span data-ttu-id="ef7c9-125">주체 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-125">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef7c9-126">-ResourceGroupName</span></span>
<span data-ttu-id="ef7c9-127">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ef7c9-128">-역할</span><span class="sxs-lookup"><span data-stu-id="ef7c9-128">-Role</span></span>
<span data-ttu-id="ef7c9-129">클러스터 주체 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-129">Cluster principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.ClusterPrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef7c9-130">-SubscriptionId</span></span>
<span data-ttu-id="ef7c9-131">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef7c9-132">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ef7c9-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ef7c9-133">-TenantId</span></span>
<span data-ttu-id="ef7c9-134">주체의 테넌트 ID</span><span class="sxs-lookup"><span data-stu-id="ef7c9-134">The tenant id of the principal</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c9-135">-확인</span><span class="sxs-lookup"><span data-stu-id="ef7c9-135">-Confirm</span></span>
<span data-ttu-id="ef7c9-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef7c9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7c9-137">-WhatIf</span></span>
<span data-ttu-id="ef7c9-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef7c9-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef7c9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7c9-140">CommonParameters</span></span>
<span data-ttu-id="ef7c9-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef7c9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7c9-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef7c9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7c9-143">입력</span><span class="sxs-lookup"><span data-stu-id="ef7c9-143">INPUTS</span></span>

## <span data-ttu-id="ef7c9-144">출력</span><span class="sxs-lookup"><span data-stu-id="ef7c9-144">OUTPUTS</span></span>

### <span data-ttu-id="ef7c9-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="ef7c9-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="ef7c9-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef7c9-146">NOTES</span></span>

<span data-ttu-id="ef7c9-147">별칭</span><span class="sxs-lookup"><span data-stu-id="ef7c9-147">ALIASES</span></span>

## <span data-ttu-id="ef7c9-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef7c9-148">RELATED LINKS</span></span>

