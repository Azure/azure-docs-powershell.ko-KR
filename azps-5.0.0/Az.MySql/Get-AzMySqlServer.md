---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: e2187c95237cdb89915c47fc7089fd5f9d38cff1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309629"
---
# <span data-ttu-id="11a58-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="11a58-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="11a58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11a58-102">SYNOPSIS</span></span>
<span data-ttu-id="11a58-103">서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-103">Gets information about a server.</span></span>

## <span data-ttu-id="11a58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11a58-104">SYNTAX</span></span>

### <span data-ttu-id="11a58-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="11a58-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11a58-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="11a58-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11a58-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11a58-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11a58-108">목록</span><span class="sxs-lookup"><span data-stu-id="11a58-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="11a58-109">설명은</span><span class="sxs-lookup"><span data-stu-id="11a58-109">DESCRIPTION</span></span>
<span data-ttu-id="11a58-110">서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-110">Gets information about a server.</span></span>

## <span data-ttu-id="11a58-111">예제의</span><span class="sxs-lookup"><span data-stu-id="11a58-111">EXAMPLES</span></span>

### <span data-ttu-id="11a58-112">예제 1: 기본 컨텍스트를 사용 하 여 MySql 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="11a58-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="11a58-113">이 cmdlet은 기본 컨텍스트를 사용 하 여 MySql 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="11a58-114">예제 2: 리소스 그룹 및 서버 이름으로 MySql 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="11a58-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="11a58-115">이 cmdlet은 리소스 그룹 및 서버 이름에 따라 MySql 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="11a58-116">예제 3: 지정 된 리소스 그룹의 모든 MySql 서버 나열</span><span class="sxs-lookup"><span data-stu-id="11a58-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="11a58-117">이 cmdlet은 지정 된 리소스 그룹에 있는 모든 MySql 서버를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="11a58-118">예제 4: id 별 MySql 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="11a58-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="11a58-119">이 cmdlet 목록은 id를 기준으로 MySql 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="11a58-120">변수</span><span class="sxs-lookup"><span data-stu-id="11a58-120">PARAMETERS</span></span>

### <span data-ttu-id="11a58-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a58-121">-DefaultProfile</span></span>
<span data-ttu-id="11a58-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11a58-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11a58-123">-InputObject</span></span>
<span data-ttu-id="11a58-124">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="11a58-125">-이름</span><span class="sxs-lookup"><span data-stu-id="11a58-125">-Name</span></span>
<span data-ttu-id="11a58-126">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-126">The name of the server.</span></span>

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

### <span data-ttu-id="11a58-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11a58-127">-ResourceGroupName</span></span>
<span data-ttu-id="11a58-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-128">The name of the resource group.</span></span>
<span data-ttu-id="11a58-129">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="11a58-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11a58-130">-SubscriptionId</span></span>
<span data-ttu-id="11a58-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="11a58-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a58-132">CommonParameters</span></span>
<span data-ttu-id="11a58-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a58-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11a58-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a58-135">입력</span><span class="sxs-lookup"><span data-stu-id="11a58-135">INPUTS</span></span>

### <span data-ttu-id="11a58-136">IMySqlIdentity (Microsoft. PowerShell)</span><span class="sxs-lookup"><span data-stu-id="11a58-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="11a58-137">출력</span><span class="sxs-lookup"><span data-stu-id="11a58-137">OUTPUTS</span></span>

### <span data-ttu-id="11a58-138">Api20171201 (Microsoft. i m/. i m/. i m/. 서버)</span><span class="sxs-lookup"><span data-stu-id="11a58-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="11a58-139">상속자</span><span class="sxs-lookup"><span data-stu-id="11a58-139">NOTES</span></span>

<span data-ttu-id="11a58-140">별칭과</span><span class="sxs-lookup"><span data-stu-id="11a58-140">ALIASES</span></span>

<span data-ttu-id="11a58-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="11a58-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11a58-142">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11a58-143">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="11a58-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11a58-144">INPUTOBJECT <IMySqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="11a58-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11a58-145">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="11a58-146">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="11a58-147">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="11a58-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="11a58-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11a58-149">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="11a58-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="11a58-151">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="11a58-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="11a58-153">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="11a58-154">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="11a58-155">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11a58-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="11a58-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11a58-156">RELATED LINKS</span></span>

