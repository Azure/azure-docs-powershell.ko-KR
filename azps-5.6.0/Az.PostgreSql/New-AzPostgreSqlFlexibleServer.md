---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: c40f8ad000bca3026860ebc328be57e6931a1546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987695"
---
# <span data-ttu-id="ee83c-101">New-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="ee83c-101">New-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="ee83c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee83c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee83c-103">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-103">Creates a new server.</span></span>

## <span data-ttu-id="ee83c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee83c-104">SYNTAX</span></span>

```
New-AzPostgreSqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-Location <String>] [-PublicAccess <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>] [-Version <ServerVersion>] [-Vnet <String>]
 [-VnetPrefix <String>] [-Zone <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ee83c-105">설명</span><span class="sxs-lookup"><span data-stu-id="ee83c-105">DESCRIPTION</span></span>
<span data-ttu-id="ee83c-106">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-106">Creates a new server.</span></span>

## <span data-ttu-id="ee83c-107">예제</span><span class="sxs-lookup"><span data-stu-id="ee83c-107">EXAMPLES</span></span>

### <span data-ttu-id="ee83c-108">예제 1: 인수를 사용하여 새 PostgreSql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="ee83c-108">Example 1: Create a new PostgreSql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest \
-Location eastus -AdministratorUserName postgresqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellPostgreSqlTest ...
Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----          -------- ------------------ ------- ----------------------- -------       -------        
postgresql-test eastus postgresqltest      12     10240                   Standard_B1ms Burstable 

```



### <span data-ttu-id="ee83c-109">예제 2: 기본 설정을 사용하여 새 PostgreSql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="ee83c-109">Example 2: Create a new PostgreSql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server server00000000 in group group00000000...
Your server postgresql-test is using sku Standard_D2s_v3 (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="ee83c-110">이 cmdlet은 기본 매개 변수 값을 사용하여 PostgreSql 유연한 서버를 만들고 새 가상 네트워크 내에서 서버를 프로비전하고 서브넷을 서버에 위임합니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-110">This cmdlet creates PostgreSql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="ee83c-111">위치의 기본값은 미국 서부 2, Sku는 Standard_D2s_v3, Sku 계층은 GeneralPurpose, 저장소 크기는 128GiB입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-111">The default values of location is West US 2, Sku is Standard_D2s_v3, Sku tier is GeneralPurpose, and storage size is 128GiB.</span></span>


<span data-ttu-id="ee83c-112">서버에 대해 자동 생성된 암호를 찾으시고 싶으면 이 암호를 ConvertFrom-SecureString 'SecuredPassword' 속성을 일반 텍스트로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>
<span data-ttu-id="ee83c-113">(예: $server. SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span><span class="sxs-lookup"><span data-stu-id="ee83c-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="ee83c-114">예제 3: 가상 네트워크를 사용하여 새 PostgreSql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="ee83c-114">Example 3: Create a new PostgreSql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer  -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

Resource group PowershellPostgreSqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellPostgreSqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server server00000000 in group PowershellPostgreSqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="ee83c-115">이 cmdlet은 사용자가 제공하는 vnet ID 또는 vnet 이름으로 PostgreSql 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-115">This cmdlet creates PostgreSql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="ee83c-116">가상 네트워크가 없는 경우 cmdlet에서 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="ee83c-117">예제 4: 가상 네트워크 및 서브넷 이름을 사용하여 새 PostgreSql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="ee83c-117">Example 4: Create a new PostgreSql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -Vnet postgresql-vnet -Subnet postgresql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellPostgreSqlTest exists ? : True
Creating new vnet postgresql-vnet in resource group PowershellPostgreSqlTest
Creating new subnet postgresql-subnet in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="ee83c-118">이 cmdlet은 Vnet 이름, 서브넷 이름, vnet 연결선 및 서브넷 연결부가 있는 PostgreSql 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-118">This cmdlet creates PostgreSql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="ee83c-119">가상 네트워크 및 서브넷이 없는 경우 cmdlet에서 가상 네트워크와 서브넷을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="ee83c-120">예제 7: 모든 IP에 대한 공용 액세스가 있는 새 PostgreSql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="ee83c-120">Example 7: Create a new PostgreSql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess All

Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="ee83c-121">이 cmdlet은 모든 IP 주소에 대해 PostgreSql 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-121">This cmdlet creates PostgreSql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="ee83c-122">예제 8: 방화벽을 사용하여 새 PostgreSql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="ee83c-122">Example 8: Create a new PostgreSql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="ee83c-123">이 cmdlet은 지정된 IP 주소에 열려 있는 PostgreSql 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-123">This cmdlet creates PostgreSql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="ee83c-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ee83c-124">PARAMETERS</span></span>

### <span data-ttu-id="ee83c-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ee83c-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ee83c-126">관리자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-126">The password of the administrator.</span></span>
<span data-ttu-id="ee83c-127">최소 8자, 최대 128자</span><span class="sxs-lookup"><span data-stu-id="ee83c-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="ee83c-128">암호에는 영어 대문자, 영어 소문자, 숫자 및 영자 문자가 아닌 세 가지 범주의 문자가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee83c-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="ee83c-129">-AdministratorUserName</span></span>
<span data-ttu-id="ee83c-130">서버에 대한 관리자 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-130">Administrator username for the server.</span></span>
<span data-ttu-id="ee83c-131">설정하면 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="ee83c-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee83c-132">-AsJob</span></span>
<span data-ttu-id="ee83c-133">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="ee83c-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="ee83c-134">-BackupRetentionDay</span></span>
<span data-ttu-id="ee83c-135">서버에 대한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-135">Backup retention days for the server.</span></span>
<span data-ttu-id="ee83c-136">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-136">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee83c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee83c-137">-DefaultProfile</span></span>
<span data-ttu-id="ee83c-138">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee83c-139">-Location</span><span class="sxs-lookup"><span data-stu-id="ee83c-139">-Location</span></span>
<span data-ttu-id="ee83c-140">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-140">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ee83c-141">-Name</span><span class="sxs-lookup"><span data-stu-id="ee83c-141">-Name</span></span>
<span data-ttu-id="ee83c-142">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-142">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee83c-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ee83c-143">-NoWait</span></span>
<span data-ttu-id="ee83c-144">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-144">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ee83c-145">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="ee83c-145">-PublicAccess</span></span>
<span data-ttu-id="ee83c-146">공용 액세스를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-146">Determines the public access.</span></span>
<span data-ttu-id="ee83c-147">허용되는 IP 목록에 포함될 단일 또는 범위의 IP 주소를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-147">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="ee83c-148">IP 주소 범위는 대시로 구분되어야 합니다. 공백이 포함되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-148">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="ee83c-149">0.0.0.0을 지정하면 Azure 내에 배포된 모든 리소스에서 공개 액세스하여 서버에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-149">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="ee83c-150">IP 주소를 지정하면 공용 액세스 모드에서 서버를 설정하지만 방화벽 규칙을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-150">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="ee83c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee83c-151">-ResourceGroupName</span></span>
<span data-ttu-id="ee83c-152">리소스를 포함하는 리소스 그룹의 이름, Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-152">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ee83c-153">-Sku</span><span class="sxs-lookup"><span data-stu-id="ee83c-153">-Sku</span></span>
<span data-ttu-id="ee83c-154">sku의 이름은 일반적으로 계층 + 패밀리 + 코어(예: Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="ee83c-154">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="ee83c-155">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ee83c-155">-SkuTier</span></span>
<span data-ttu-id="ee83c-156">서버의 계산 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-156">Compute tier of the server.</span></span>
<span data-ttu-id="ee83c-157">수락된 값: Burstable, GeneralPurpose, 메모리 최적화.</span><span class="sxs-lookup"><span data-stu-id="ee83c-157">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="ee83c-158">기본값: Burstable입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-158">Default: Burstable.</span></span>

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

### <span data-ttu-id="ee83c-159">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ee83c-159">-StorageInMb</span></span>
<span data-ttu-id="ee83c-160">서버에 대해 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-160">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee83c-161">-서브넷</span><span class="sxs-lookup"><span data-stu-id="ee83c-161">-Subnet</span></span>
<span data-ttu-id="ee83c-162">기존 서브넷의 이름 또는 ID 또는 만들 새 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-162">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="ee83c-163">서브넷은 Microsoft.DBforPostgreSQL/flexibleServers에 위임됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-163">Please note that the subnet will be delegated to Microsoft.DBforPostgreSQL/flexibleServers.</span></span>
<span data-ttu-id="ee83c-164">위임 후 이 서브넷은 다른 유형의 Azure 리소스에 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-164">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="ee83c-165">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="ee83c-165">-SubnetPrefix</span></span>
<span data-ttu-id="ee83c-166">CIDR 형식으로 새 vnet을 만들 때 사용할 서브넷 IP 주소 연결부입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-166">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="ee83c-167">기본값은 10.0.0.0/24입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-167">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="ee83c-168">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee83c-168">-SubscriptionId</span></span>
<span data-ttu-id="ee83c-169">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-169">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee83c-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee83c-170">-Tag</span></span>
<span data-ttu-id="ee83c-171">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-171">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee83c-172">-Version</span><span class="sxs-lookup"><span data-stu-id="ee83c-172">-Version</span></span>
<span data-ttu-id="ee83c-173">서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-173">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee83c-174">-Vnet</span><span class="sxs-lookup"><span data-stu-id="ee83c-174">-Vnet</span></span>
<span data-ttu-id="ee83c-175">기존 가상 네트워크의 이름 또는 ID 또는 만들 새 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-175">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="ee83c-176">이름은 2~64자 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-176">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="ee83c-177">이름은 문자 또는 숫자로 시작하고 문자, 숫자 또는 밑면으로 끝나야 합니다. 문자, 숫자, 밑부분, 기간 또는 하이픈만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-177">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="ee83c-178">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="ee83c-178">-VnetPrefix</span></span>
<span data-ttu-id="ee83c-179">CIDR 형식으로 새 vnet을 만들 때 사용할 IP 주소 연결선입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-179">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="ee83c-180">기본값은 10.0.0.0/16입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-180">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="ee83c-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="ee83c-181">-Zone</span></span>
<span data-ttu-id="ee83c-182">리소스를 프로비전할 가용성 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-182">Availability zone into which to provision the resource.</span></span>

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

### <span data-ttu-id="ee83c-183">-확인</span><span class="sxs-lookup"><span data-stu-id="ee83c-183">-Confirm</span></span>
<span data-ttu-id="ee83c-184">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee83c-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee83c-185">-WhatIf</span></span>
<span data-ttu-id="ee83c-186">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee83c-187">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee83c-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee83c-188">CommonParameters</span></span>
<span data-ttu-id="ee83c-189">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee83c-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee83c-190">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee83c-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee83c-191">입력</span><span class="sxs-lookup"><span data-stu-id="ee83c-191">INPUTS</span></span>

## <span data-ttu-id="ee83c-192">출력</span><span class="sxs-lookup"><span data-stu-id="ee83c-192">OUTPUTS</span></span>

### <span data-ttu-id="ee83c-193">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="ee83c-193">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="ee83c-194">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee83c-194">NOTES</span></span>

<span data-ttu-id="ee83c-195">별칭</span><span class="sxs-lookup"><span data-stu-id="ee83c-195">ALIASES</span></span>

## <span data-ttu-id="ee83c-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee83c-196">RELATED LINKS</span></span>

