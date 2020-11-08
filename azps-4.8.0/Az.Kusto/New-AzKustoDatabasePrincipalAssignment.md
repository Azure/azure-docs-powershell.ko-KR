---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 8bfcb3a96ee8db53a6a869a01441739ee9c503bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211689"
---
# <span data-ttu-id="dfded-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="dfded-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="dfded-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfded-102">SYNOPSIS</span></span>
<span data-ttu-id="dfded-103">클러스터 데이터베이스 principalAssignment에 대 한 Kusto를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="dfded-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfded-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dfded-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dfded-105">DESCRIPTION</span></span>
<span data-ttu-id="dfded-106">클러스터 데이터베이스 principalAssignment에 대 한 Kusto를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="dfded-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dfded-107">EXAMPLES</span></span>

### <span data-ttu-id="dfded-108">예제 1: 클러스터 데이터베이스 위치에 대 한 Kusto 만들기 할당</span><span class="sxs-lookup"><span data-stu-id="dfded-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="dfded-109">위의 명령은 Kusto 클러스터 데이터베이스 principalAssignment을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="dfded-110">변수</span><span class="sxs-lookup"><span data-stu-id="dfded-110">PARAMETERS</span></span>

### <span data-ttu-id="dfded-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfded-111">-AsJob</span></span>
<span data-ttu-id="dfded-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="dfded-112">Run the command as a job</span></span>

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

### <span data-ttu-id="dfded-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dfded-113">-ClusterName</span></span>
<span data-ttu-id="dfded-114">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="dfded-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dfded-115">-DatabaseName</span></span>
<span data-ttu-id="dfded-116">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="dfded-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfded-117">-DefaultProfile</span></span>
<span data-ttu-id="dfded-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfded-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dfded-119">-NoWait</span></span>
<span data-ttu-id="dfded-120">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="dfded-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dfded-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="dfded-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="dfded-122">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="dfded-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="dfded-123">-PrincipalId</span></span>
<span data-ttu-id="dfded-124">데이터베이스 보안 주체에 할당 된 principal ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="dfded-125">사용자 전자 메일, 응용 프로그램 ID 또는 보안 그룹 이름이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="dfded-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="dfded-126">-PrincipalType</span></span>
<span data-ttu-id="dfded-127">Principal 형식.</span><span class="sxs-lookup"><span data-stu-id="dfded-127">Principal type.</span></span>

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

### <span data-ttu-id="dfded-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfded-128">-ResourceGroupName</span></span>
<span data-ttu-id="dfded-129">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="dfded-130">-역할</span><span class="sxs-lookup"><span data-stu-id="dfded-130">-Role</span></span>
<span data-ttu-id="dfded-131">데이터베이스 보안 주체 역할</span><span class="sxs-lookup"><span data-stu-id="dfded-131">Database principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DatabasePrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfded-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfded-132">-SubscriptionId</span></span>
<span data-ttu-id="dfded-133">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dfded-134">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dfded-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="dfded-135">-TenantId</span></span>
<span data-ttu-id="dfded-136">주체의 테 넌 트 id</span><span class="sxs-lookup"><span data-stu-id="dfded-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="dfded-137">-확인</span><span class="sxs-lookup"><span data-stu-id="dfded-137">-Confirm</span></span>
<span data-ttu-id="dfded-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfded-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfded-139">-WhatIf</span></span>
<span data-ttu-id="dfded-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfded-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfded-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfded-142">CommonParameters</span></span>
<span data-ttu-id="dfded-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfded-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfded-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfded-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfded-145">입력</span><span class="sxs-lookup"><span data-stu-id="dfded-145">INPUTS</span></span>

## <span data-ttu-id="dfded-146">출력</span><span class="sxs-lookup"><span data-stu-id="dfded-146">OUTPUTS</span></span>

### <span data-ttu-id="dfded-147">Api20200614. IDatabasePrincipalAssignment의 a에 대 한 대입</span><span class="sxs-lookup"><span data-stu-id="dfded-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="dfded-148">상속자</span><span class="sxs-lookup"><span data-stu-id="dfded-148">NOTES</span></span>

<span data-ttu-id="dfded-149">별칭과</span><span class="sxs-lookup"><span data-stu-id="dfded-149">ALIASES</span></span>

## <span data-ttu-id="dfded-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfded-150">RELATED LINKS</span></span>

