---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203813"
---
# <span data-ttu-id="44b8c-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="44b8c-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="44b8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="44b8c-103">기존 가상 네트워크 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="44b8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44b8c-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44b8c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44b8c-105">DESCRIPTION</span></span>
<span data-ttu-id="44b8c-106">기존 가상 네트워크 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="44b8c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="44b8c-107">EXAMPLES</span></span>

### <span data-ttu-id="44b8c-108">예제 1: 새 PostgreSql 서버 가상 네트워크 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="44b8c-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="44b8c-109">이러한 cmdlet은 PostgreSql 서버 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="44b8c-110">변수</span><span class="sxs-lookup"><span data-stu-id="44b8c-110">PARAMETERS</span></span>

### <span data-ttu-id="44b8c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44b8c-111">-AsJob</span></span>
<span data-ttu-id="44b8c-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="44b8c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="44b8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b8c-113">-DefaultProfile</span></span>
<span data-ttu-id="44b8c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44b8c-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="44b8c-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="44b8c-116">가상 네트워크에 vnet 서비스 끝점을 사용 하도록 설정 하기 전에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="44b8c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="44b8c-117">-Name</span></span>
<span data-ttu-id="44b8c-118">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b8c-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="44b8c-119">-NoWait</span></span>
<span data-ttu-id="44b8c-120">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="44b8c-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="44b8c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44b8c-121">-PassThru</span></span>
<span data-ttu-id="44b8c-122">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="44b8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="44b8c-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-124">The name of the resource group.</span></span>
<span data-ttu-id="44b8c-125">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="44b8c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="44b8c-126">-ServerName</span></span>
<span data-ttu-id="44b8c-127">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-127">The name of the server.</span></span>

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

### <span data-ttu-id="44b8c-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="44b8c-128">-SubnetId</span></span>
<span data-ttu-id="44b8c-129">가상 네트워크 서브넷의 ARM 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="44b8c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44b8c-130">-SubscriptionId</span></span>
<span data-ttu-id="44b8c-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="44b8c-132">-확인</span><span class="sxs-lookup"><span data-stu-id="44b8c-132">-Confirm</span></span>
<span data-ttu-id="44b8c-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44b8c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b8c-134">-WhatIf</span></span>
<span data-ttu-id="44b8c-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44b8c-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44b8c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b8c-137">CommonParameters</span></span>
<span data-ttu-id="44b8c-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44b8c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b8c-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="44b8c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b8c-140">입력</span><span class="sxs-lookup"><span data-stu-id="44b8c-140">INPUTS</span></span>

## <span data-ttu-id="44b8c-141">출력</span><span class="sxs-lookup"><span data-stu-id="44b8c-141">OUTPUTS</span></span>

### <span data-ttu-id="44b8c-142">PostgreSql. Api20171201. IVirtualNetworkRule에 대 한</span><span class="sxs-lookup"><span data-stu-id="44b8c-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="44b8c-143">상속자</span><span class="sxs-lookup"><span data-stu-id="44b8c-143">NOTES</span></span>

<span data-ttu-id="44b8c-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="44b8c-144">ALIASES</span></span>

## <span data-ttu-id="44b8c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44b8c-145">RELATED LINKS</span></span>

