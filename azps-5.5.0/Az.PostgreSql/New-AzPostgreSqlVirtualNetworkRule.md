---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: f617f853a8e9106ecb2d1268dfbe4e46a22efb45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193116"
---
# <span data-ttu-id="10389-101">New-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="10389-101">New-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="10389-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10389-102">SYNOPSIS</span></span>
<span data-ttu-id="10389-103">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10389-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="10389-104">구문</span><span class="sxs-lookup"><span data-stu-id="10389-104">SYNTAX</span></span>

```
New-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10389-105">설명</span><span class="sxs-lookup"><span data-stu-id="10389-105">DESCRIPTION</span></span>
<span data-ttu-id="10389-106">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10389-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="10389-107">예제</span><span class="sxs-lookup"><span data-stu-id="10389-107">EXAMPLES</span></span>

### <span data-ttu-id="10389-108">예제 1: 새 PostgreSql 서버 Virtual Network 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="10389-108">Example 1: Create a new PostgreSql server Virtual Network Rule</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> New-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="10389-109">이러한 cmdlet은 PostgreSql 서버 Virtual Network 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="10389-109">These cmdlets create a PostgreSql server Virtual Network Rule.</span></span>

## <span data-ttu-id="10389-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10389-110">PARAMETERS</span></span>

### <span data-ttu-id="10389-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10389-111">-AsJob</span></span>
<span data-ttu-id="10389-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="10389-112">Run the command as a job</span></span>

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

### <span data-ttu-id="10389-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10389-113">-DefaultProfile</span></span>
<span data-ttu-id="10389-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10389-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10389-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="10389-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="10389-116">가상 네트워크에 vnet 서비스 엔드포인트를 사용하도록 설정하기 전에 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="10389-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="10389-117">-Name</span><span class="sxs-lookup"><span data-stu-id="10389-117">-Name</span></span>
<span data-ttu-id="10389-118">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10389-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="10389-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="10389-119">-NoWait</span></span>
<span data-ttu-id="10389-120">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="10389-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="10389-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10389-121">-PassThru</span></span>
<span data-ttu-id="10389-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="10389-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="10389-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10389-123">-ResourceGroupName</span></span>
<span data-ttu-id="10389-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10389-124">The name of the resource group.</span></span>
<span data-ttu-id="10389-125">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="10389-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="10389-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="10389-126">-ServerName</span></span>
<span data-ttu-id="10389-127">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10389-127">The name of the server.</span></span>

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

### <span data-ttu-id="10389-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="10389-128">-SubnetId</span></span>
<span data-ttu-id="10389-129">가상 ARM 서브넷의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="10389-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="10389-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10389-130">-SubscriptionId</span></span>
<span data-ttu-id="10389-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="10389-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="10389-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10389-132">-Confirm</span></span>
<span data-ttu-id="10389-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10389-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10389-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10389-134">-WhatIf</span></span>
<span data-ttu-id="10389-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="10389-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10389-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10389-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10389-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10389-137">CommonParameters</span></span>
<span data-ttu-id="10389-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10389-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10389-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10389-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10389-140">입력</span><span class="sxs-lookup"><span data-stu-id="10389-140">INPUTS</span></span>

## <span data-ttu-id="10389-141">출력</span><span class="sxs-lookup"><span data-stu-id="10389-141">OUTPUTS</span></span>

### <span data-ttu-id="10389-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="10389-142">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="10389-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10389-143">NOTES</span></span>

<span data-ttu-id="10389-144">별칭</span><span class="sxs-lookup"><span data-stu-id="10389-144">ALIASES</span></span>

## <span data-ttu-id="10389-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10389-145">RELATED LINKS</span></span>

