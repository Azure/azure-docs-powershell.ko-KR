---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 97b16f3930eda94e69c3528432ee54927c3eef7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951088"
---
# <span data-ttu-id="8e434-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e434-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="8e434-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e434-102">SYNOPSIS</span></span>
<span data-ttu-id="8e434-103">서버 구성에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="8e434-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e434-104">SYNTAX</span></span>

### <span data-ttu-id="8e434-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="8e434-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e434-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="8e434-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e434-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e434-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e434-108">설명</span><span class="sxs-lookup"><span data-stu-id="8e434-108">DESCRIPTION</span></span>
<span data-ttu-id="8e434-109">서버 구성에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="8e434-110">예제</span><span class="sxs-lookup"><span data-stu-id="8e434-110">EXAMPLES</span></span>

### <span data-ttu-id="8e434-111">예제 1: PostgreSql 서버의 모든 구성 나열</span><span class="sxs-lookup"><span data-stu-id="8e434-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="8e434-112">이 cmdlet은 지정된 PostgreSql 서버의 모든 구성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="8e434-113">예제 2: 이름에 따라 지정된 PostgreSql 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="8e434-114">이 cmdlet은 이름으로 지정된 PostgreSql 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="8e434-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e434-115">PARAMETERS</span></span>

### <span data-ttu-id="8e434-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e434-116">-DefaultProfile</span></span>
<span data-ttu-id="8e434-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e434-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e434-118">-InputObject</span></span>
<span data-ttu-id="8e434-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8e434-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e434-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8e434-120">-Name</span></span>
<span data-ttu-id="8e434-121">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e434-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e434-122">-ResourceGroupName</span></span>
<span data-ttu-id="8e434-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-123">The name of the resource group.</span></span>
<span data-ttu-id="8e434-124">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-124">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e434-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e434-125">-ServerName</span></span>
<span data-ttu-id="8e434-126">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e434-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e434-127">-SubscriptionId</span></span>
<span data-ttu-id="8e434-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e434-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e434-129">CommonParameters</span></span>
<span data-ttu-id="8e434-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e434-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e434-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e434-132">입력</span><span class="sxs-lookup"><span data-stu-id="8e434-132">INPUTS</span></span>

### <span data-ttu-id="8e434-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8e434-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="8e434-134">출력</span><span class="sxs-lookup"><span data-stu-id="8e434-134">OUTPUTS</span></span>

### <span data-ttu-id="8e434-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e434-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="8e434-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e434-136">NOTES</span></span>

<span data-ttu-id="8e434-137">별칭</span><span class="sxs-lookup"><span data-stu-id="8e434-137">ALIASES</span></span>

<span data-ttu-id="8e434-138">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8e434-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e434-139">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e434-140">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e434-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e434-141">INPUTOBJECT <IPostgreSqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e434-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e434-142">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8e434-143">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8e434-144">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8e434-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="8e434-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e434-146">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8e434-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8e434-148">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="8e434-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8e434-150">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8e434-151">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8e434-152">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e434-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8e434-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e434-153">RELATED LINKS</span></span>

