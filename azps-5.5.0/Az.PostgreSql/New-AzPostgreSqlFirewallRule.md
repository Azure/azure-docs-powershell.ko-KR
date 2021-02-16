---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179137"
---
# <span data-ttu-id="bcdcc-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bcdcc-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="bcdcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcdcc-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdcc-103">새 방화벽 규칙을 생성하거나 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="bcdcc-104">구문</span><span class="sxs-lookup"><span data-stu-id="bcdcc-104">SYNTAX</span></span>

### <span data-ttu-id="bcdcc-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="bcdcc-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bcdcc-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="bcdcc-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bcdcc-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="bcdcc-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bcdcc-108">설명</span><span class="sxs-lookup"><span data-stu-id="bcdcc-108">DESCRIPTION</span></span>
<span data-ttu-id="bcdcc-109">새 방화벽 규칙을 생성하거나 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="bcdcc-110">예제</span><span class="sxs-lookup"><span data-stu-id="bcdcc-110">EXAMPLES</span></span>

### <span data-ttu-id="bcdcc-111">예제 1: 새 PostgreSql 서버 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="bcdcc-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="bcdcc-112">이 cmdlet은 PostgreSql 서버 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="bcdcc-113">예제 2: -ClientIPAddress를 사용하여 새 PostgreSql 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="bcdcc-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="bcdcc-114">이 cmdlet은 -ClientIPAddress를 사용하여 PostgreSql 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="bcdcc-115">예제 3: 모든 IP를 허용하는 새 PostgreSql 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="bcdcc-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="bcdcc-116">이 cmdlet은 모든 IPS를 허용하는 새 PostgreSql 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="bcdcc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcdcc-117">PARAMETERS</span></span>

### <span data-ttu-id="bcdcc-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="bcdcc-118">-AllowAll</span></span>
<span data-ttu-id="bcdcc-119">0.0.0.0에서 255.255.255.255.255까지 모든 범위의 IPS를 허용하도록 제시합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdcc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcdcc-120">-AsJob</span></span>
<span data-ttu-id="bcdcc-121">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="bcdcc-121">Run the command as a job</span></span>

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

### <span data-ttu-id="bcdcc-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="bcdcc-122">-ClientIPAddress</span></span>
<span data-ttu-id="bcdcc-123">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="bcdcc-124">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdcc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdcc-125">-DefaultProfile</span></span>
<span data-ttu-id="bcdcc-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcdcc-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="bcdcc-127">-EndIPAddress</span></span>
<span data-ttu-id="bcdcc-128">서버 방화벽 규칙의 최종 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="bcdcc-129">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdcc-130">-Name</span><span class="sxs-lookup"><span data-stu-id="bcdcc-130">-Name</span></span>
<span data-ttu-id="bcdcc-131">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-131">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdcc-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bcdcc-132">-NoWait</span></span>
<span data-ttu-id="bcdcc-133">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="bcdcc-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bcdcc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcdcc-134">-ResourceGroupName</span></span>
<span data-ttu-id="bcdcc-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-135">The name of the resource group.</span></span>
<span data-ttu-id="bcdcc-136">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bcdcc-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bcdcc-137">-ServerName</span></span>
<span data-ttu-id="bcdcc-138">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-138">The name of the server.</span></span>

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

### <span data-ttu-id="bcdcc-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="bcdcc-139">-StartIPAddress</span></span>
<span data-ttu-id="bcdcc-140">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="bcdcc-141">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-141">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdcc-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bcdcc-142">-SubscriptionId</span></span>
<span data-ttu-id="bcdcc-143">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bcdcc-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcdcc-144">-Confirm</span></span>
<span data-ttu-id="bcdcc-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcdcc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcdcc-146">-WhatIf</span></span>
<span data-ttu-id="bcdcc-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bcdcc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcdcc-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcdcc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdcc-149">CommonParameters</span></span>
<span data-ttu-id="bcdcc-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdcc-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bcdcc-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdcc-152">입력</span><span class="sxs-lookup"><span data-stu-id="bcdcc-152">INPUTS</span></span>

## <span data-ttu-id="bcdcc-153">출력</span><span class="sxs-lookup"><span data-stu-id="bcdcc-153">OUTPUTS</span></span>

### <span data-ttu-id="bcdcc-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bcdcc-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="bcdcc-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bcdcc-155">NOTES</span></span>

<span data-ttu-id="bcdcc-156">별칭</span><span class="sxs-lookup"><span data-stu-id="bcdcc-156">ALIASES</span></span>

## <span data-ttu-id="bcdcc-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcdcc-157">RELATED LINKS</span></span>

