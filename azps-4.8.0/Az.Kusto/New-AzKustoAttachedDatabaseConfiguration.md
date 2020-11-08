---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 26da7e8b0bf3ca24edd9f4abd52f0c27aabf49e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213550"
---
# <span data-ttu-id="738c3-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="738c3-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="738c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="738c3-102">SYNOPSIS</span></span>
<span data-ttu-id="738c3-103">연결 된 데이터베이스 구성을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="738c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="738c3-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="738c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="738c3-105">DESCRIPTION</span></span>
<span data-ttu-id="738c3-106">연결 된 데이터베이스 구성을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="738c3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="738c3-107">EXAMPLES</span></span>

### <span data-ttu-id="738c3-108">예제 1: 새 AttachedDatabaseConfiguration 만들기</span><span class="sxs-lookup"><span data-stu-id="738c3-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="738c3-109">위의 명령은 "testnewkustoclusterf" 클러스터에서 읽기 전용 데이터베이스 "mykustodatabase"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="738c3-110">"Testnewkustocluster" 클러스터의 "mykustodatabase" 데이터베이스를 따릅니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="738c3-111">변수</span><span class="sxs-lookup"><span data-stu-id="738c3-111">PARAMETERS</span></span>

### <span data-ttu-id="738c3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="738c3-112">-AsJob</span></span>
<span data-ttu-id="738c3-113">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="738c3-113">Run the command as a job</span></span>

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

### <span data-ttu-id="738c3-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="738c3-114">-ClusterName</span></span>
<span data-ttu-id="738c3-115">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="738c3-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="738c3-116">-ClusterResourceId</span></span>
<span data-ttu-id="738c3-117">연결할 데이터베이스가 있는 클러스터의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="738c3-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="738c3-118">-DatabaseName</span></span>
<span data-ttu-id="738c3-119">첨부할 데이터베이스의 이름입니다. 현재와 미래의 모든 데이터베이스를 팔 로우 하려면 \*를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="738c3-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="738c3-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="738c3-121">기본 보안 주체 수정 종류</span><span class="sxs-lookup"><span data-stu-id="738c3-121">The default principals modification kind</span></span>

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

### <span data-ttu-id="738c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="738c3-122">-DefaultProfile</span></span>
<span data-ttu-id="738c3-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="738c3-124">-위치</span><span class="sxs-lookup"><span data-stu-id="738c3-124">-Location</span></span>
<span data-ttu-id="738c3-125">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-125">Resource location.</span></span>

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

### <span data-ttu-id="738c3-126">-이름</span><span class="sxs-lookup"><span data-stu-id="738c3-126">-Name</span></span>
<span data-ttu-id="738c3-127">연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-127">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="738c3-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="738c3-128">-NoWait</span></span>
<span data-ttu-id="738c3-129">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="738c3-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="738c3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="738c3-130">-ResourceGroupName</span></span>
<span data-ttu-id="738c3-131">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="738c3-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="738c3-132">-SubscriptionId</span></span>
<span data-ttu-id="738c3-133">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="738c3-134">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="738c3-135">-확인</span><span class="sxs-lookup"><span data-stu-id="738c3-135">-Confirm</span></span>
<span data-ttu-id="738c3-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="738c3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="738c3-137">-WhatIf</span></span>
<span data-ttu-id="738c3-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="738c3-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="738c3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="738c3-140">CommonParameters</span></span>
<span data-ttu-id="738c3-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="738c3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="738c3-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="738c3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="738c3-143">입력</span><span class="sxs-lookup"><span data-stu-id="738c3-143">INPUTS</span></span>

## <span data-ttu-id="738c3-144">출력</span><span class="sxs-lookup"><span data-stu-id="738c3-144">OUTPUTS</span></span>

### <span data-ttu-id="738c3-145">Microsoft. Api20200614. IAttachedDatabaseConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="738c3-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="738c3-146">상속자</span><span class="sxs-lookup"><span data-stu-id="738c3-146">NOTES</span></span>

<span data-ttu-id="738c3-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="738c3-147">ALIASES</span></span>

## <span data-ttu-id="738c3-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="738c3-148">RELATED LINKS</span></span>

