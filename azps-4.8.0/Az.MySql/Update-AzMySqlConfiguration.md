---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: c4eb244dd2d1a0d685bf18f39deedf9992b5597e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048977"
---
# <span data-ttu-id="9f113-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f113-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="9f113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f113-102">SYNOPSIS</span></span>
<span data-ttu-id="9f113-103">서버 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="9f113-104">AdministratorLoginPassword, sku 등을 업데이트 하려는 경우 대신 Update-AzMySqlServer를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="9f113-105">구문과</span><span class="sxs-lookup"><span data-stu-id="9f113-105">SYNTAX</span></span>

### <span data-ttu-id="9f113-106">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9f113-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9f113-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9f113-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f113-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9f113-108">DESCRIPTION</span></span>
<span data-ttu-id="9f113-109">서버 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="9f113-110">AdministratorLoginPassword, sku 등을 업데이트 하려는 경우 대신 Update-AzMySqlServer를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="9f113-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9f113-111">EXAMPLES</span></span>

### <span data-ttu-id="9f113-112">예제 1: 이름별로 MySql 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="9f113-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="9f113-113">이 cmdlet은 이름으로 MySql 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="9f113-114">예제 2: id를 기준으로 MySql 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="9f113-115">이러한 cmdlet은 id를 기준으로 MySql 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="9f113-116">변수</span><span class="sxs-lookup"><span data-stu-id="9f113-116">PARAMETERS</span></span>

### <span data-ttu-id="9f113-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f113-117">-AsJob</span></span>
<span data-ttu-id="9f113-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9f113-118">Run the command as a job</span></span>

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

### <span data-ttu-id="9f113-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f113-119">-DefaultProfile</span></span>
<span data-ttu-id="9f113-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f113-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f113-121">-InputObject</span></span>
<span data-ttu-id="9f113-122">Id 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-122">Identity Parameter.</span></span>
<span data-ttu-id="9f113-123">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f113-124">-이름</span><span class="sxs-lookup"><span data-stu-id="9f113-124">-Name</span></span>
<span data-ttu-id="9f113-125">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-125">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f113-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9f113-126">-NoWait</span></span>
<span data-ttu-id="9f113-127">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9f113-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9f113-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f113-128">-ResourceGroupName</span></span>
<span data-ttu-id="9f113-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-129">The name of the resource group.</span></span>
<span data-ttu-id="9f113-130">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-130">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f113-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9f113-131">-ServerName</span></span>
<span data-ttu-id="9f113-132">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-132">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f113-133">-원본</span><span class="sxs-lookup"><span data-stu-id="9f113-133">-Source</span></span>
<span data-ttu-id="9f113-134">구성의 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-134">Source of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f113-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f113-135">-SubscriptionId</span></span>
<span data-ttu-id="9f113-136">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f113-137">-값</span><span class="sxs-lookup"><span data-stu-id="9f113-137">-Value</span></span>
<span data-ttu-id="9f113-138">구성의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-138">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f113-139">-확인</span><span class="sxs-lookup"><span data-stu-id="9f113-139">-Confirm</span></span>
<span data-ttu-id="9f113-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f113-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f113-141">-WhatIf</span></span>
<span data-ttu-id="9f113-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f113-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f113-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f113-144">CommonParameters</span></span>
<span data-ttu-id="9f113-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f113-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f113-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f113-147">입력</span><span class="sxs-lookup"><span data-stu-id="9f113-147">INPUTS</span></span>

### <span data-ttu-id="9f113-148">IMySqlIdentity (Microsoft. PowerShell)</span><span class="sxs-lookup"><span data-stu-id="9f113-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9f113-149">출력</span><span class="sxs-lookup"><span data-stu-id="9f113-149">OUTPUTS</span></span>

### <span data-ttu-id="9f113-150">Api20171201. IConfiguration에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9f113-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="9f113-151">상속자</span><span class="sxs-lookup"><span data-stu-id="9f113-151">NOTES</span></span>

<span data-ttu-id="9f113-152">별칭과</span><span class="sxs-lookup"><span data-stu-id="9f113-152">ALIASES</span></span>

<span data-ttu-id="9f113-153">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="9f113-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f113-154">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f113-155">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f113-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f113-156">INPUTOBJECT <IMySqlIdentity> : Identity 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="9f113-157">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9f113-158">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9f113-159">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9f113-160">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="9f113-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9f113-161">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9f113-162">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9f113-163">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="9f113-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9f113-165">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9f113-166">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9f113-167">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f113-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9f113-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f113-168">RELATED LINKS</span></span>

