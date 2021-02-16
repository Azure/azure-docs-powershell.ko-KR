---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/test-azmysqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
ms.openlocfilehash: ccb22d41ec1a4f2f2bceb711a09f7448015f9f38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194028"
---
# <span data-ttu-id="3456f-101">Test-AzMySqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="3456f-101">Test-AzMySqlFlexibleServerConnect</span></span>

## <span data-ttu-id="3456f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3456f-102">SYNOPSIS</span></span>
<span data-ttu-id="3456f-103">데이터베이스 서버에 대한 연결 테스트</span><span class="sxs-lookup"><span data-stu-id="3456f-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="3456f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3456f-104">SYNTAX</span></span>

### <span data-ttu-id="3456f-105">테스트(기본값)</span><span class="sxs-lookup"><span data-stu-id="3456f-105">Test (Default)</span></span>
```
Test-AzMySqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3456f-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="3456f-106">TestAndQuery</span></span>
```
Test-AzMySqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3456f-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3456f-107">TestViaIdentity</span></span>
```
Test-AzMySqlFlexibleServerConnect -AdministratorLoginPassword <SecureString> -InputObject <IMySqlIdentity>
 [-DatabaseName <String>] [-AdministratorUserName <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3456f-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="3456f-108">TestViaIdentityAndQuery</span></span>
```
Test-AzMySqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IMySqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3456f-109">설명</span><span class="sxs-lookup"><span data-stu-id="3456f-109">DESCRIPTION</span></span>
<span data-ttu-id="3456f-110">데이터베이스 서버에 대한 연결 테스트</span><span class="sxs-lookup"><span data-stu-id="3456f-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="3456f-111">예제</span><span class="sxs-lookup"><span data-stu-id="3456f-111">EXAMPLES</span></span>

### <span data-ttu-id="3456f-112">예제 1: 이름으로 연결 테스트</span><span class="sxs-lookup"><span data-stu-id="3456f-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

<span data-ttu-id="3456f-113">리소스 그룹 및 서버 이름으로 연결 테스트</span><span class="sxs-lookup"><span data-stu-id="3456f-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="3456f-114">예제 2: ID로 연결 테스트</span><span class="sxs-lookup"><span data-stu-id="3456f-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

<span data-ttu-id="3456f-115">ID로 연결 테스트</span><span class="sxs-lookup"><span data-stu-id="3456f-115">Test connection by the identity</span></span>

### <span data-ttu-id="3456f-116">예제 3: 이름으로 쿼리 테스트</span><span class="sxs-lookup"><span data-stu-id="3456f-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="3456f-117">리소스 그룹 및 서버 이름으로 쿼리 테스트</span><span class="sxs-lookup"><span data-stu-id="3456f-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="3456f-118">예제 4: ID로 연결 테스트</span><span class="sxs-lookup"><span data-stu-id="3456f-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="3456f-119">ID로 쿼리 테스트</span><span class="sxs-lookup"><span data-stu-id="3456f-119">Test a query by the identity</span></span>

## <span data-ttu-id="3456f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3456f-120">PARAMETERS</span></span>

### <span data-ttu-id="3456f-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3456f-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3456f-122">관리자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-122">The password of the administrator.</span></span>
<span data-ttu-id="3456f-123">최소 8자 및 최대 128자입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="3456f-124">암호는 영어 대문자, 영어 소문자, 숫자 및 영문자 이 세 가지 범주의 문자를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3456f-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="3456f-125">-AdministratorUserName</span></span>
<span data-ttu-id="3456f-126">서버에 대한 관리자 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-126">Administrator username for the server.</span></span>
<span data-ttu-id="3456f-127">설정하면 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-127">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="3456f-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3456f-128">-DatabaseName</span></span>
<span data-ttu-id="3456f-129">연결할 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-129">The database name to connect.</span></span>

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

### <span data-ttu-id="3456f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3456f-130">-DefaultProfile</span></span>
<span data-ttu-id="3456f-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3456f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3456f-132">-InputObject</span></span>
<span data-ttu-id="3456f-133">연결할 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-133">The server to connect.</span></span>
<span data-ttu-id="3456f-134">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3456f-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3456f-135">-Name</span><span class="sxs-lookup"><span data-stu-id="3456f-135">-Name</span></span>
<span data-ttu-id="3456f-136">연결할 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-136">The name of the server to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3456f-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="3456f-137">-QueryText</span></span>
<span data-ttu-id="3456f-138">테스트할 데이터베이스에 대한 쿼리</span><span class="sxs-lookup"><span data-stu-id="3456f-138">The query for the database to test</span></span>

```yaml
Type: System.String
Parameter Sets: TestAndQuery, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3456f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3456f-139">-ResourceGroupName</span></span>
<span data-ttu-id="3456f-140">리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3456f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3456f-141">CommonParameters</span></span>
<span data-ttu-id="3456f-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3456f-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3456f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3456f-144">입력</span><span class="sxs-lookup"><span data-stu-id="3456f-144">INPUTS</span></span>

### <span data-ttu-id="3456f-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3456f-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="3456f-146">출력</span><span class="sxs-lookup"><span data-stu-id="3456f-146">OUTPUTS</span></span>

### <span data-ttu-id="3456f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3456f-147">System.String</span></span>

## <span data-ttu-id="3456f-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3456f-148">NOTES</span></span>

<span data-ttu-id="3456f-149">별칭</span><span class="sxs-lookup"><span data-stu-id="3456f-149">ALIASES</span></span>

<span data-ttu-id="3456f-150">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3456f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3456f-151">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3456f-152">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3456f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3456f-153">INPUTOBJECT: <IMySqlIdentity> 연결할 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-153">INPUTOBJECT <IMySqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="3456f-154">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3456f-155">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3456f-156">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3456f-157">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="3456f-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3456f-158">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="3456f-159">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3456f-160">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3456f-161">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="3456f-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3456f-163">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3456f-164">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3456f-165">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3456f-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3456f-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3456f-166">RELATED LINKS</span></span>

