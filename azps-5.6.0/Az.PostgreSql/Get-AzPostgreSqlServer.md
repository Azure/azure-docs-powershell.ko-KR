---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 718443cc31972f1d1d53a5b5802dc50c1ac31df0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982320"
---
# <span data-ttu-id="73339-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="73339-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="73339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73339-102">SYNOPSIS</span></span>
<span data-ttu-id="73339-103">서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73339-103">Gets information about a server.</span></span>

## <span data-ttu-id="73339-104">구문</span><span class="sxs-lookup"><span data-stu-id="73339-104">SYNTAX</span></span>

### <span data-ttu-id="73339-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="73339-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73339-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="73339-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73339-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73339-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73339-108">목록</span><span class="sxs-lookup"><span data-stu-id="73339-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="73339-109">설명</span><span class="sxs-lookup"><span data-stu-id="73339-109">DESCRIPTION</span></span>
<span data-ttu-id="73339-110">서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73339-110">Gets information about a server.</span></span>

## <span data-ttu-id="73339-111">예제</span><span class="sxs-lookup"><span data-stu-id="73339-111">EXAMPLES</span></span>

### <span data-ttu-id="73339-112">예제 1: 기본 컨텍스트가 있는 PostgreSql 서버 사용</span><span class="sxs-lookup"><span data-stu-id="73339-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="73339-113">이 cmdlet은 기본 컨텍스트가 있는 PostgreSql 서버를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="73339-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="73339-114">예제 2: 리소스 그룹 및 서버 이름으로 PostgreSql 서버 사용</span><span class="sxs-lookup"><span data-stu-id="73339-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="73339-115">이 cmdlet은 리소스 그룹 및 서버 이름으로 PostgreSql 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73339-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="73339-116">예제 3: 지정된 리소스 그룹에 모든 PostgreSql 서버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="73339-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="73339-117">이 cmdlet은 지정된 리소스 그룹에 있는 모든 PostgreSql 서버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="73339-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="73339-118">예제 4: ID로 PostgreSql 서버 사용</span><span class="sxs-lookup"><span data-stu-id="73339-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="73339-119">이 cmdlet 목록은 ID로 PostgreSql 서버를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="73339-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="73339-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="73339-120">PARAMETERS</span></span>

### <span data-ttu-id="73339-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73339-121">-DefaultProfile</span></span>
<span data-ttu-id="73339-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73339-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73339-123">-InputObject</span></span>
<span data-ttu-id="73339-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="73339-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73339-125">-Name</span><span class="sxs-lookup"><span data-stu-id="73339-125">-Name</span></span>
<span data-ttu-id="73339-126">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73339-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73339-127">-ResourceGroupName</span></span>
<span data-ttu-id="73339-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-128">The name of the resource group.</span></span>
<span data-ttu-id="73339-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="73339-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="73339-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73339-130">-SubscriptionId</span></span>
<span data-ttu-id="73339-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73339-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73339-132">CommonParameters</span></span>
<span data-ttu-id="73339-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73339-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73339-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73339-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73339-135">입력</span><span class="sxs-lookup"><span data-stu-id="73339-135">INPUTS</span></span>

### <span data-ttu-id="73339-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="73339-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="73339-137">출력</span><span class="sxs-lookup"><span data-stu-id="73339-137">OUTPUTS</span></span>

### <span data-ttu-id="73339-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="73339-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="73339-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="73339-139">NOTES</span></span>

<span data-ttu-id="73339-140">별칭</span><span class="sxs-lookup"><span data-stu-id="73339-140">ALIASES</span></span>

<span data-ttu-id="73339-141">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="73339-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73339-142">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="73339-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73339-143">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73339-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73339-144">INPUTOBJECT <IPostgreSqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="73339-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73339-145">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="73339-146">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="73339-147">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="73339-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="73339-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73339-149">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="73339-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="73339-151">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="73339-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="73339-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="73339-153">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="73339-154">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="73339-155">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73339-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="73339-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73339-156">RELATED LINKS</span></span>

