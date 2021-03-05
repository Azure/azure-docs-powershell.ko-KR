---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 4d4581d78b2e1f90ce334fda77107058f2294f50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995456"
---
# <span data-ttu-id="16559-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="16559-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="16559-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16559-102">SYNOPSIS</span></span>
<span data-ttu-id="16559-103">새 MySQL 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16559-103">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="16559-104">구문</span><span class="sxs-lookup"><span data-stu-id="16559-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-HighAvailability <Object>] [-Location <String>] [-PublicAccess <String>] [-Sku <String>]
 [-SkuTier <String>] [-StorageInMb <Int32>] [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>]
 [-Version <ServerVersion>] [-Vnet <String>] [-VnetPrefix <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16559-105">설명</span><span class="sxs-lookup"><span data-stu-id="16559-105">DESCRIPTION</span></span>
<span data-ttu-id="16559-106">새 MySQL 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16559-106">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="16559-107">예제</span><span class="sxs-lookup"><span data-stu-id="16559-107">EXAMPLES</span></span>

### <span data-ttu-id="16559-108">예제 1: 인수를 사용하여 새 MySql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="16559-108">Example 1: Create a new MySql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellMySqlTest ...
Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group MySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```



### <span data-ttu-id="16559-109">예제 2: 기본 설정을 사용하여 새 MySql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="16559-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="16559-110">이 cmdlet은 기본 매개 변수 값을 사용하여 MySql 유연한 서버를 만들고 새 가상 네트워크 내에서 서버를 프로비전하고 서브넷을 서버에 위임합니다.</span><span class="sxs-lookup"><span data-stu-id="16559-110">This cmdlet creates MySql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="16559-111">위치의 기본값은 미국 서부 2, Sku는 Standard_B1ms, Sku 계층은 Burstable, 저장소 크기는 10GiB입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>


<span data-ttu-id="16559-112">서버에 대해 자동 생성된 암호를 찾으시고 싶으면 이 암호를 ConvertFrom-SecureString 'SecuredPassword' 속성을 일반 텍스트로 변환합니다.</span><span class="sxs-lookup"><span data-stu-id="16559-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>

<span data-ttu-id="16559-113">(예: $server. SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span><span class="sxs-lookup"><span data-stu-id="16559-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="16559-114">예제 3: 가상 네트워크를 사용하여 새 MySql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="16559-114">Example 3: Create a new MySql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzMySqlFlexibleServer  -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

Resource group PowershellMySqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellMySqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellMySqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="16559-115">이 cmdlet은 사용자가 제공하는 vnet ID 또는 vnet 이름으로 MySql 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16559-115">This cmdlet creates MySql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="16559-116">가상 네트워크가 없는 경우 cmdlet에서 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16559-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="16559-117">예제 4: 가상 네트워크 및 서브넷 이름을 사용하여 새 MySql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="16559-117">Example 4: Create a new MySql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Vnet mysql-vnet -Subnet mysql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellMySqlTest exists ? : True
Creating new vnet mysql-vnet in resource group PowershellMySqlTest
Creating new subnet mysql-subnet in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="16559-118">이 cmdlet은 vnet 이름, 서브넷 이름, vnet 연결선 및 서브넷 연결부가 있는 MySql 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16559-118">This cmdlet creates MySql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="16559-119">가상 네트워크 및 서브넷이 없는 경우 cmdlet에서 가상 네트워크와 서브넷을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16559-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="16559-120">예제 7: 모든 IP에 대한 공용 액세스가 있는 새 MySql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="16559-120">Example 7: Create a new MySql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess All

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="16559-121">이 cmdlet은 모든 IP 주소에 대해 MySql 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16559-121">This cmdlet creates MySql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="16559-122">예제 8: 방화벽을 사용하여 새 MySql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="16559-122">Example 8: Create a new MySql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="16559-123">이 cmdlet은 지정된 IP 주소에 대해 MySql 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16559-123">This cmdlet creates MySql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="16559-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="16559-124">PARAMETERS</span></span>

### <span data-ttu-id="16559-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="16559-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="16559-126">관리자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-126">The password of the administrator.</span></span>
<span data-ttu-id="16559-127">최소 8자, 최대 128자</span><span class="sxs-lookup"><span data-stu-id="16559-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="16559-128">암호에는 영어 대문자, 영어 소문자, 숫자 및 영자 문자가 아닌 세 가지 범주의 문자가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16559-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="16559-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="16559-129">-AdministratorUserName</span></span>
<span data-ttu-id="16559-130">서버에 대한 관리자 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-130">Administrator username for the server.</span></span>
<span data-ttu-id="16559-131">설정하면 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="16559-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="16559-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16559-132">-AsJob</span></span>
<span data-ttu-id="16559-133">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="16559-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="16559-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="16559-134">-BackupRetentionDay</span></span>
<span data-ttu-id="16559-135">서버에 대한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-135">Backup retention days for the server.</span></span>
<span data-ttu-id="16559-136">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="16559-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16559-137">-DefaultProfile</span></span>
<span data-ttu-id="16559-138">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16559-139">-HighAvailability</span><span class="sxs-lookup"><span data-stu-id="16559-139">-HighAvailability</span></span>
<span data-ttu-id="16559-140">고가용성 기능을 사용하도록 설정하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="16559-140">Enable or disable high availability feature.</span></span>
<span data-ttu-id="16559-141">기본값은 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16559-141">Default value is Disabled.</span></span>
<span data-ttu-id="16559-142">기본값: 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16559-142">Default: Disabled.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16559-143">-Location</span><span class="sxs-lookup"><span data-stu-id="16559-143">-Location</span></span>
<span data-ttu-id="16559-144">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-144">The location the resource resides in.</span></span>

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

### <span data-ttu-id="16559-145">-Name</span><span class="sxs-lookup"><span data-stu-id="16559-145">-Name</span></span>
<span data-ttu-id="16559-146">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-146">The name of the server.</span></span>

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

### <span data-ttu-id="16559-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="16559-147">-NoWait</span></span>
<span data-ttu-id="16559-148">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="16559-148">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="16559-149">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="16559-149">-PublicAccess</span></span>
<span data-ttu-id="16559-150">공용 액세스를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="16559-150">Determines the public access.</span></span>
<span data-ttu-id="16559-151">허용되는 IP 목록에 포함될 단일 또는 범위의 IP 주소를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="16559-151">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="16559-152">IP 주소 범위는 대시로 구분되어야 합니다. 공백이 포함되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16559-152">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="16559-153">0.0.0.0을 지정하면 Azure 내에 배포된 모든 리소스에서 공개 액세스하여 서버에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16559-153">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="16559-154">IP 주소를 지정하면 공용 액세스 모드에서 서버를 설정하지만 방화벽 규칙을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16559-154">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="16559-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16559-155">-ResourceGroupName</span></span>
<span data-ttu-id="16559-156">리소스를 포함하는 리소스 그룹의 이름, Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16559-156">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="16559-157">-Sku</span><span class="sxs-lookup"><span data-stu-id="16559-157">-Sku</span></span>
<span data-ttu-id="16559-158">sku의 이름은 일반적으로 계층 + 패밀리 + 코어(예: Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="16559-158">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="16559-159">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="16559-159">-SkuTier</span></span>
<span data-ttu-id="16559-160">서버의 계산 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-160">Compute tier of the server.</span></span>
<span data-ttu-id="16559-161">수락된 값: Burstable, GeneralPurpose, 메모리 최적화.</span><span class="sxs-lookup"><span data-stu-id="16559-161">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="16559-162">기본값: Burstable입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-162">Default: Burstable.</span></span>

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

### <span data-ttu-id="16559-163">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="16559-163">-StorageInMb</span></span>
<span data-ttu-id="16559-164">서버에 대해 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-164">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="16559-165">-서브넷</span><span class="sxs-lookup"><span data-stu-id="16559-165">-Subnet</span></span>
<span data-ttu-id="16559-166">기존 서브넷의 이름 또는 ID 또는 만들 새 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-166">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="16559-167">서브넷은 Microsoft.DBforMySQL/flexibleServers에 위임됩니다.</span><span class="sxs-lookup"><span data-stu-id="16559-167">Please note that the subnet will be delegated to Microsoft.DBforMySQL/flexibleServers.</span></span>
<span data-ttu-id="16559-168">위임 후 이 서브넷은 다른 유형의 Azure 리소스에 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="16559-168">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="16559-169">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="16559-169">-SubnetPrefix</span></span>
<span data-ttu-id="16559-170">CIDR 형식으로 새 vnet을 만들 때 사용할 서브넷 IP 주소 연결부입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-170">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="16559-171">기본값은 10.0.0.0/24입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-171">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="16559-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16559-172">-SubscriptionId</span></span>
<span data-ttu-id="16559-173">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-173">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="16559-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="16559-174">-Tag</span></span>
<span data-ttu-id="16559-175">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-175">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="16559-176">-Version</span><span class="sxs-lookup"><span data-stu-id="16559-176">-Version</span></span>
<span data-ttu-id="16559-177">서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-177">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16559-178">-Vnet</span><span class="sxs-lookup"><span data-stu-id="16559-178">-Vnet</span></span>
<span data-ttu-id="16559-179">기존 가상 네트워크의 이름 또는 ID 또는 만들 새 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-179">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="16559-180">이름은 2~64자 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-180">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="16559-181">이름은 문자 또는 숫자로 시작하고 문자, 숫자 또는 밑면으로 끝나야 합니다. 문자, 숫자, 밑부분, 기간 또는 하이픈만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16559-181">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="16559-182">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="16559-182">-VnetPrefix</span></span>
<span data-ttu-id="16559-183">CIDR 형식으로 새 vnet을 만들 때 사용할 IP 주소 연결선입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-183">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="16559-184">기본값은 10.0.0.0/16입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-184">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="16559-185">-Zone</span><span class="sxs-lookup"><span data-stu-id="16559-185">-Zone</span></span>
<span data-ttu-id="16559-186">리소스를 프로비전할 가용성 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="16559-186">Availability zone into which to provision the resource.</span></span>

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

### <span data-ttu-id="16559-187">-확인</span><span class="sxs-lookup"><span data-stu-id="16559-187">-Confirm</span></span>
<span data-ttu-id="16559-188">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16559-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16559-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16559-189">-WhatIf</span></span>
<span data-ttu-id="16559-190">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="16559-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16559-191">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16559-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16559-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16559-192">CommonParameters</span></span>
<span data-ttu-id="16559-193">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16559-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16559-194">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16559-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16559-195">입력</span><span class="sxs-lookup"><span data-stu-id="16559-195">INPUTS</span></span>

## <span data-ttu-id="16559-196">출력</span><span class="sxs-lookup"><span data-stu-id="16559-196">OUTPUTS</span></span>

### <span data-ttu-id="16559-197">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="16559-197">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="16559-198">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16559-198">NOTES</span></span>

<span data-ttu-id="16559-199">별칭</span><span class="sxs-lookup"><span data-stu-id="16559-199">ALIASES</span></span>

## <span data-ttu-id="16559-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16559-200">RELATED LINKS</span></span>

