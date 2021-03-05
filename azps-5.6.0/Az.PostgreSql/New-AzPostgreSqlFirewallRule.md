---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 7ba5a72d161f07ae55669ddfa9d0e399d7cf81ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003264"
---
# <span data-ttu-id="e0adc-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e0adc-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="e0adc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0adc-102">SYNOPSIS</span></span>
<span data-ttu-id="e0adc-103">새 방화벽 규칙을 만들고 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="e0adc-104">구문</span><span class="sxs-lookup"><span data-stu-id="e0adc-104">SYNTAX</span></span>

### <span data-ttu-id="e0adc-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="e0adc-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0adc-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="e0adc-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e0adc-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="e0adc-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0adc-108">설명</span><span class="sxs-lookup"><span data-stu-id="e0adc-108">DESCRIPTION</span></span>
<span data-ttu-id="e0adc-109">새 방화벽 규칙을 만들고 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="e0adc-110">예제</span><span class="sxs-lookup"><span data-stu-id="e0adc-110">EXAMPLES</span></span>

### <span data-ttu-id="e0adc-111">예제 1: 새 PostgreSql 서버 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="e0adc-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="e0adc-112">이 cmdlet은 PostgreSql 서버 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="e0adc-113">예제 2: -ClientIPAddress를 사용하여 새 PostgreSql 방화벽 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="e0adc-114">이 cmdlet은 -ClientIPAddress를 사용하여 PostgreSql 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="e0adc-115">예제 3: 모든 IPS를 허용하는 새 PostgreSql 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="e0adc-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="e0adc-116">이 cmdlet은 모든 IPS를 허용하는 새 PostgreSql 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="e0adc-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e0adc-117">PARAMETERS</span></span>

### <span data-ttu-id="e0adc-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="e0adc-118">-AllowAll</span></span>
<span data-ttu-id="e0adc-119">0.0.0.0.0에서 255.255.255.255까지 모든 범위의 IPS를 허용하도록 제시합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="e0adc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0adc-120">-AsJob</span></span>
<span data-ttu-id="e0adc-121">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-121">Run the command as a job</span></span>

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

### <span data-ttu-id="e0adc-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="e0adc-122">-ClientIPAddress</span></span>
<span data-ttu-id="e0adc-123">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="e0adc-124">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e0adc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0adc-125">-DefaultProfile</span></span>
<span data-ttu-id="e0adc-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0adc-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="e0adc-127">-EndIPAddress</span></span>
<span data-ttu-id="e0adc-128">서버 방화벽 규칙의 최종 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="e0adc-129">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e0adc-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e0adc-130">-Name</span></span>
<span data-ttu-id="e0adc-131">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="e0adc-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e0adc-132">-NoWait</span></span>
<span data-ttu-id="e0adc-133">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="e0adc-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e0adc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0adc-134">-ResourceGroupName</span></span>
<span data-ttu-id="e0adc-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-135">The name of the resource group.</span></span>
<span data-ttu-id="e0adc-136">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e0adc-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e0adc-137">-ServerName</span></span>
<span data-ttu-id="e0adc-138">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-138">The name of the server.</span></span>

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

### <span data-ttu-id="e0adc-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="e0adc-139">-StartIPAddress</span></span>
<span data-ttu-id="e0adc-140">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="e0adc-141">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e0adc-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0adc-142">-SubscriptionId</span></span>
<span data-ttu-id="e0adc-143">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e0adc-144">-확인</span><span class="sxs-lookup"><span data-stu-id="e0adc-144">-Confirm</span></span>
<span data-ttu-id="e0adc-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0adc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0adc-146">-WhatIf</span></span>
<span data-ttu-id="e0adc-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0adc-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0adc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0adc-149">CommonParameters</span></span>
<span data-ttu-id="e0adc-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e0adc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0adc-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0adc-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0adc-152">입력</span><span class="sxs-lookup"><span data-stu-id="e0adc-152">INPUTS</span></span>

## <span data-ttu-id="e0adc-153">출력</span><span class="sxs-lookup"><span data-stu-id="e0adc-153">OUTPUTS</span></span>

### <span data-ttu-id="e0adc-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e0adc-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="e0adc-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e0adc-155">NOTES</span></span>

<span data-ttu-id="e0adc-156">별칭</span><span class="sxs-lookup"><span data-stu-id="e0adc-156">ALIASES</span></span>

## <span data-ttu-id="e0adc-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0adc-157">RELATED LINKS</span></span>

