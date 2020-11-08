---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056683"
---
# <span data-ttu-id="77cb7-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="77cb7-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="77cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="77cb7-103">지정 된 Kusto 클러스터 및 데이터베이스의 데이터베이스 사용자 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="77cb7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77cb7-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="77cb7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="77cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="77cb7-106">지정 된 Kusto 클러스터 및 데이터베이스의 데이터베이스 사용자 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="77cb7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="77cb7-107">EXAMPLES</span></span>

### <span data-ttu-id="77cb7-108">예제 1: 지정 된 Kusto 클러스터 및 데이터베이스의 데이터베이스 사용자 목록</span><span class="sxs-lookup"><span data-stu-id="77cb7-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="77cb7-109">위의 명령은 지정 된 Kusto에 대 한 데이터베이스 주체의 목록을 클러스터 및 데이터베이스에 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="77cb7-110">변수</span><span class="sxs-lookup"><span data-stu-id="77cb7-110">PARAMETERS</span></span>

### <span data-ttu-id="77cb7-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="77cb7-111">-ClusterName</span></span>
<span data-ttu-id="77cb7-112">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="77cb7-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="77cb7-113">-DatabaseName</span></span>
<span data-ttu-id="77cb7-114">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="77cb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77cb7-115">-DefaultProfile</span></span>
<span data-ttu-id="77cb7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77cb7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77cb7-117">-ResourceGroupName</span></span>
<span data-ttu-id="77cb7-118">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="77cb7-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77cb7-119">-SubscriptionId</span></span>
<span data-ttu-id="77cb7-120">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="77cb7-121">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="77cb7-122">-확인</span><span class="sxs-lookup"><span data-stu-id="77cb7-122">-Confirm</span></span>
<span data-ttu-id="77cb7-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77cb7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77cb7-124">-WhatIf</span></span>
<span data-ttu-id="77cb7-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77cb7-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77cb7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77cb7-127">CommonParameters</span></span>
<span data-ttu-id="77cb7-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77cb7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77cb7-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77cb7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77cb7-130">입력</span><span class="sxs-lookup"><span data-stu-id="77cb7-130">INPUTS</span></span>

## <span data-ttu-id="77cb7-131">출력</span><span class="sxs-lookup"><span data-stu-id="77cb7-131">OUTPUTS</span></span>

### <span data-ttu-id="77cb7-132">Api20200614. i a PowerShell. IDatabasePrincipal.</span><span class="sxs-lookup"><span data-stu-id="77cb7-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="77cb7-133">상속자</span><span class="sxs-lookup"><span data-stu-id="77cb7-133">NOTES</span></span>

<span data-ttu-id="77cb7-134">별칭과</span><span class="sxs-lookup"><span data-stu-id="77cb7-134">ALIASES</span></span>

## <span data-ttu-id="77cb7-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77cb7-135">RELATED LINKS</span></span>

