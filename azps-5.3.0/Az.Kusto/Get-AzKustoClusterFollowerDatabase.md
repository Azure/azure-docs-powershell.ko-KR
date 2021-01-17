---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: ecc811e98545816e69f7baa6fc96ea92fbeb43d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490231"
---
# <span data-ttu-id="8d93e-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="8d93e-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="8d93e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d93e-102">SYNOPSIS</span></span>
<span data-ttu-id="8d93e-103">이 클러스터가 소유하고 그 다음에 다른 클러스터가 이어진 데이터베이스 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="8d93e-104">구문</span><span class="sxs-lookup"><span data-stu-id="8d93e-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d93e-105">설명</span><span class="sxs-lookup"><span data-stu-id="8d93e-105">DESCRIPTION</span></span>
<span data-ttu-id="8d93e-106">이 클러스터가 소유하고 그 다음에 다른 클러스터가 이어진 데이터베이스 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="8d93e-107">예제</span><span class="sxs-lookup"><span data-stu-id="8d93e-107">EXAMPLES</span></span>

### <span data-ttu-id="8d93e-108">예제 1: 팔로우하는 모든 데이터베이스 나열</span><span class="sxs-lookup"><span data-stu-id="8d93e-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="8d93e-109">위의 명령은 이 클러스터가 소유하고 그 다음에 다른 클러스터가 이어진 모든 데이터베이스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="8d93e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d93e-110">PARAMETERS</span></span>

### <span data-ttu-id="8d93e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8d93e-111">-ClusterName</span></span>
<span data-ttu-id="8d93e-112">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="8d93e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d93e-113">-DefaultProfile</span></span>
<span data-ttu-id="8d93e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d93e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d93e-115">-ResourceGroupName</span></span>
<span data-ttu-id="8d93e-116">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="8d93e-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d93e-117">-SubscriptionId</span></span>
<span data-ttu-id="8d93e-118">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8d93e-119">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d93e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d93e-120">-Confirm</span></span>
<span data-ttu-id="8d93e-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d93e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d93e-122">-WhatIf</span></span>
<span data-ttu-id="8d93e-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8d93e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d93e-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d93e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d93e-125">CommonParameters</span></span>
<span data-ttu-id="8d93e-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8d93e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d93e-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d93e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d93e-128">입력</span><span class="sxs-lookup"><span data-stu-id="8d93e-128">INPUTS</span></span>

## <span data-ttu-id="8d93e-129">출력</span><span class="sxs-lookup"><span data-stu-id="8d93e-129">OUTPUTS</span></span>

### <span data-ttu-id="8d93e-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="8d93e-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="8d93e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8d93e-131">NOTES</span></span>

<span data-ttu-id="8d93e-132">별칭</span><span class="sxs-lookup"><span data-stu-id="8d93e-132">ALIASES</span></span>

## <span data-ttu-id="8d93e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d93e-133">RELATED LINKS</span></span>

