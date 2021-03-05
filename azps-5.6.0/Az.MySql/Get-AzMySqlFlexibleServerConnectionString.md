---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: a1f5c89b33ad4d547907bd63427a45ef262518c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011952"
---
# <span data-ttu-id="7f65b-101">Get-AzMySqlFlexibleServerConnectionString</span><span class="sxs-lookup"><span data-stu-id="7f65b-101">Get-AzMySqlFlexibleServerConnectionString</span></span>

## <span data-ttu-id="7f65b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f65b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f65b-103">클라이언트 연결 공급자에 따라 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="7f65b-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f65b-104">SYNTAX</span></span>

### <span data-ttu-id="7f65b-105">Get(기본값)</span><span class="sxs-lookup"><span data-stu-id="7f65b-105">Get (Default)</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7f65b-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7f65b-106">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7f65b-107">설명</span><span class="sxs-lookup"><span data-stu-id="7f65b-107">DESCRIPTION</span></span>
<span data-ttu-id="7f65b-108">클라이언트 연결 공급자에 따라 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="7f65b-109">예제</span><span class="sxs-lookup"><span data-stu-id="7f65b-109">EXAMPLES</span></span>

### <span data-ttu-id="7f65b-110">예제 1: 이름에 따라 연결 문자열을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-110">Example 1: Get connection string by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

<span data-ttu-id="7f65b-111">이 cmdlet은 서버 이름으로 클라이언트의 연결 문자열을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-111">This cmdlet shows connection string of a client by server name.</span></span>

### <span data-ttu-id="7f65b-112">예제 2: ID로 MySql 서버 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="7f65b-113">이 cmdlet은 ID에 따라 MySql 서버 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="7f65b-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f65b-114">PARAMETERS</span></span>

### <span data-ttu-id="7f65b-115">-Client</span><span class="sxs-lookup"><span data-stu-id="7f65b-115">-Client</span></span>
<span data-ttu-id="7f65b-116">클라이언트 연결 공급자입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-116">Client connection provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f65b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f65b-117">-DefaultProfile</span></span>
<span data-ttu-id="7f65b-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f65b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f65b-119">-InputObject</span></span>
<span data-ttu-id="7f65b-120">연결 문자열의 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-120">The server for the connection string.</span></span>
<span data-ttu-id="7f65b-121">생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7f65b-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7f65b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7f65b-122">-Name</span></span>
<span data-ttu-id="7f65b-123">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-123">The name of the server.</span></span>

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

### <span data-ttu-id="7f65b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f65b-124">-ResourceGroupName</span></span>
<span data-ttu-id="7f65b-125">리소스를 포함하는 리소스 그룹의 이름, Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f65b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f65b-126">-SubscriptionId</span></span>
<span data-ttu-id="7f65b-127">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f65b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f65b-128">CommonParameters</span></span>
<span data-ttu-id="7f65b-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f65b-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f65b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f65b-131">입력</span><span class="sxs-lookup"><span data-stu-id="7f65b-131">INPUTS</span></span>

### <span data-ttu-id="7f65b-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7f65b-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="7f65b-133">출력</span><span class="sxs-lookup"><span data-stu-id="7f65b-133">OUTPUTS</span></span>

### <span data-ttu-id="7f65b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7f65b-134">System.String</span></span>

## <span data-ttu-id="7f65b-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f65b-135">NOTES</span></span>

<span data-ttu-id="7f65b-136">별칭</span><span class="sxs-lookup"><span data-stu-id="7f65b-136">ALIASES</span></span>

<span data-ttu-id="7f65b-137">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7f65b-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7f65b-138">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f65b-139">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f65b-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7f65b-140">INPUTOBJECT <IMySqlIdentity> : 연결 문자열의 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-140">INPUTOBJECT <IMySqlIdentity>: The server for the connection string.</span></span>
  - <span data-ttu-id="7f65b-141">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-141">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7f65b-142">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-142">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7f65b-143">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-143">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7f65b-144">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="7f65b-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7f65b-145">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-145">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="7f65b-146">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7f65b-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7f65b-148">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="7f65b-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7f65b-150">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7f65b-151">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7f65b-152">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f65b-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7f65b-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f65b-153">RELATED LINKS</span></span>

