---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConnectionString.md
ms.openlocfilehash: 8df35a38889e2c91bd74625ae916fd10739d9db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048784"
---
# <span data-ttu-id="42c76-101">Get-AzPostgreSqlConnectionString</span><span class="sxs-lookup"><span data-stu-id="42c76-101">Get-AzPostgreSqlConnectionString</span></span>

## <span data-ttu-id="42c76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42c76-102">SYNOPSIS</span></span>
<span data-ttu-id="42c76-103">클라이언트 연결 공급자에 따라 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="42c76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42c76-104">SYNTAX</span></span>

### <span data-ttu-id="42c76-105">Get (기본값)</span><span class="sxs-lookup"><span data-stu-id="42c76-105">Get (Default)</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="42c76-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="42c76-106">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="42c76-107">설명은</span><span class="sxs-lookup"><span data-stu-id="42c76-107">DESCRIPTION</span></span>
<span data-ttu-id="42c76-108">클라이언트 연결 공급자에 따라 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="42c76-109">예제의</span><span class="sxs-lookup"><span data-stu-id="42c76-109">EXAMPLES</span></span>

### <span data-ttu-id="42c76-110">예제 1: 리소스 그룹 및 서버 이름으로 PostgreSql 서버 연결 문자열 가져오기</span><span class="sxs-lookup"><span data-stu-id="42c76-110">Example 1: Get PostgreSql server connection string by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConnectionString -Client ADO.NET -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG

Server=postgresqltestserver.postgres.database.azure.com;Database={your_database};Port=5432;User Id=pwsh@postgresqltestserver;Password={your_password};Ssl Mode=Require;
```

<span data-ttu-id="42c76-111">이 cmdlet은 리소스 그룹과 서버 이름으로 PostgreSql 서버 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-111">This cmdlet gets PostgreSql server connection string by resource group and server name.</span></span>

### <span data-ttu-id="42c76-112">예제 2: id를 기준으로 PostgreSql 서버 연결 문자열 가져오기</span><span class="sxs-lookup"><span data-stu-id="42c76-112">Example 2: Get PostgreSql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Get-AzPostgreSqlConnectionString -Client PHP

host=postgresqltestserver.postgres.database.azure.com port=5432 dbname={your_database} user=pwsh@postgresqltestserver password={your_password} sslmode=require
```

<span data-ttu-id="42c76-113">이 cmdlet은 id를 기준으로 PostgreSql 서버 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-113">This cmdlet gets PostgreSql server connection string by identity.</span></span>

## <span data-ttu-id="42c76-114">변수</span><span class="sxs-lookup"><span data-stu-id="42c76-114">PARAMETERS</span></span>

### <span data-ttu-id="42c76-115">-클라이언트</span><span class="sxs-lookup"><span data-stu-id="42c76-115">-Client</span></span>
<span data-ttu-id="42c76-116">클라이언트 연결 공급자.</span><span class="sxs-lookup"><span data-stu-id="42c76-116">Client connection provider.</span></span>

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

### <span data-ttu-id="42c76-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c76-117">-DefaultProfile</span></span>
<span data-ttu-id="42c76-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42c76-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42c76-119">-InputObject</span></span>
<span data-ttu-id="42c76-120">복제를 만들 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-120">The source server object to create replica from.</span></span>
<span data-ttu-id="42c76-121">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42c76-122">-이름</span><span class="sxs-lookup"><span data-stu-id="42c76-122">-Name</span></span>
<span data-ttu-id="42c76-123">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-123">The name of the server.</span></span>

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

### <span data-ttu-id="42c76-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c76-124">-ResourceGroupName</span></span>
<span data-ttu-id="42c76-125">리소스가 포함 된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="42c76-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42c76-126">-SubscriptionId</span></span>
<span data-ttu-id="42c76-127">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="42c76-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c76-128">CommonParameters</span></span>
<span data-ttu-id="42c76-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c76-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="42c76-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c76-131">입력</span><span class="sxs-lookup"><span data-stu-id="42c76-131">INPUTS</span></span>

### <span data-ttu-id="42c76-132">PostgreSql. Api20171201. i m m.</span><span class="sxs-lookup"><span data-stu-id="42c76-132">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="42c76-133">출력</span><span class="sxs-lookup"><span data-stu-id="42c76-133">OUTPUTS</span></span>

### <span data-ttu-id="42c76-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="42c76-134">System.String</span></span>

## <span data-ttu-id="42c76-135">상속자</span><span class="sxs-lookup"><span data-stu-id="42c76-135">NOTES</span></span>

<span data-ttu-id="42c76-136">별칭과</span><span class="sxs-lookup"><span data-stu-id="42c76-136">ALIASES</span></span>

<span data-ttu-id="42c76-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="42c76-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="42c76-138">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="42c76-139">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="42c76-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="42c76-140">INPUTOBJECT <IServer> : 복제를 만들 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-140">INPUTOBJECT <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="42c76-141">`Location <String>`: 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-141">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="42c76-142">`[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="42c76-142">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="42c76-143">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-143">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="42c76-144">`[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-144">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="42c76-145">서버를 만드는 경우에만 지정할 수 있습니다 (만들기에 필요 함).</span><span class="sxs-lookup"><span data-stu-id="42c76-145">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="42c76-146">`[EarliestRestoreDate <DateTime?>]`: 초기 복원 시점 생성 시간 (ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="42c76-146">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="42c76-147">`[FullyQualifiedDomainName <String>]`: 서버의 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-147">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="42c76-148">`[IdentityType <IdentityType?>]`: Id 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-148">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="42c76-149">해당 리소스에 대 한 Azure Active Directory 보안 주체를 자동으로 만들고 할당 하려면이를 ' SystemAssigned '로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-149">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="42c76-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: 서버에서 인프라 암호화를 사용 하는지 여부를 나타내는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-150">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="42c76-151">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 id입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-151">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="42c76-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: 서버에 대해 최소 Tls 버전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-152">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="42c76-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`:이 서버에 공용 네트워크 액세스가 허용 되는지 여부</span><span class="sxs-lookup"><span data-stu-id="42c76-153">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="42c76-154">값은 선택 사항 이지만, 전달 되는 경우에는 ' Enabled ' 또는 ' Disabled ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-154">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="42c76-155">`[ReplicaCapacity <Int32?>]`: 마스터 서버에 포함할 수 있는 최대 복제 데이터베이스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-155">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="42c76-156">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-156">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="42c76-157">`[SkuCapacity <Int32?>]`: 서버의 계산 단위를 나타내는 스케일 업/out 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-157">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="42c76-158">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-158">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="42c76-159">`[SkuName <String>]`: Sku의 이름 (일반적으로 계층 + 패밀리 + 코어) (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-159">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="42c76-160">`[SkuSize <String>]`: 리소스에 따라 적절 하 게 해석 되는 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-160">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="42c76-161">`[SkuTier <SkuTier?>]`: 특정 SKU (예: 기본)의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-161">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="42c76-162">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-162">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="42c76-163">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대 한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-163">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="42c76-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 대해 지리적 중복을 사용 하거나 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-164">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="42c76-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-165">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="42c76-166">`[StorageProfileStorageMb <Int32?>]`: 서버에 허용 된 최대 저장소.</span><span class="sxs-lookup"><span data-stu-id="42c76-166">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="42c76-167">`[UserVisibleState <ServerState?>]`: 사용자에 게 표시 되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="42c76-167">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="42c76-168">`[Version <ServerVersion?>]`: 서버 버전.</span><span class="sxs-lookup"><span data-stu-id="42c76-168">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="42c76-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42c76-169">RELATED LINKS</span></span>

