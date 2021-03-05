---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b540b82ed07e42a6789a2603299508c21c7c3aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983483"
---
# <span data-ttu-id="0a832-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a832-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="0a832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a832-102">SYNOPSIS</span></span>
<span data-ttu-id="0a832-103">연결된 데이터베이스 구성을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="0a832-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a832-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0a832-105">설명</span><span class="sxs-lookup"><span data-stu-id="0a832-105">DESCRIPTION</span></span>
<span data-ttu-id="0a832-106">연결된 데이터베이스 구성을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="0a832-107">예제</span><span class="sxs-lookup"><span data-stu-id="0a832-107">EXAMPLES</span></span>

### <span data-ttu-id="0a832-108">예제 1: 새 AttachedDatabaseConfiguration 만들기</span><span class="sxs-lookup"><span data-stu-id="0a832-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="0a832-109">위의 명령은 클러스터 "testnewkustoclusterf"에 ReadOnly 데이터베이스 "mykustodatabase"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="0a832-110">클러스터 "testnewkustocluster"에서 데이터베이스 "mykustodatabase"를 따르고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="0a832-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0a832-111">PARAMETERS</span></span>

### <span data-ttu-id="0a832-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a832-112">-AsJob</span></span>
<span data-ttu-id="0a832-113">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-113">Run the command as a job</span></span>

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

### <span data-ttu-id="0a832-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0a832-114">-ClusterName</span></span>
<span data-ttu-id="0a832-115">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0a832-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="0a832-116">-ClusterResourceId</span></span>
<span data-ttu-id="0a832-117">연결할 데이터베이스가 있는 클러스터의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="0a832-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a832-118">-DatabaseName</span></span>
<span data-ttu-id="0a832-119">연결하려는 데이터베이스의 이름은 모든 현재 및 향후 데이터베이스를 따르고자 하는 경우 \* 를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="0a832-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="0a832-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="0a832-121">기본 주체 수정 종류</span><span class="sxs-lookup"><span data-stu-id="0a832-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a832-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a832-122">-DefaultProfile</span></span>
<span data-ttu-id="0a832-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a832-124">-Location</span><span class="sxs-lookup"><span data-stu-id="0a832-124">-Location</span></span>
<span data-ttu-id="0a832-125">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-125">Resource location.</span></span>

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

### <span data-ttu-id="0a832-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0a832-126">-Name</span></span>
<span data-ttu-id="0a832-127">연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a832-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0a832-128">-NoWait</span></span>
<span data-ttu-id="0a832-129">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="0a832-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0a832-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a832-130">-ResourceGroupName</span></span>
<span data-ttu-id="0a832-131">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0a832-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a832-132">-SubscriptionId</span></span>
<span data-ttu-id="0a832-133">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0a832-134">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0a832-135">-확인</span><span class="sxs-lookup"><span data-stu-id="0a832-135">-Confirm</span></span>
<span data-ttu-id="0a832-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a832-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a832-137">-WhatIf</span></span>
<span data-ttu-id="0a832-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a832-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a832-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a832-140">CommonParameters</span></span>
<span data-ttu-id="0a832-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a832-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a832-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a832-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a832-143">입력</span><span class="sxs-lookup"><span data-stu-id="0a832-143">INPUTS</span></span>

## <span data-ttu-id="0a832-144">출력</span><span class="sxs-lookup"><span data-stu-id="0a832-144">OUTPUTS</span></span>

### <span data-ttu-id="0a832-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a832-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="0a832-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a832-146">NOTES</span></span>

<span data-ttu-id="0a832-147">별칭</span><span class="sxs-lookup"><span data-stu-id="0a832-147">ALIASES</span></span>

## <span data-ttu-id="0a832-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a832-148">RELATED LINKS</span></span>

