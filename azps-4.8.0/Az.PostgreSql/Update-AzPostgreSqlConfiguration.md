---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203803"
---
# <span data-ttu-id="b0a4a-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0a4a-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="b0a4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a4a-103">서버 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="b0a4a-104">AdministratorLoginPassword, sku 등을 업데이트 하려는 경우 대신 Update-AzPostgreSqlServer를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="b0a4a-105">구문과</span><span class="sxs-lookup"><span data-stu-id="b0a4a-105">SYNTAX</span></span>

### <span data-ttu-id="b0a4a-106">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b0a4a-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b0a4a-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b0a4a-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b0a4a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b0a4a-108">DESCRIPTION</span></span>
<span data-ttu-id="b0a4a-109">서버 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="b0a4a-110">AdministratorLoginPassword, sku 등을 업데이트 하려는 경우 대신 Update-AzPostgreSqlServer를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="b0a4a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b0a4a-111">EXAMPLES</span></span>

### <span data-ttu-id="b0a4a-112">예제 1: 이름으로 PostgreSql 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="b0a4a-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="b0a4a-113">이 cmdlet은 이름으로 PostgreSql 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="b0a4a-114">예제 2: id를 기준으로 PostgreSql 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="b0a4a-115">이러한 cmdlet은 id를 기준으로 PostgreSql 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="b0a4a-116">변수</span><span class="sxs-lookup"><span data-stu-id="b0a4a-116">PARAMETERS</span></span>

### <span data-ttu-id="b0a4a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0a4a-117">-AsJob</span></span>
<span data-ttu-id="b0a4a-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b0a4a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b0a4a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a4a-119">-DefaultProfile</span></span>
<span data-ttu-id="b0a4a-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0a4a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0a4a-121">-InputObject</span></span>
<span data-ttu-id="b0a4a-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a4a-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b0a4a-123">-Name</span></span>
<span data-ttu-id="b0a4a-124">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="b0a4a-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b0a4a-125">-NoWait</span></span>
<span data-ttu-id="b0a4a-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b0a4a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b0a4a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a4a-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0a4a-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-128">The name of the resource group.</span></span>
<span data-ttu-id="b0a4a-129">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b0a4a-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b0a4a-130">-ServerName</span></span>
<span data-ttu-id="b0a4a-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-131">The name of the server.</span></span>

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

### <span data-ttu-id="b0a4a-132">-원본</span><span class="sxs-lookup"><span data-stu-id="b0a4a-132">-Source</span></span>
<span data-ttu-id="b0a4a-133">구성의 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="b0a4a-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0a4a-134">-SubscriptionId</span></span>
<span data-ttu-id="b0a4a-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b0a4a-136">-값</span><span class="sxs-lookup"><span data-stu-id="b0a4a-136">-Value</span></span>
<span data-ttu-id="b0a4a-137">구성의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="b0a4a-138">-확인</span><span class="sxs-lookup"><span data-stu-id="b0a4a-138">-Confirm</span></span>
<span data-ttu-id="b0a4a-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0a4a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0a4a-140">-WhatIf</span></span>
<span data-ttu-id="b0a4a-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0a4a-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0a4a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a4a-143">CommonParameters</span></span>
<span data-ttu-id="b0a4a-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a4a-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a4a-146">입력</span><span class="sxs-lookup"><span data-stu-id="b0a4a-146">INPUTS</span></span>

### <span data-ttu-id="b0a4a-147">PostgreSql. IPostgreSqlIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0a4a-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b0a4a-148">출력</span><span class="sxs-lookup"><span data-stu-id="b0a4a-148">OUTPUTS</span></span>

### <span data-ttu-id="b0a4a-149">PostgreSql. Api20171201. IConfiguration에 대 한</span><span class="sxs-lookup"><span data-stu-id="b0a4a-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="b0a4a-150">상속자</span><span class="sxs-lookup"><span data-stu-id="b0a4a-150">NOTES</span></span>

<span data-ttu-id="b0a4a-151">별칭과</span><span class="sxs-lookup"><span data-stu-id="b0a4a-151">ALIASES</span></span>

<span data-ttu-id="b0a4a-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b0a4a-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0a4a-153">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0a4a-154">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0a4a-155">INPUTOBJECT <IPostgreSqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b0a4a-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0a4a-156">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b0a4a-157">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b0a4a-158">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b0a4a-159">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b0a4a-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0a4a-160">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b0a4a-161">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b0a4a-162">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="b0a4a-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b0a4a-164">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b0a4a-165">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b0a4a-166">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a4a-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b0a4a-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0a4a-167">RELATED LINKS</span></span>

