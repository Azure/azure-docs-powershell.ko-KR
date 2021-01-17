---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: d6dda5e26603c2276210e4bf00b8b9c040568f12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359024"
---
# <span data-ttu-id="d776c-101">Get-AzMySqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="d776c-101">Get-AzMySqlConnectionString</span></span>

## <span data-ttu-id="d776c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d776c-102">SYNOPSIS</span></span>
<span data-ttu-id="d776c-103">클라이언트 연결 공급자에 따라 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="d776c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d776c-104">SYNTAX</span></span>

### <span data-ttu-id="d776c-105">Get(기본값)</span><span class="sxs-lookup"><span data-stu-id="d776c-105">Get (Default)</span></span>
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d776c-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d776c-106">GetViaIdentity</span></span>
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d776c-107">설명</span><span class="sxs-lookup"><span data-stu-id="d776c-107">DESCRIPTION</span></span>
<span data-ttu-id="d776c-108">클라이언트 연결 공급자에 따라 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="d776c-109">예제</span><span class="sxs-lookup"><span data-stu-id="d776c-109">EXAMPLES</span></span>

### <span data-ttu-id="d776c-110">예제 1: 리소스 그룹 및 서버 이름으로 MySql 서버 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-110">Example 1: Get MySql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

<span data-ttu-id="d776c-111">이 cmdlet은 리소스 그룹 및 서버 이름으로 MySql 서버 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-111">This cmdlet gets MySql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="d776c-112">예제 2: ID로 MySql 서버 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="d776c-113">이 cmdlet은 ID로 MySql 서버 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="d776c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d776c-114">PARAMETERS</span></span>

### <span data-ttu-id="d776c-115">-Client</span><span class="sxs-lookup"><span data-stu-id="d776c-115">-Client</span></span>
<span data-ttu-id="d776c-116">클라이언트 연결 공급자.</span><span class="sxs-lookup"><span data-stu-id="d776c-116">Client connection provider.</span></span>

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

### <span data-ttu-id="d776c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d776c-117">-DefaultProfile</span></span>
<span data-ttu-id="d776c-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d776c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d776c-119">-InputObject</span></span>
<span data-ttu-id="d776c-120">복제본을 만들 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-120">The source server object to create replica from.</span></span>
<span data-ttu-id="d776c-121">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d776c-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d776c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d776c-122">-Name</span></span>
<span data-ttu-id="d776c-123">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-123">The name of the server.</span></span>

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

### <span data-ttu-id="d776c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d776c-124">-ResourceGroupName</span></span>
<span data-ttu-id="d776c-125">리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d776c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d776c-126">-SubscriptionId</span></span>
<span data-ttu-id="d776c-127">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d776c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d776c-128">CommonParameters</span></span>
<span data-ttu-id="d776c-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d776c-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d776c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d776c-131">입력</span><span class="sxs-lookup"><span data-stu-id="d776c-131">INPUTS</span></span>

### <span data-ttu-id="d776c-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="d776c-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="d776c-133">출력</span><span class="sxs-lookup"><span data-stu-id="d776c-133">OUTPUTS</span></span>

### <span data-ttu-id="d776c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d776c-134">System.String</span></span>

## <span data-ttu-id="d776c-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d776c-135">NOTES</span></span>

<span data-ttu-id="d776c-136">별칭</span><span class="sxs-lookup"><span data-stu-id="d776c-136">ALIASES</span></span>

<span data-ttu-id="d776c-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d776c-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d776c-138">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d776c-139">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d776c-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d776c-140">INPUTOBJECT: 복제본을 만들 <IServer> 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="d776c-141">`Location <String>`: 리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="d776c-141">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="d776c-142">`SkuName <String>`: SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="d776c-142">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="d776c-143">`[Tag <ITrackedResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-143">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="d776c-144">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-144">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d776c-145">`[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-145">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="d776c-146">서버를 만들 때만 지정할 수 있습니다(생성에 필요).</span><span class="sxs-lookup"><span data-stu-id="d776c-146">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="d776c-147">`[EarliestRestoreDate <DateTime?>]`: 가장 빠른 복원 지점 생성 시간(ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="d776c-147">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="d776c-148">`[FullyQualifiedDomainName <String>]`: 서버의 정식 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-148">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="d776c-149">`[IdentityType <IdentityType?>]`: ID 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-149">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="d776c-150">리소스에 대한 Azure Active Directory 주체를 자동으로 만들고 할당하기 위해 이를 'SystemAssigned'로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="d776c-150">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="d776c-151">`[InfrastructureEncryption <InfrastructureEncryption?>]`: 서버가 인프라 암호화를 사용할 수 있는지 여부를 보여주는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-151">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="d776c-152">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-152">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="d776c-153">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: 서버에 최소 Tls 버전을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-153">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="d776c-154">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: 이 서버에 대해 공용 네트워크 액세스가 허용되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-154">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="d776c-155">값은 선택 사항이지만 전달된 경우 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-155">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="d776c-156">`[ReplicaCapacity <Int32?>]`: 마스터 서버가 사용할 수 있는 최대 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-156">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="d776c-157">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-157">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="d776c-158">`[SkuCapacity <Int32?>]`: 서버의 컴퓨팅 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-158">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="d776c-159">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-159">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="d776c-160">`[SkuSize <String>]`: 리소스에서 적절하게 해석할 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="d776c-161">`[SkuTier <SkuTier?>]`: 특정 SKU의 계층(예: 기본)</span><span class="sxs-lookup"><span data-stu-id="d776c-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="d776c-162">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="d776c-163">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="d776c-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 지역 중복 사용 또는 사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d776c-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="d776c-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d776c-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="d776c-166">`[StorageProfileStorageMb <Int32?>]`: 서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="d776c-167">`[UserVisibleState <ServerState?>]`: 사용자에게 표시되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="d776c-168">`[Version <ServerVersion?>]`: 서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="d776c-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="d776c-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d776c-169">RELATED LINKS</span></span>

