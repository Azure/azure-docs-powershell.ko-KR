---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: 7b1ed42777dcd24460dabb91cf67160dac709aea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985894"
---
# <span data-ttu-id="57e8a-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e8a-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="57e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="57e8a-103">서버 구성에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="57e8a-104">구문</span><span class="sxs-lookup"><span data-stu-id="57e8a-104">SYNTAX</span></span>

### <span data-ttu-id="57e8a-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="57e8a-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57e8a-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="57e8a-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57e8a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57e8a-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="57e8a-108">설명</span><span class="sxs-lookup"><span data-stu-id="57e8a-108">DESCRIPTION</span></span>
<span data-ttu-id="57e8a-109">서버 구성에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="57e8a-110">예제</span><span class="sxs-lookup"><span data-stu-id="57e8a-110">EXAMPLES</span></span>

### <span data-ttu-id="57e8a-111">예제 1: 지정된 MySql 서버의 모든 구성 나열</span><span class="sxs-lookup"><span data-stu-id="57e8a-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="57e8a-112">이 cmdlet은 지정된 MySql 서버의 모든 구성을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="57e8a-113">예제 2: 이름에 따라 지정된 MySql 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="57e8a-114">이 cmdlet은 이름으로 지정된 MySql 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="57e8a-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="57e8a-115">PARAMETERS</span></span>

### <span data-ttu-id="57e8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e8a-116">-DefaultProfile</span></span>
<span data-ttu-id="57e8a-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57e8a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57e8a-118">-InputObject</span></span>
<span data-ttu-id="57e8a-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="57e8a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57e8a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="57e8a-120">-Name</span></span>
<span data-ttu-id="57e8a-121">서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="57e8a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57e8a-122">-ResourceGroupName</span></span>
<span data-ttu-id="57e8a-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-123">The name of the resource group.</span></span>
<span data-ttu-id="57e8a-124">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="57e8a-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57e8a-125">-ServerName</span></span>
<span data-ttu-id="57e8a-126">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-126">The name of the server.</span></span>

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

### <span data-ttu-id="57e8a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57e8a-127">-SubscriptionId</span></span>
<span data-ttu-id="57e8a-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="57e8a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e8a-129">CommonParameters</span></span>
<span data-ttu-id="57e8a-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e8a-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57e8a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e8a-132">입력</span><span class="sxs-lookup"><span data-stu-id="57e8a-132">INPUTS</span></span>

### <span data-ttu-id="57e8a-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="57e8a-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="57e8a-134">출력</span><span class="sxs-lookup"><span data-stu-id="57e8a-134">OUTPUTS</span></span>

### <span data-ttu-id="57e8a-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e8a-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="57e8a-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57e8a-136">NOTES</span></span>

<span data-ttu-id="57e8a-137">별칭</span><span class="sxs-lookup"><span data-stu-id="57e8a-137">ALIASES</span></span>

<span data-ttu-id="57e8a-138">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="57e8a-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57e8a-139">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57e8a-140">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57e8a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57e8a-141">INPUTOBJECT <IMySqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="57e8a-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57e8a-142">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="57e8a-143">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="57e8a-144">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="57e8a-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="57e8a-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57e8a-146">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="57e8a-147">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="57e8a-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="57e8a-149">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="57e8a-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="57e8a-151">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="57e8a-152">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="57e8a-153">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57e8a-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="57e8a-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57e8a-154">RELATED LINKS</span></span>

