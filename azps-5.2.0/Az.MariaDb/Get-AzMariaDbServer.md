---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324106"
---
# <span data-ttu-id="428b2-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="428b2-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="428b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="428b2-102">SYNOPSIS</span></span>
<span data-ttu-id="428b2-103">서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-103">Gets information about a server.</span></span>

## <span data-ttu-id="428b2-104">구문</span><span class="sxs-lookup"><span data-stu-id="428b2-104">SYNTAX</span></span>

### <span data-ttu-id="428b2-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="428b2-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="428b2-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="428b2-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="428b2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="428b2-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="428b2-108">목록</span><span class="sxs-lookup"><span data-stu-id="428b2-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="428b2-109">설명</span><span class="sxs-lookup"><span data-stu-id="428b2-109">DESCRIPTION</span></span>
<span data-ttu-id="428b2-110">서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-110">Gets information about a server.</span></span>

## <span data-ttu-id="428b2-111">예제</span><span class="sxs-lookup"><span data-stu-id="428b2-111">EXAMPLES</span></span>

### <span data-ttu-id="428b2-112">예제 1: 구독에서 모든 MariaDB 나열</span><span class="sxs-lookup"><span data-stu-id="428b2-112">Example 1: List all MariaDB under a subscriptions</span></span>
```powershell
PS C:\> Get-AzMariaDbServer

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mrdb01                     eastus   dolauli            10.2    5120                    B_Gen5_1   Basic          Enabled
wyunchi-10                 eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi                    eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi-eastus             eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="428b2-113">이 명령은 구독에 있는 모든 MariaDB를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="428b2-114">예제 2: 리소스 그룹 아래에 모든 MariaDB 나열</span><span class="sxs-lookup"><span data-stu-id="428b2-114">Example 2: List all MariaDB under a resource group</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="428b2-115">이 명령은 리소스 그룹 아래에 있는 모든 MariaDB를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="428b2-116">예제 3: MariaDB를 얻게</span><span class="sxs-lookup"><span data-stu-id="428b2-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="428b2-117">이 명령은 MariaDB를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="428b2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="428b2-118">PARAMETERS</span></span>

### <span data-ttu-id="428b2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428b2-119">-DefaultProfile</span></span>
<span data-ttu-id="428b2-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428b2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="428b2-121">-InputObject</span></span>
<span data-ttu-id="428b2-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="428b2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="428b2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="428b2-123">-Name</span></span>
<span data-ttu-id="428b2-124">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-124">The name of the server.</span></span>

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

### <span data-ttu-id="428b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="428b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="428b2-126">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="428b2-127">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="428b2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="428b2-128">-SubscriptionId</span></span>
<span data-ttu-id="428b2-129">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="428b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428b2-130">CommonParameters</span></span>
<span data-ttu-id="428b2-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428b2-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="428b2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428b2-133">입력</span><span class="sxs-lookup"><span data-stu-id="428b2-133">INPUTS</span></span>

### <span data-ttu-id="428b2-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="428b2-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="428b2-135">출력</span><span class="sxs-lookup"><span data-stu-id="428b2-135">OUTPUTS</span></span>

### <span data-ttu-id="428b2-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="428b2-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="428b2-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="428b2-137">NOTES</span></span>

<span data-ttu-id="428b2-138">별칭</span><span class="sxs-lookup"><span data-stu-id="428b2-138">ALIASES</span></span>

<span data-ttu-id="428b2-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="428b2-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="428b2-140">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="428b2-141">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="428b2-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="428b2-142">INPUTOBJECT: <IMariaDbIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="428b2-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="428b2-143">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="428b2-144">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="428b2-145">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="428b2-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="428b2-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="428b2-147">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="428b2-148">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="428b2-149">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="428b2-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="428b2-151">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="428b2-152">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="428b2-153">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="428b2-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="428b2-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="428b2-154">RELATED LINKS</span></span>

