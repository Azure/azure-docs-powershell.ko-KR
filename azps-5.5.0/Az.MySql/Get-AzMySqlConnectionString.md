---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConnectionString.md
ms.openlocfilehash: 65eb0d924391e6e12b3b81ac487b746e1b91fa94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192156"
---
# Get-AzMySqlConnectionString

## SYNOPSIS
클라이언트 연결 공급자에 따라 연결 문자열을 얻습니다.

## 구문

### Get(기본값)
```
Get-AzMySqlConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## 설명
클라이언트 연결 공급자에 따라 연결 문자열을 얻습니다.

## 예제

### 예제 1: 리소스 그룹 및 서버 이름으로 MySql 서버 연결 문자열을 얻습니다.
```powershell
PS C:\> Get-AzMySqlConnectionString -Client ADO.NET -Name mysql-test -ResourceGroupName PowershellMySqlTest

Server=mysql-test.mysql.database.azure.com; Port=3306; Database={your_database}; Uid=mysql_test@mysql-test; Pwd={your_password};
```

이 cmdlet은 리소스 그룹 및 서버 이름으로 MySql 서버 연결 문자열을 얻습니다.

### 예제 2: ID로 MySql 서버 연결 문자열을 얻습니다.
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test@mysql-test", {your_password}, {your_database}, 3306);
```

이 cmdlet은 ID로 MySql 서버 연결 문자열을 얻습니다.

## PARAMETERS

### -Client
클라이언트 연결 공급자.

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

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -InputObject
연결 문자열에 대한 서버입니다.
생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

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

### -Name
서버의 이름입니다.

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

### -ResourceGroupName
리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.

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

### -SubscriptionId
Azure 구독을 식별하는 구독 ID입니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer

## 출력

### System.String

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


INPUTOBJECT: <IServer> 연결 문자열에 대한 서버입니다.
  - `Location <String>`: 리소스가 있는 지리적 위치
  - `[Tag <ITrackedResourceTags>]`: 리소스 태그입니다.
    - `[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.
  - `[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다. 서버를 만들 때만 지정할 수 있습니다(생성에 필요).
  - `[EarliestRestoreDate <DateTime?>]`: 가장 빠른 복원 지점 생성 시간(ISO8601 형식)
  - `[FullyQualifiedDomainName <String>]`: 서버의 정식 도메인 이름입니다.
  - `[IdentityType <IdentityType?>]`: ID 유형입니다. 리소스에 대한 Azure Active Directory 주체를 자동으로 만들고 할당하기 위해 이를 'SystemAssigned'로 설정하세요.
  - `[InfrastructureEncryption <InfrastructureEncryption?>]`: 서버가 인프라 암호화를 사용할 수 있는지 여부를 보여주는 상태입니다.
  - `[MasterServerId <String>]`: 복제본 서버의 마스터 서버 ID입니다.
  - `[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: 서버에 최소 Tls 버전을 적용합니다.
  - `[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: 이 서버에 대해 공용 네트워크 액세스가 허용되는지 여부입니다. 값은 선택 사항이지만 전달된 경우 'Enabled' 또는 'Disabled'입니다.
  - `[ReplicaCapacity <Int32?>]`: 마스터 서버가 사용할 수 있는 최대 복제본 수입니다.
  - `[ReplicationRole <String>]`: 서버의 복제 역할입니다.
  - `[SkuCapacity <Int32?>]`: 서버의 컴퓨팅 단위를 나타내는 확장/확장 용량입니다.
  - `[SkuFamily <String>]`: 하드웨어의 패밀리입니다.
  - `[SkuName <String>]`: SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.
  - `[SkuSize <String>]`: 리소스에서 적절하게 해석할 크기 코드입니다.
  - `[SkuTier <SkuTier?>]`: 특정 SKU의 계층(예: 기본)
  - `[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 설정하지 않습니다.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대한 백업 보존 기간입니다.
  - `[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 지역 중복 사용 또는 사용 안 하도록 설정
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용하도록 설정
  - `[StorageProfileStorageMb <Int32?>]`: 서버에 허용되는 최대 저장소입니다.
  - `[UserVisibleState <ServerState?>]`: 사용자에게 표시되는 서버의 상태입니다.
  - `[Version <ServerVersion?>]`: 서버 버전입니다.

## 관련 링크

