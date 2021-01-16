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
# Get-AzMariaDbConnectionString

## SYNOPSIS
주어진 프레임워크에서 MariaDB의 연결 문자열을 얻습니다.

## 구문

### ServerName(기본값)
```
Get-AzMariaDbConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ServerObject
```
Get-AzMariaDbConnectionString -Client <String> -InputObject <IServer> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## 설명
주어진 프레임워크에서 MariaDB의 연결 문자열을 얻습니다.

## 예제

### 예제 1: MariaDB의 연결 문자열을 확인합니다.
```powershell
PS C:\> Get-AzMariaDbConnectionString -ServerName mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0 -Client ADO.NET

Server=mariadb-asd-01.mariadb.database.azure.com; Port=3306; Database={your_database}; Uid=adminuser@mariadb-asd-01; Pwd={your_password}; SslMode=Preferred;
```

이 명령은 MariaDB의 연결 문자열을 얻습니다.

### 예제 2: MariaDB의 연결 문자열을 얻게 됩니다.
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-gp-t03 -ResourceGroupName lucas-manual-test | Get-AzMariaDbConnectionString -Client PHP

$con=mysqli_init();mysqli_ssl_set($con, NULL, NULL, {ca-cert filename}, NULL, NULL); mysqli_real_connect($con, "mariadb-gp-t03.mariadb.database.azure.com", "adminuser@mariadb-gp-t03", {your_password}, {your_database}, 3306);
```

이 명령은 MariaDB의 연결 문자열을 얻습니다.

## PARAMETERS

### -Client
클라이언트 유형 연결

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
region DefaultParameters Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

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

### -Name
서버의 이름입니다.

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

### -ResourceGroupName
리소스를 포함하는 리소스 그룹의 이름입니다.

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

### -SubscriptionId
구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer

## 출력

### System.String

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


INPUTOBJECT: <IServer> ID 매개 변수
  - `Location <String>`: 리소스가 있는 위치입니다.
  - `[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.
    - `[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.
  - `[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다. 서버를 만들 때만 지정할 수 있습니다(생성에 필요).
  - `[EarliestRestoreDate <DateTime?>]`: 가장 빠른 복원 지점 생성 시간(ISO8601 형식)
  - `[FullyQualifiedDomainName <String>]`: 서버의 정식 도메인 이름입니다.
  - `[IdentityType <IdentityType?>]`: ID 유형입니다. 리소스에 대한 Azure Active Directory 주체를 자동으로 만들고 할당하기 위해 이를 'SystemAssigned'로 설정하세요.
  - `[MasterServerId <String>]`: 복제본 서버의 마스터 서버 ID입니다.
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

