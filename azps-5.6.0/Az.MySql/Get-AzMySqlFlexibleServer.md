---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: cbbe321f23fb95bca8a4a70dd59f30ec098cf2d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012011"
---
# <span data-ttu-id="0e4c4-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="0e4c4-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="0e4c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4c4-103">서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-103">Gets information about a server.</span></span>

## <span data-ttu-id="0e4c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="0e4c4-104">SYNTAX</span></span>

### <span data-ttu-id="0e4c4-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="0e4c4-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0e4c4-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="0e4c4-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0e4c4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0e4c4-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0e4c4-108">목록</span><span class="sxs-lookup"><span data-stu-id="0e4c4-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0e4c4-109">설명</span><span class="sxs-lookup"><span data-stu-id="0e4c4-109">DESCRIPTION</span></span>
<span data-ttu-id="0e4c4-110">서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-110">Gets information about a server.</span></span>

## <span data-ttu-id="0e4c4-111">예제</span><span class="sxs-lookup"><span data-stu-id="0e4c4-111">EXAMPLES</span></span>

### <span data-ttu-id="0e4c4-112">예제 1: 기본 컨텍스트로 MySql 서버 얻기</span><span class="sxs-lookup"><span data-stu-id="0e4c4-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="0e4c4-113">이 cmdlet은 기본 컨텍스트가 있는 MySql 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="0e4c4-114">예제 2: 리소스 그룹 및 서버 이름으로 MySql 서버 사용</span><span class="sxs-lookup"><span data-stu-id="0e4c4-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="0e4c4-115">이 cmdlet은 리소스 그룹 및 서버 이름으로 MySql 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="0e4c4-116">예제 3: 지정된 리소스 그룹에 있는 모든 MySql 서버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="0e4c4-117">이 cmdlet은 지정된 리소스 그룹에 있는 모든 MySql 서버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="0e4c4-118">예제 4: ID로 MySql 서버 사용</span><span class="sxs-lookup"><span data-stu-id="0e4c4-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="0e4c4-119">이 cmdlet 목록은 ID로 MySql 서버를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="0e4c4-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0e4c4-120">PARAMETERS</span></span>

### <span data-ttu-id="0e4c4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e4c4-121">-DefaultProfile</span></span>
<span data-ttu-id="0e4c4-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e4c4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e4c4-123">-InputObject</span></span>
<span data-ttu-id="0e4c4-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0e4c4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0e4c4-125">-Name</span></span>
<span data-ttu-id="0e4c4-126">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-126">The name of the server.</span></span>

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

### <span data-ttu-id="0e4c4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e4c4-127">-ResourceGroupName</span></span>
<span data-ttu-id="0e4c4-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-128">The name of the resource group.</span></span>
<span data-ttu-id="0e4c4-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0e4c4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e4c4-130">-SubscriptionId</span></span>
<span data-ttu-id="0e4c4-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0e4c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4c4-132">CommonParameters</span></span>
<span data-ttu-id="0e4c4-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4c4-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e4c4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4c4-135">입력</span><span class="sxs-lookup"><span data-stu-id="0e4c4-135">INPUTS</span></span>

### <span data-ttu-id="0e4c4-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0e4c4-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0e4c4-137">출력</span><span class="sxs-lookup"><span data-stu-id="0e4c4-137">OUTPUTS</span></span>

### <span data-ttu-id="0e4c4-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="0e4c4-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="0e4c4-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0e4c4-139">NOTES</span></span>

<span data-ttu-id="0e4c4-140">별칭</span><span class="sxs-lookup"><span data-stu-id="0e4c4-140">ALIASES</span></span>

<span data-ttu-id="0e4c4-141">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0e4c4-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0e4c4-142">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e4c4-143">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0e4c4-144">INPUTOBJECT <IMySqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0e4c4-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0e4c4-145">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0e4c4-146">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0e4c4-147">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0e4c4-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="0e4c4-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0e4c4-149">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="0e4c4-150">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0e4c4-151">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0e4c4-152">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="0e4c4-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0e4c4-154">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0e4c4-155">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0e4c4-156">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0e4c4-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e4c4-157">RELATED LINKS</span></span>

