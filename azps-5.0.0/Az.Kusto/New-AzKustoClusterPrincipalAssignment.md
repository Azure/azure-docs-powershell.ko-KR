---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218997"
---
# <span data-ttu-id="cd29c-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="cd29c-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="cd29c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd29c-102">SYNOPSIS</span></span>
<span data-ttu-id="cd29c-103">클러스터 principalAssignment에 대 한 Kusto를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="cd29c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd29c-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd29c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cd29c-105">DESCRIPTION</span></span>
<span data-ttu-id="cd29c-106">클러스터 principalAssignment에 대 한 Kusto를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="cd29c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cd29c-107">EXAMPLES</span></span>

### <span data-ttu-id="cd29c-108">예제 1: 클러스터 principalAssignment에 대 한 Kusto 할당</span><span class="sxs-lookup"><span data-stu-id="cd29c-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="cd29c-109">위 명령에 대 한 클러스터 principalAssignment에 대 한 Kusto 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="cd29c-110">변수</span><span class="sxs-lookup"><span data-stu-id="cd29c-110">PARAMETERS</span></span>

### <span data-ttu-id="cd29c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd29c-111">-AsJob</span></span>
<span data-ttu-id="cd29c-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="cd29c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="cd29c-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cd29c-113">-ClusterName</span></span>
<span data-ttu-id="cd29c-114">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cd29c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd29c-115">-DefaultProfile</span></span>
<span data-ttu-id="cd29c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd29c-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cd29c-117">-NoWait</span></span>
<span data-ttu-id="cd29c-118">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="cd29c-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd29c-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="cd29c-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="cd29c-120">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="cd29c-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="cd29c-121">-PrincipalId</span></span>
<span data-ttu-id="cd29c-122">클러스터 사용자에 게 할당 된 주 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="cd29c-123">사용자 전자 메일, 응용 프로그램 ID 또는 보안 그룹 이름이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="cd29c-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="cd29c-124">-PrincipalType</span></span>
<span data-ttu-id="cd29c-125">Principal 형식.</span><span class="sxs-lookup"><span data-stu-id="cd29c-125">Principal type.</span></span>

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

### <span data-ttu-id="cd29c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd29c-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd29c-127">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cd29c-128">-역할</span><span class="sxs-lookup"><span data-stu-id="cd29c-128">-Role</span></span>
<span data-ttu-id="cd29c-129">클러스터 사용자 역할.</span><span class="sxs-lookup"><span data-stu-id="cd29c-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="cd29c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd29c-130">-SubscriptionId</span></span>
<span data-ttu-id="cd29c-131">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd29c-132">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cd29c-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="cd29c-133">-TenantId</span></span>
<span data-ttu-id="cd29c-134">주체의 테 넌 트 id</span><span class="sxs-lookup"><span data-stu-id="cd29c-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="cd29c-135">-확인</span><span class="sxs-lookup"><span data-stu-id="cd29c-135">-Confirm</span></span>
<span data-ttu-id="cd29c-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd29c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd29c-137">-WhatIf</span></span>
<span data-ttu-id="cd29c-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd29c-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd29c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd29c-140">CommonParameters</span></span>
<span data-ttu-id="cd29c-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd29c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd29c-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd29c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd29c-143">입력</span><span class="sxs-lookup"><span data-stu-id="cd29c-143">INPUTS</span></span>

## <span data-ttu-id="cd29c-144">출력</span><span class="sxs-lookup"><span data-stu-id="cd29c-144">OUTPUTS</span></span>

### <span data-ttu-id="cd29c-145">Microsoft. Api20200614. IClusterPrincipalAssignment에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cd29c-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="cd29c-146">상속자</span><span class="sxs-lookup"><span data-stu-id="cd29c-146">NOTES</span></span>

<span data-ttu-id="cd29c-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="cd29c-147">ALIASES</span></span>

## <span data-ttu-id="cd29c-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd29c-148">RELATED LINKS</span></span>

