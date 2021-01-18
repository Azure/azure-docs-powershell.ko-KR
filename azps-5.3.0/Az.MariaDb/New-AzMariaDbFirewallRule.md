---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492827"
---
# <span data-ttu-id="b4ee6-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4ee6-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="b4ee6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ee6-103">새 방화벽 규칙을 생성하거나 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b4ee6-104">구문</span><span class="sxs-lookup"><span data-stu-id="b4ee6-104">SYNTAX</span></span>

### <span data-ttu-id="b4ee6-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="b4ee6-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b4ee6-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="b4ee6-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b4ee6-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b4ee6-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b4ee6-108">설명</span><span class="sxs-lookup"><span data-stu-id="b4ee6-108">DESCRIPTION</span></span>
<span data-ttu-id="b4ee6-109">새 방화벽 규칙을 생성하거나 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b4ee6-110">예제</span><span class="sxs-lookup"><span data-stu-id="b4ee6-110">EXAMPLES</span></span>

### <span data-ttu-id="b4ee6-111">예제 1: MariaDB에서 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="b4ee6-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="b4ee6-112">이 명령은 MariaDB 아래에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="b4ee6-113">예제 2: -ClientIPAddress를 사용하여 새 MariaDB 방화벽 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="b4ee6-114">이 cmdlet은 -ClientIPAddress를 사용하여 MariaDB 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="b4ee6-115">예제 3: 모든 IPS를 허용하는 새 MariaDB 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="b4ee6-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="b4ee6-116">이 cmdlet은 모든 IPS를 허용하는 새 MariaDB 방화벽 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="b4ee6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4ee6-117">PARAMETERS</span></span>

### <span data-ttu-id="b4ee6-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="b4ee6-118">-AllowAll</span></span>
<span data-ttu-id="b4ee6-119">0.0.0.0에서 255.255.255.255.255까지 모든 범위의 IPS를 허용하도록 제시합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="b4ee6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4ee6-120">-AsJob</span></span>
<span data-ttu-id="b4ee6-121">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b4ee6-121">Run the command as a job</span></span>

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

### <span data-ttu-id="b4ee6-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b4ee6-122">-ClientIPAddress</span></span>
<span data-ttu-id="b4ee6-123">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b4ee6-124">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b4ee6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ee6-125">-DefaultProfile</span></span>
<span data-ttu-id="b4ee6-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ee6-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b4ee6-127">-EndIPAddress</span></span>
<span data-ttu-id="b4ee6-128">서버 방화벽 규칙의 최종 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b4ee6-129">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b4ee6-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b4ee6-130">-Name</span></span>
<span data-ttu-id="b4ee6-131">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="b4ee6-132">지정하지 않으면 기본값이 정의되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="b4ee6-133">AllowAll이 있는 경우 기본 이름은 AllowAll_yyyy-MM-dd_HH-mm-ss입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="b4ee6-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b4ee6-134">-NoWait</span></span>
<span data-ttu-id="b4ee6-135">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="b4ee6-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b4ee6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ee6-136">-ResourceGroupName</span></span>
<span data-ttu-id="b4ee6-137">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b4ee6-138">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b4ee6-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4ee6-139">-ServerName</span></span>
<span data-ttu-id="b4ee6-140">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-140">The name of the server.</span></span>

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

### <span data-ttu-id="b4ee6-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b4ee6-141">-StartIPAddress</span></span>
<span data-ttu-id="b4ee6-142">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b4ee6-143">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b4ee6-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4ee6-144">-SubscriptionId</span></span>
<span data-ttu-id="b4ee6-145">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b4ee6-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4ee6-146">-Confirm</span></span>
<span data-ttu-id="b4ee6-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ee6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ee6-148">-WhatIf</span></span>
<span data-ttu-id="b4ee6-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b4ee6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4ee6-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ee6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ee6-151">CommonParameters</span></span>
<span data-ttu-id="b4ee6-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ee6-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4ee6-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ee6-154">입력</span><span class="sxs-lookup"><span data-stu-id="b4ee6-154">INPUTS</span></span>

## <span data-ttu-id="b4ee6-155">출력</span><span class="sxs-lookup"><span data-stu-id="b4ee6-155">OUTPUTS</span></span>

### <span data-ttu-id="b4ee6-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4ee6-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="b4ee6-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b4ee6-157">NOTES</span></span>

<span data-ttu-id="b4ee6-158">별칭</span><span class="sxs-lookup"><span data-stu-id="b4ee6-158">ALIASES</span></span>

## <span data-ttu-id="b4ee6-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4ee6-159">RELATED LINKS</span></span>

