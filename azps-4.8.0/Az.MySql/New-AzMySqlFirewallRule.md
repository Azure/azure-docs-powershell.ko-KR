---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFirewallRule.md
ms.openlocfilehash: 036628943afc8b2c5f07b30f2db14f27229364c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211783"
---
# <span data-ttu-id="2763e-101">New-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2763e-101">New-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="2763e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2763e-102">SYNOPSIS</span></span>
<span data-ttu-id="2763e-103">새 방화벽 규칙을 만들거나 기존 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="2763e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2763e-104">SYNTAX</span></span>

### <span data-ttu-id="2763e-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="2763e-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2763e-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="2763e-106">AllowAll</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2763e-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="2763e-107">ClientIPAddress</span></span>
```
New-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2763e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2763e-108">DESCRIPTION</span></span>
<span data-ttu-id="2763e-109">새 방화벽 규칙을 만들거나 기존 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="2763e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2763e-110">EXAMPLES</span></span>

### <span data-ttu-id="2763e-111">예제 1: 새 MySql 서버 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="2763e-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="2763e-112">이 cmdlet은 MySql 서버 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="2763e-113">예제 2:-ClientIPAddress를 사용 하 여 새 MySql 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="2763e-114">이 cmdlet은-ClientIPAddress를 사용 하 여 MySql 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="2763e-115">예제 3: 모든 Ip를 허용 하는 새 MySql 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="2763e-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="2763e-116">이 cmdlet은 모든 Ip를 허용 하는 새 MySql 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="2763e-117">변수</span><span class="sxs-lookup"><span data-stu-id="2763e-117">PARAMETERS</span></span>

### <span data-ttu-id="2763e-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="2763e-118">-AllowAll</span></span>
<span data-ttu-id="2763e-119">모든 범위 Ip를 허용 하기 위해 제공 합니다 (0.0.0.0 ~ 255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="2763e-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="2763e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2763e-120">-AsJob</span></span>
<span data-ttu-id="2763e-121">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="2763e-121">Run the command as a job</span></span>

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

### <span data-ttu-id="2763e-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="2763e-122">-ClientIPAddress</span></span>
<span data-ttu-id="2763e-123">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="2763e-124">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="2763e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2763e-125">-DefaultProfile</span></span>
<span data-ttu-id="2763e-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2763e-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="2763e-127">-EndIPAddress</span></span>
<span data-ttu-id="2763e-128">서버 방화벽 규칙의 끝 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="2763e-129">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="2763e-130">-이름</span><span class="sxs-lookup"><span data-stu-id="2763e-130">-Name</span></span>
<span data-ttu-id="2763e-131">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="2763e-132">지정 하지 않으면 기본값이 정의 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="2763e-133">AllowAll이 있으면 기본 이름은 AllowAll_yyyy dd_HH-mm-ss입니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="2763e-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2763e-134">-NoWait</span></span>
<span data-ttu-id="2763e-135">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="2763e-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2763e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2763e-136">-ResourceGroupName</span></span>
<span data-ttu-id="2763e-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-137">The name of the resource group.</span></span>
<span data-ttu-id="2763e-138">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2763e-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2763e-139">-ServerName</span></span>
<span data-ttu-id="2763e-140">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-140">The name of the server.</span></span>

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

### <span data-ttu-id="2763e-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="2763e-141">-StartIPAddress</span></span>
<span data-ttu-id="2763e-142">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="2763e-143">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="2763e-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2763e-144">-SubscriptionId</span></span>
<span data-ttu-id="2763e-145">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2763e-146">-확인</span><span class="sxs-lookup"><span data-stu-id="2763e-146">-Confirm</span></span>
<span data-ttu-id="2763e-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2763e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2763e-148">-WhatIf</span></span>
<span data-ttu-id="2763e-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2763e-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2763e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2763e-151">CommonParameters</span></span>
<span data-ttu-id="2763e-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2763e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2763e-153">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2763e-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2763e-154">입력</span><span class="sxs-lookup"><span data-stu-id="2763e-154">INPUTS</span></span>

## <span data-ttu-id="2763e-155">출력</span><span class="sxs-lookup"><span data-stu-id="2763e-155">OUTPUTS</span></span>

### <span data-ttu-id="2763e-156">Api20171201. IFirewallRule에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2763e-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="2763e-157">상속자</span><span class="sxs-lookup"><span data-stu-id="2763e-157">NOTES</span></span>

<span data-ttu-id="2763e-158">별칭과</span><span class="sxs-lookup"><span data-stu-id="2763e-158">ALIASES</span></span>

## <span data-ttu-id="2763e-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2763e-159">RELATED LINKS</span></span>

