---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049017"
---
# <span data-ttu-id="d3553-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d3553-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="d3553-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3553-102">SYNOPSIS</span></span>
<span data-ttu-id="d3553-103">새 방화벽 규칙을 만들거나 기존 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d3553-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3553-104">SYNTAX</span></span>

### <span data-ttu-id="d3553-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="d3553-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d3553-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="d3553-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d3553-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d3553-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d3553-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d3553-108">DESCRIPTION</span></span>
<span data-ttu-id="d3553-109">새 방화벽 규칙을 만들거나 기존 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d3553-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d3553-110">EXAMPLES</span></span>

### <span data-ttu-id="d3553-111">예제 1: a 2 i 아래에 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="d3553-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="d3553-112">이 명령은 그 아래에 있는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="d3553-113">예제 2:-ClientIPAddress를 사용 하 여 새 Iadb 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="d3553-114">이 cmdlet은-ClientIPAddress를 사용 하 여로이를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="d3553-115">예제 3: 모든 Ip를 허용 하는 새로운 작업을 새로 하는 Adb 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="d3553-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="d3553-116">이 cmdlet은 모든 Ip를 허용 하는 새로운을 위한 새 \ \* 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="d3553-117">변수</span><span class="sxs-lookup"><span data-stu-id="d3553-117">PARAMETERS</span></span>

### <span data-ttu-id="d3553-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="d3553-118">-AllowAll</span></span>
<span data-ttu-id="d3553-119">모든 범위 Ip를 허용 하기 위해 제공 합니다 (0.0.0.0 ~ 255.255.255.255).</span><span class="sxs-lookup"><span data-stu-id="d3553-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="d3553-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3553-120">-AsJob</span></span>
<span data-ttu-id="d3553-121">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d3553-121">Run the command as a job</span></span>

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

### <span data-ttu-id="d3553-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d3553-122">-ClientIPAddress</span></span>
<span data-ttu-id="d3553-123">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="d3553-124">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d3553-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3553-125">-DefaultProfile</span></span>
<span data-ttu-id="d3553-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3553-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="d3553-127">-EndIPAddress</span></span>
<span data-ttu-id="d3553-128">서버 방화벽 규칙의 끝 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="d3553-129">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d3553-130">-이름</span><span class="sxs-lookup"><span data-stu-id="d3553-130">-Name</span></span>
<span data-ttu-id="d3553-131">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="d3553-132">지정 하지 않으면 기본값이 정의 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="d3553-133">AllowAll이 있으면 기본 이름은 AllowAll_yyyy dd_HH-mm-ss입니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="d3553-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d3553-134">-NoWait</span></span>
<span data-ttu-id="d3553-135">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d3553-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d3553-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3553-136">-ResourceGroupName</span></span>
<span data-ttu-id="d3553-137">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d3553-138">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d3553-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3553-139">-ServerName</span></span>
<span data-ttu-id="d3553-140">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-140">The name of the server.</span></span>

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

### <span data-ttu-id="d3553-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="d3553-141">-StartIPAddress</span></span>
<span data-ttu-id="d3553-142">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="d3553-143">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d3553-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3553-144">-SubscriptionId</span></span>
<span data-ttu-id="d3553-145">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d3553-146">-확인</span><span class="sxs-lookup"><span data-stu-id="d3553-146">-Confirm</span></span>
<span data-ttu-id="d3553-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3553-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3553-148">-WhatIf</span></span>
<span data-ttu-id="d3553-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3553-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3553-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3553-151">CommonParameters</span></span>
<span data-ttu-id="d3553-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3553-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3553-153">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3553-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3553-154">입력</span><span class="sxs-lookup"><span data-stu-id="d3553-154">INPUTS</span></span>

## <span data-ttu-id="d3553-155">출력</span><span class="sxs-lookup"><span data-stu-id="d3553-155">OUTPUTS</span></span>

### <span data-ttu-id="d3553-156">Microsoft. Api20180601Preview. IFirewallRule에 대 한. b a r i.</span><span class="sxs-lookup"><span data-stu-id="d3553-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="d3553-157">상속자</span><span class="sxs-lookup"><span data-stu-id="d3553-157">NOTES</span></span>

<span data-ttu-id="d3553-158">별칭과</span><span class="sxs-lookup"><span data-stu-id="d3553-158">ALIASES</span></span>

## <span data-ttu-id="d3553-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3553-159">RELATED LINKS</span></span>

