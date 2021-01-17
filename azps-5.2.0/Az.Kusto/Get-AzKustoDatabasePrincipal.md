---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349293"
---
# <span data-ttu-id="6bf54-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="6bf54-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="6bf54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bf54-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf54-103">주어진 Kusto 클러스터 및 데이터베이스의 데이터베이스 주체 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="6bf54-104">구문</span><span class="sxs-lookup"><span data-stu-id="6bf54-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6bf54-105">설명</span><span class="sxs-lookup"><span data-stu-id="6bf54-105">DESCRIPTION</span></span>
<span data-ttu-id="6bf54-106">주어진 Kusto 클러스터 및 데이터베이스의 데이터베이스 주체 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="6bf54-107">예제</span><span class="sxs-lookup"><span data-stu-id="6bf54-107">EXAMPLES</span></span>

### <span data-ttu-id="6bf54-108">예제 1: 주어진 Kusto 클러스터 및 데이터베이스의 데이터베이스 주체 목록</span><span class="sxs-lookup"><span data-stu-id="6bf54-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="6bf54-109">위의 명령은 주어진 Kusto 클러스터 및 데이터베이스의 데이터베이스 주체 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="6bf54-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bf54-110">PARAMETERS</span></span>

### <span data-ttu-id="6bf54-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6bf54-111">-ClusterName</span></span>
<span data-ttu-id="6bf54-112">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="6bf54-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6bf54-113">-DatabaseName</span></span>
<span data-ttu-id="6bf54-114">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="6bf54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf54-115">-DefaultProfile</span></span>
<span data-ttu-id="6bf54-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bf54-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bf54-117">-ResourceGroupName</span></span>
<span data-ttu-id="6bf54-118">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="6bf54-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6bf54-119">-SubscriptionId</span></span>
<span data-ttu-id="6bf54-120">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6bf54-121">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6bf54-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bf54-122">-Confirm</span></span>
<span data-ttu-id="6bf54-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bf54-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bf54-124">-WhatIf</span></span>
<span data-ttu-id="6bf54-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6bf54-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bf54-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bf54-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf54-127">CommonParameters</span></span>
<span data-ttu-id="6bf54-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6bf54-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf54-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6bf54-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf54-130">입력</span><span class="sxs-lookup"><span data-stu-id="6bf54-130">INPUTS</span></span>

## <span data-ttu-id="6bf54-131">출력</span><span class="sxs-lookup"><span data-stu-id="6bf54-131">OUTPUTS</span></span>

### <span data-ttu-id="6bf54-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="6bf54-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="6bf54-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6bf54-133">NOTES</span></span>

<span data-ttu-id="6bf54-134">별칭</span><span class="sxs-lookup"><span data-stu-id="6bf54-134">ALIASES</span></span>

## <span data-ttu-id="6bf54-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bf54-135">RELATED LINKS</span></span>

