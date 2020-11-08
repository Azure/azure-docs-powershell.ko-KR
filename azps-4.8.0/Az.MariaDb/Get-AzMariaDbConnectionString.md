---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056276"
---
# <span data-ttu-id="4ecc3-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="4ecc3-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="4ecc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ecc3-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecc3-103">지정 된 프레임 워크 아래에 있는 고 대의 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="4ecc3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ecc3-104">SYNTAX</span></span>

### <span data-ttu-id="4ecc3-105">ServerName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4ecc3-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4ecc3-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="4ecc3-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ecc3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4ecc3-107">DESCRIPTION</span></span>
<span data-ttu-id="4ecc3-108">지정 된 프레임 워크 아래에 있는 고 대의 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="4ecc3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4ecc3-109">EXAMPLES</span></span>

### <span data-ttu-id="4ecc3-110">예제 1: a 2의 연결 문자열 가져오기</span><span class="sxs-lookup"><span data-stu-id="4ecc3-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="4ecc3-111">이 명령은 a 2 i의 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="4ecc3-112">예제 2: a 2 i 연결 문자열 가져오기</span><span class="sxs-lookup"><span data-stu-id="4ecc3-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="4ecc3-113">이 명령은 a 2 i의 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="4ecc3-114">변수</span><span class="sxs-lookup"><span data-stu-id="4ecc3-114">PARAMETERS</span></span>

### <span data-ttu-id="4ecc3-115">-클라이언트</span><span class="sxs-lookup"><span data-stu-id="4ecc3-115">-Client</span></span>
<span data-ttu-id="4ecc3-116">클라이언트 유형 연결</span><span class="sxs-lookup"><span data-stu-id="4ecc3-116">Connect client type</span></span>

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

### <span data-ttu-id="4ecc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecc3-117">-DefaultProfile</span></span>
<span data-ttu-id="4ecc3-118">region DefaultParameters Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ecc3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ecc3-119">-InputObject</span></span>
<span data-ttu-id="4ecc3-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecc3-121">-이름</span><span class="sxs-lookup"><span data-stu-id="4ecc3-121">-Name</span></span>
<span data-ttu-id="4ecc3-122">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ecc3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ecc3-123">-ResourceGroupName</span></span>
<span data-ttu-id="4ecc3-124">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-124">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ecc3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ecc3-125">-SubscriptionId</span></span>
<span data-ttu-id="4ecc3-126">구독 ID는 모든 서비스 통화에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-126">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ecc3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecc3-127">CommonParameters</span></span>
<span data-ttu-id="4ecc3-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecc3-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecc3-130">입력</span><span class="sxs-lookup"><span data-stu-id="4ecc3-130">INPUTS</span></span>

### <span data-ttu-id="4ecc3-131">Api20180601Preview Iadb. i r i. IServer</span><span class="sxs-lookup"><span data-stu-id="4ecc3-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="4ecc3-132">출력</span><span class="sxs-lookup"><span data-stu-id="4ecc3-132">OUTPUTS</span></span>

### <span data-ttu-id="4ecc3-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4ecc3-133">System.String</span></span>

## <span data-ttu-id="4ecc3-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4ecc3-134">NOTES</span></span>

<span data-ttu-id="4ecc3-135">별칭과</span><span class="sxs-lookup"><span data-stu-id="4ecc3-135">ALIASES</span></span>

<span data-ttu-id="4ecc3-136">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4ecc3-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ecc3-137">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ecc3-138">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ecc3-139">INPUTOBJECT <IServer> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4ecc3-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="4ecc3-140">`Location <String>`: 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="4ecc3-141">`[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="4ecc3-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="4ecc3-142">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4ecc3-143">`[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="4ecc3-144">서버를 만드는 경우에만 지정할 수 있습니다 (만들기에 필요 함).</span><span class="sxs-lookup"><span data-stu-id="4ecc3-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="4ecc3-145">`[EarliestRestoreDate <DateTime?>]`: 초기 복원 시점 생성 시간 (ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="4ecc3-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="4ecc3-146">`[FullyQualifiedDomainName <String>]`: 서버의 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="4ecc3-147">`[IdentityType <IdentityType?>]`: Id 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="4ecc3-148">해당 리소스에 대 한 Azure Active Directory 보안 주체를 자동으로 만들고 할당 하려면이를 ' SystemAssigned '로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="4ecc3-149">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="4ecc3-150">`[ReplicaCapacity <Int32?>]`: 마스터 서버에 포함할 수 있는 최대 복제 데이터베이스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="4ecc3-151">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="4ecc3-152">`[SkuCapacity <Int32?>]`: 서버의 계산 단위를 나타내는 스케일 업/out 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="4ecc3-153">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="4ecc3-154">`[SkuName <String>]`: Sku의 이름 (일반적으로 계층 + 패밀리 + 코어) (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="4ecc3-155">`[SkuSize <String>]`: 리소스에 따라 적절 하 게 해석 되는 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="4ecc3-156">`[SkuTier <SkuTier?>]`: 특정 SKU (예: 기본)의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="4ecc3-157">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="4ecc3-158">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대 한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="4ecc3-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 대해 지리적 중복을 사용 하거나 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="4ecc3-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="4ecc3-161">`[StorageProfileStorageMb <Int32?>]`: 서버에 허용 된 최대 저장소.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="4ecc3-162">`[UserVisibleState <ServerState?>]`: 사용자에 게 표시 되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="4ecc3-163">`[Version <ServerVersion?>]`: 서버 버전.</span><span class="sxs-lookup"><span data-stu-id="4ecc3-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="4ecc3-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ecc3-164">RELATED LINKS</span></span>

