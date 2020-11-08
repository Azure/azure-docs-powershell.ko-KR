---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: e35e0731fb14cf8ca45b6e56d3957d13ccb88398
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056688"
---
# <span data-ttu-id="c4def-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="c4def-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="c4def-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4def-102">SYNOPSIS</span></span>
<span data-ttu-id="c4def-103">이 클러스터가 소유 하 고 다른 클러스터가 팔 로우 하는 데이터베이스의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="c4def-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4def-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4def-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c4def-105">DESCRIPTION</span></span>
<span data-ttu-id="c4def-106">이 클러스터가 소유 하 고 다른 클러스터가 팔 로우 하는 데이터베이스의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="c4def-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c4def-107">EXAMPLES</span></span>

### <span data-ttu-id="c4def-108">예제 1: 팔 로우 하는 모든 데이터베이스 나열</span><span class="sxs-lookup"><span data-stu-id="c4def-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="c4def-109">위 명령에는이 클러스터에서 소유 하 고 그 다음에 다른 클러스터가 나오는 모든 데이터베이스가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="c4def-110">변수</span><span class="sxs-lookup"><span data-stu-id="c4def-110">PARAMETERS</span></span>

### <span data-ttu-id="c4def-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c4def-111">-ClusterName</span></span>
<span data-ttu-id="c4def-112">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c4def-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4def-113">-DefaultProfile</span></span>
<span data-ttu-id="c4def-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4def-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4def-115">-ResourceGroupName</span></span>
<span data-ttu-id="c4def-116">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c4def-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4def-117">-SubscriptionId</span></span>
<span data-ttu-id="c4def-118">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c4def-119">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c4def-120">-확인</span><span class="sxs-lookup"><span data-stu-id="c4def-120">-Confirm</span></span>
<span data-ttu-id="c4def-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4def-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4def-122">-WhatIf</span></span>
<span data-ttu-id="c4def-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4def-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4def-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4def-125">CommonParameters</span></span>
<span data-ttu-id="c4def-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4def-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4def-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c4def-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4def-128">입력</span><span class="sxs-lookup"><span data-stu-id="c4def-128">INPUTS</span></span>

## <span data-ttu-id="c4def-129">출력</span><span class="sxs-lookup"><span data-stu-id="c4def-129">OUTPUTS</span></span>

### <span data-ttu-id="c4def-130">Api20200614. a PowerShell. i i m. a에 대 한 모든 정의</span><span class="sxs-lookup"><span data-stu-id="c4def-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="c4def-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c4def-131">NOTES</span></span>

<span data-ttu-id="c4def-132">별칭과</span><span class="sxs-lookup"><span data-stu-id="c4def-132">ALIASES</span></span>

## <span data-ttu-id="c4def-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4def-133">RELATED LINKS</span></span>

