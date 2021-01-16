---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbConnectionString.md
ms.openlocfilehash: 1a6e96a8b8e030628655bdf95c58b726341dd2cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324155"
---
# <span data-ttu-id="d1aa8-101">Get-AzMariaDbConnectionString</span><span class="sxs-lookup"><span data-stu-id="d1aa8-101">Get-AzMariaDbConnectionString</span></span>

## <span data-ttu-id="d1aa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="d1aa8-103">주어진 프레임워크에서 MariaDB의 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-103">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="d1aa8-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1aa8-104">SYNTAX</span></span>

### <span data-ttu-id="d1aa8-105">ServerName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d1aa8-105">ServerName (Default)</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d1aa8-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="d1aa8-106">ServerObject</span></span>
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1aa8-107">설명</span><span class="sxs-lookup"><span data-stu-id="d1aa8-107">DESCRIPTION</span></span>
<span data-ttu-id="d1aa8-108">주어진 프레임워크에서 MariaDB의 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-108">Get connection string of a MariaDB under a given framework.</span></span>

## <span data-ttu-id="d1aa8-109">예제</span><span class="sxs-lookup"><span data-stu-id="d1aa8-109">EXAMPLES</span></span>

### <span data-ttu-id="d1aa8-110">예제 1: MariaDB의 연결 문자열을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-110">Example 1: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

<span data-ttu-id="d1aa8-111">이 명령은 MariaDB의 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-111">This command gets a connection string of MariaDB.</span></span>

### <span data-ttu-id="d1aa8-112">예제 2: MariaDB의 연결 문자열을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-112">Example 2: Get a connection string of MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="d1aa8-113">이 명령은 MariaDB의 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-113">This command gets a connection string of MariaDB.</span></span>

## <span data-ttu-id="d1aa8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1aa8-114">PARAMETERS</span></span>

### <span data-ttu-id="d1aa8-115">-Client</span><span class="sxs-lookup"><span data-stu-id="d1aa8-115">-Client</span></span>
<span data-ttu-id="d1aa8-116">클라이언트 유형 연결</span><span class="sxs-lookup"><span data-stu-id="d1aa8-116">Connect client type</span></span>

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

### <span data-ttu-id="d1aa8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1aa8-117">-DefaultProfile</span></span>
<span data-ttu-id="d1aa8-118">region DefaultParameters Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-118">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1aa8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1aa8-119">-InputObject</span></span>
<span data-ttu-id="d1aa8-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d1aa8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d1aa8-121">-Name</span></span>
<span data-ttu-id="d1aa8-122">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-122">The name of the server.</span></span>

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

### <span data-ttu-id="d1aa8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1aa8-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1aa8-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-124">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="d1aa8-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1aa8-125">-SubscriptionId</span></span>
<span data-ttu-id="d1aa8-126">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-126">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="d1aa8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1aa8-127">CommonParameters</span></span>
<span data-ttu-id="d1aa8-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1aa8-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1aa8-130">입력</span><span class="sxs-lookup"><span data-stu-id="d1aa8-130">INPUTS</span></span>

### <span data-ttu-id="d1aa8-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="d1aa8-131">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="d1aa8-132">출력</span><span class="sxs-lookup"><span data-stu-id="d1aa8-132">OUTPUTS</span></span>

### <span data-ttu-id="d1aa8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d1aa8-133">System.String</span></span>

## <span data-ttu-id="d1aa8-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1aa8-134">NOTES</span></span>

<span data-ttu-id="d1aa8-135">별칭</span><span class="sxs-lookup"><span data-stu-id="d1aa8-135">ALIASES</span></span>

<span data-ttu-id="d1aa8-136">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d1aa8-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1aa8-137">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1aa8-138">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1aa8-139">INPUTOBJECT: <IServer> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1aa8-139">INPUTOBJECT <IServer>: Identity Parameter</span></span>
  - <span data-ttu-id="d1aa8-140">`Location <String>`: 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-140">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="d1aa8-141">`[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-141">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="d1aa8-142">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-142">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d1aa8-143">`[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-143">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="d1aa8-144">서버를 만들 때만 지정할 수 있습니다(생성에 필요).</span><span class="sxs-lookup"><span data-stu-id="d1aa8-144">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="d1aa8-145">`[EarliestRestoreDate <DateTime?>]`: 가장 빠른 복원 지점 생성 시간(ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="d1aa8-145">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="d1aa8-146">`[FullyQualifiedDomainName <String>]`: 서버의 정식 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-146">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="d1aa8-147">`[IdentityType <IdentityType?>]`: ID 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-147">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="d1aa8-148">리소스에 대한 Azure Active Directory 주체를 자동으로 만들고 할당하기 위해 이를 'SystemAssigned'로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-148">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="d1aa8-149">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-149">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="d1aa8-150">`[ReplicaCapacity <Int32?>]`: 마스터 서버가 사용할 수 있는 최대 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-150">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="d1aa8-151">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-151">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="d1aa8-152">`[SkuCapacity <Int32?>]`: 서버의 컴퓨팅 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-152">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="d1aa8-153">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-153">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="d1aa8-154">`[SkuName <String>]`: SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-154">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="d1aa8-155">`[SkuSize <String>]`: 리소스에서 적절하게 해석할 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-155">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="d1aa8-156">`[SkuTier <SkuTier?>]`: 특정 SKU의 계층(예: 기본)</span><span class="sxs-lookup"><span data-stu-id="d1aa8-156">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="d1aa8-157">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-157">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="d1aa8-158">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-158">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="d1aa8-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 지역 중복 사용 또는 사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d1aa8-159">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="d1aa8-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d1aa8-160">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="d1aa8-161">`[StorageProfileStorageMb <Int32?>]`: 서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-161">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="d1aa8-162">`[UserVisibleState <ServerState?>]`: 사용자에게 표시되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-162">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="d1aa8-163">`[Version <ServerVersion?>]`: 서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="d1aa8-163">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="d1aa8-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1aa8-164">RELATED LINKS</span></span>

