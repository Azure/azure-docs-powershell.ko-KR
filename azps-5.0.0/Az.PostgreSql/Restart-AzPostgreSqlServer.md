---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218222"
---
# <span data-ttu-id="a38d5-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="a38d5-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="a38d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a38d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a38d5-103">서버를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-103">Restarts a server.</span></span>

## <span data-ttu-id="a38d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a38d5-104">SYNTAX</span></span>

### <span data-ttu-id="a38d5-105">다시 시작 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a38d5-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a38d5-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a38d5-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a38d5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a38d5-107">DESCRIPTION</span></span>
<span data-ttu-id="a38d5-108">서버를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-108">Restarts a server.</span></span>

## <span data-ttu-id="a38d5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a38d5-109">EXAMPLES</span></span>

### <span data-ttu-id="a38d5-110">예제 1: 리소스 그룹 및 서버 이름으로 PostgreSql 서버 다시 시작</span><span class="sxs-lookup"><span data-stu-id="a38d5-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="a38d5-111">이 cmdlet은 PostgreSql server를 리소스 그룹 및 서버 이름으로 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="a38d5-112">예제 2: id를 기준으로 PostgreSql 서버 다시 시작</span><span class="sxs-lookup"><span data-stu-id="a38d5-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="a38d5-113">이러한 cmdlet은 id를 기준으로 PostgreSql 서버를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="a38d5-114">변수</span><span class="sxs-lookup"><span data-stu-id="a38d5-114">PARAMETERS</span></span>

### <span data-ttu-id="a38d5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a38d5-115">-AsJob</span></span>
<span data-ttu-id="a38d5-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a38d5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a38d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a38d5-117">-DefaultProfile</span></span>
<span data-ttu-id="a38d5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a38d5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a38d5-119">-InputObject</span></span>
<span data-ttu-id="a38d5-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a38d5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="a38d5-121">-Name</span></span>
<span data-ttu-id="a38d5-122">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a38d5-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a38d5-123">-NoWait</span></span>
<span data-ttu-id="a38d5-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a38d5-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a38d5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a38d5-125">-PassThru</span></span>
<span data-ttu-id="a38d5-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a38d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a38d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="a38d5-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-128">The name of the resource group.</span></span>
<span data-ttu-id="a38d5-129">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a38d5-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a38d5-130">-SubscriptionId</span></span>
<span data-ttu-id="a38d5-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a38d5-132">-확인</span><span class="sxs-lookup"><span data-stu-id="a38d5-132">-Confirm</span></span>
<span data-ttu-id="a38d5-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a38d5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a38d5-134">-WhatIf</span></span>
<span data-ttu-id="a38d5-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a38d5-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a38d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a38d5-137">CommonParameters</span></span>
<span data-ttu-id="a38d5-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a38d5-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a38d5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a38d5-140">입력</span><span class="sxs-lookup"><span data-stu-id="a38d5-140">INPUTS</span></span>

### <span data-ttu-id="a38d5-141">PostgreSql. IPostgreSqlIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="a38d5-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="a38d5-142">출력</span><span class="sxs-lookup"><span data-stu-id="a38d5-142">OUTPUTS</span></span>

### <span data-ttu-id="a38d5-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a38d5-143">System.Boolean</span></span>

## <span data-ttu-id="a38d5-144">상속자</span><span class="sxs-lookup"><span data-stu-id="a38d5-144">NOTES</span></span>

<span data-ttu-id="a38d5-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="a38d5-145">ALIASES</span></span>

<span data-ttu-id="a38d5-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a38d5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a38d5-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a38d5-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a38d5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a38d5-149">INPUTOBJECT <IPostgreSqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a38d5-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a38d5-150">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a38d5-151">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a38d5-152">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a38d5-153">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="a38d5-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a38d5-154">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a38d5-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a38d5-156">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="a38d5-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a38d5-158">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a38d5-159">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a38d5-160">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a38d5-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a38d5-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a38d5-161">RELATED LINKS</span></span>

