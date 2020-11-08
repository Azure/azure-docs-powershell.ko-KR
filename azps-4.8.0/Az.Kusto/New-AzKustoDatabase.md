---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: dc0b4ea1616c916edacaf4d5a4a2b431e7f7d113
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211688"
---
# <span data-ttu-id="39f22-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="39f22-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="39f22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39f22-102">SYNOPSIS</span></span>
<span data-ttu-id="39f22-103">데이터베이스를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-103">Creates or updates a database.</span></span>

## <span data-ttu-id="39f22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39f22-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39f22-105">설명은</span><span class="sxs-lookup"><span data-stu-id="39f22-105">DESCRIPTION</span></span>
<span data-ttu-id="39f22-106">데이터베이스를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-106">Creates or updates a database.</span></span>

## <span data-ttu-id="39f22-107">예제의</span><span class="sxs-lookup"><span data-stu-id="39f22-107">EXAMPLES</span></span>

### <span data-ttu-id="39f22-108">예제 1: 이름으로 새 Kusto 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="39f22-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="39f22-109">위의 명령은 리소스 그룹 "testrg"에 있는 기존 클러스터 "testnewkustocluster"에 "mykustodatabase" 이라는 새 Kusto 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="39f22-110">변수</span><span class="sxs-lookup"><span data-stu-id="39f22-110">PARAMETERS</span></span>

### <span data-ttu-id="39f22-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39f22-111">-AsJob</span></span>
<span data-ttu-id="39f22-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="39f22-112">Run the command as a job</span></span>

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

### <span data-ttu-id="39f22-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="39f22-113">-ClusterName</span></span>
<span data-ttu-id="39f22-114">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="39f22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f22-115">-DefaultProfile</span></span>
<span data-ttu-id="39f22-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39f22-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="39f22-117">-HotCachePeriod</span></span>
<span data-ttu-id="39f22-118">TimeSpan에서 빠른 쿼리를 위해 캐시에 데이터를 유지 해야 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f22-119">-종류</span><span class="sxs-lookup"><span data-stu-id="39f22-119">-Kind</span></span>
<span data-ttu-id="39f22-120">데이터베이스의 종류</span><span class="sxs-lookup"><span data-stu-id="39f22-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f22-121">-위치</span><span class="sxs-lookup"><span data-stu-id="39f22-121">-Location</span></span>
<span data-ttu-id="39f22-122">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-122">Resource location.</span></span>

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

### <span data-ttu-id="39f22-123">-이름</span><span class="sxs-lookup"><span data-stu-id="39f22-123">-Name</span></span>
<span data-ttu-id="39f22-124">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f22-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="39f22-125">-NoWait</span></span>
<span data-ttu-id="39f22-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="39f22-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="39f22-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f22-127">-ResourceGroupName</span></span>
<span data-ttu-id="39f22-128">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="39f22-129">-소프트 Deleteperiod</span><span class="sxs-lookup"><span data-stu-id="39f22-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="39f22-130">TimeSpan의 쿼리에 액세스할 수 있으려면 먼저 데이터를 유지 해야 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f22-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39f22-131">-SubscriptionId</span></span>
<span data-ttu-id="39f22-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="39f22-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="39f22-134">-확인</span><span class="sxs-lookup"><span data-stu-id="39f22-134">-Confirm</span></span>
<span data-ttu-id="39f22-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39f22-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39f22-136">-WhatIf</span></span>
<span data-ttu-id="39f22-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39f22-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39f22-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f22-139">CommonParameters</span></span>
<span data-ttu-id="39f22-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f22-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f22-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="39f22-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f22-142">입력</span><span class="sxs-lookup"><span data-stu-id="39f22-142">INPUTS</span></span>

## <span data-ttu-id="39f22-143">출력</span><span class="sxs-lookup"><span data-stu-id="39f22-143">OUTPUTS</span></span>

### <span data-ttu-id="39f22-144">Microsoft. Api20200614 데이터베이스에 대 한 자세한 모든.</span><span class="sxs-lookup"><span data-stu-id="39f22-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="39f22-145">상속자</span><span class="sxs-lookup"><span data-stu-id="39f22-145">NOTES</span></span>

<span data-ttu-id="39f22-146">별칭과</span><span class="sxs-lookup"><span data-stu-id="39f22-146">ALIASES</span></span>

## <span data-ttu-id="39f22-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39f22-147">RELATED LINKS</span></span>

