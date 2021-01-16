---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: 4308f2ec3da458f03e53d17a873d92ea5d775ff4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367389"
---
# <span data-ttu-id="e717c-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="e717c-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="e717c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e717c-102">SYNOPSIS</span></span>
<span data-ttu-id="e717c-103">서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-103">Gets information about a server.</span></span>

## <span data-ttu-id="e717c-104">구문</span><span class="sxs-lookup"><span data-stu-id="e717c-104">SYNTAX</span></span>

### <span data-ttu-id="e717c-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="e717c-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e717c-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e717c-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e717c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e717c-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e717c-108">목록</span><span class="sxs-lookup"><span data-stu-id="e717c-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e717c-109">설명</span><span class="sxs-lookup"><span data-stu-id="e717c-109">DESCRIPTION</span></span>
<span data-ttu-id="e717c-110">서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-110">Gets information about a server.</span></span>

## <span data-ttu-id="e717c-111">예제</span><span class="sxs-lookup"><span data-stu-id="e717c-111">EXAMPLES</span></span>

### <span data-ttu-id="e717c-112">예제 1: 기본 컨텍스트를 통해 MySql 서버 얻기</span><span class="sxs-lookup"><span data-stu-id="e717c-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e717c-113">이 cmdlet은 기본 컨텍스트를 통해 MySql 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="e717c-114">예제 2: 리소스 그룹 및 서버 이름으로 MySql 서버 얻기</span><span class="sxs-lookup"><span data-stu-id="e717c-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e717c-115">이 cmdlet은 리소스 그룹 및 서버 이름으로 MySql 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="e717c-116">예제 3: 지정된 리소스 그룹의 모든 MySql 서버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e717c-117">이 cmdlet은 지정된 리소스 그룹의 모든 MySql 서버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="e717c-118">예제 4: ID로 MySql 서버 얻기</span><span class="sxs-lookup"><span data-stu-id="e717c-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e717c-119">이 cmdlet 목록은 ID로 MySql 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="e717c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e717c-120">PARAMETERS</span></span>

### <span data-ttu-id="e717c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e717c-121">-DefaultProfile</span></span>
<span data-ttu-id="e717c-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e717c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e717c-123">-InputObject</span></span>
<span data-ttu-id="e717c-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e717c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e717c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e717c-125">-Name</span></span>
<span data-ttu-id="e717c-126">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-126">The name of the server.</span></span>

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

### <span data-ttu-id="e717c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e717c-127">-ResourceGroupName</span></span>
<span data-ttu-id="e717c-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-128">The name of the resource group.</span></span>
<span data-ttu-id="e717c-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e717c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e717c-130">-SubscriptionId</span></span>
<span data-ttu-id="e717c-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e717c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e717c-132">CommonParameters</span></span>
<span data-ttu-id="e717c-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e717c-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e717c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e717c-135">입력</span><span class="sxs-lookup"><span data-stu-id="e717c-135">INPUTS</span></span>

### <span data-ttu-id="e717c-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e717c-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="e717c-137">출력</span><span class="sxs-lookup"><span data-stu-id="e717c-137">OUTPUTS</span></span>

### <span data-ttu-id="e717c-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="e717c-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e717c-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e717c-139">NOTES</span></span>

<span data-ttu-id="e717c-140">별칭</span><span class="sxs-lookup"><span data-stu-id="e717c-140">ALIASES</span></span>

<span data-ttu-id="e717c-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e717c-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e717c-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e717c-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e717c-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e717c-144">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e717c-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e717c-145">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e717c-146">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e717c-147">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e717c-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e717c-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e717c-149">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="e717c-150">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e717c-151">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e717c-152">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="e717c-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e717c-154">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e717c-155">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e717c-156">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e717c-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e717c-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e717c-157">RELATED LINKS</span></span>

