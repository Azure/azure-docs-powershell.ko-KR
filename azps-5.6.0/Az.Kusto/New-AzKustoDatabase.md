---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: b3e6319de721d63071c730bb43e1ef7db5a46e25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956128"
---
# <span data-ttu-id="94c6b-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="94c6b-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="94c6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="94c6b-103">데이터베이스를 만들고 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-103">Creates or updates a database.</span></span>

## <span data-ttu-id="94c6b-104">구문</span><span class="sxs-lookup"><span data-stu-id="94c6b-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94c6b-105">설명</span><span class="sxs-lookup"><span data-stu-id="94c6b-105">DESCRIPTION</span></span>
<span data-ttu-id="94c6b-106">데이터베이스를 만들고 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-106">Creates or updates a database.</span></span>

## <span data-ttu-id="94c6b-107">예제</span><span class="sxs-lookup"><span data-stu-id="94c6b-107">EXAMPLES</span></span>

### <span data-ttu-id="94c6b-108">예제 1: 이름으로 새 Kusto 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="94c6b-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="94c6b-109">위의 명령은 리소스 그룹 "testrg"에 있는 기존 클러스터 "testnewkustocluster"에 "mykustodatabase"라는 새 Kusto 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="94c6b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="94c6b-110">PARAMETERS</span></span>

### <span data-ttu-id="94c6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94c6b-111">-AsJob</span></span>
<span data-ttu-id="94c6b-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="94c6b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="94c6b-113">-ClusterName</span></span>
<span data-ttu-id="94c6b-114">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="94c6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c6b-115">-DefaultProfile</span></span>
<span data-ttu-id="94c6b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94c6b-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="94c6b-117">-HotCachePeriod</span></span>
<span data-ttu-id="94c6b-118">TimeSpan에서 빠른 쿼리를 위해 데이터를 캐시에 보관해야 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="94c6b-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="94c6b-119">-Kind</span></span>
<span data-ttu-id="94c6b-120">데이터베이스의 종류</span><span class="sxs-lookup"><span data-stu-id="94c6b-120">Kind of the database</span></span>

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

### <span data-ttu-id="94c6b-121">-Location</span><span class="sxs-lookup"><span data-stu-id="94c6b-121">-Location</span></span>
<span data-ttu-id="94c6b-122">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-122">Resource location.</span></span>

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

### <span data-ttu-id="94c6b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="94c6b-123">-Name</span></span>
<span data-ttu-id="94c6b-124">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-124">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="94c6b-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="94c6b-125">-NoWait</span></span>
<span data-ttu-id="94c6b-126">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="94c6b-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="94c6b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c6b-127">-ResourceGroupName</span></span>
<span data-ttu-id="94c6b-128">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="94c6b-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="94c6b-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="94c6b-130">TimeSpan에서 쿼리에 액세스할 수 없는 것을 중지하기 전에 데이터를 유지해야 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="94c6b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94c6b-131">-SubscriptionId</span></span>
<span data-ttu-id="94c6b-132">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="94c6b-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="94c6b-134">-확인</span><span class="sxs-lookup"><span data-stu-id="94c6b-134">-Confirm</span></span>
<span data-ttu-id="94c6b-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94c6b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94c6b-136">-WhatIf</span></span>
<span data-ttu-id="94c6b-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c6b-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94c6b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c6b-139">CommonParameters</span></span>
<span data-ttu-id="94c6b-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94c6b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c6b-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94c6b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c6b-142">입력</span><span class="sxs-lookup"><span data-stu-id="94c6b-142">INPUTS</span></span>

## <span data-ttu-id="94c6b-143">출력</span><span class="sxs-lookup"><span data-stu-id="94c6b-143">OUTPUTS</span></span>

### <span data-ttu-id="94c6b-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="94c6b-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="94c6b-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94c6b-145">NOTES</span></span>

<span data-ttu-id="94c6b-146">별칭</span><span class="sxs-lookup"><span data-stu-id="94c6b-146">ALIASES</span></span>

## <span data-ttu-id="94c6b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94c6b-147">RELATED LINKS</span></span>

