---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
ms.openlocfilehash: d8303dadef33944addf63323e57727ef85acce6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702110"
---
# <span data-ttu-id="6a8b8-101">New-AzureRmDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="6a8b8-101">New-AzureRmDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="6a8b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8b8-103">마이그레이션에 대 한 원본 및 대상 데이터베이스에 대 한 정보가 포함 된 데이터베이스 입력 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a8b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a8b8-104">SYNTAX</span></span>

### <span data-ttu-id="6a8b8-105">MigrateSqlServerSqlDb (기본값)</span><span class="sxs-lookup"><span data-stu-id="6a8b8-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a8b8-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="6a8b8-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a8b8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6a8b8-107">DESCRIPTION</span></span>
<span data-ttu-id="6a8b8-108">New-AzureRmDataMigrationSelectedDB cmdlet은 원본 및 대상 데이터베이스에 대 한 정보 및 테이블 매핑과 마이그레이션에 대 한 정보가 포함 된 데이터베이스 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-108">The New-AzureRmDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="6a8b8-109">이 cmdlet은 New-AzureRmDataMigrationTask cmdlet을 사용 하 여 매개 변수로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-109">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="6a8b8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6a8b8-110">EXAMPLES</span></span>

### <span data-ttu-id="6a8b8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a8b8-111">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```


### <span data-ttu-id="6a8b8-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="6a8b8-112">Example 2</span></span>
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```


## <span data-ttu-id="6a8b8-113">변수</span><span class="sxs-lookup"><span data-stu-id="6a8b8-113">PARAMETERS</span></span>

### <span data-ttu-id="6a8b8-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="6a8b8-114">-BackupFileShare</span></span>
<span data-ttu-id="6a8b8-115">이 데이터베이스의 원본 서버 데이터베이스 파일을 백업할 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="6a8b8-116">이 설정을 사용 하 여 각 데이터베이스에 대 한 파일 공유 정보를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="6a8b8-117">서버에 정규화 된 도메인 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-117">Use fully qualified domain name for the server.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8b8-118">-DefaultProfile</span></span>
<span data-ttu-id="6a8b8-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8b8-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="6a8b8-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="6a8b8-121">마이그레이션하기 전에 데이터베이스를 읽기 전용으로 설정</span><span class="sxs-lookup"><span data-stu-id="6a8b8-121">Set Database to readonly before migration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8b8-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="6a8b8-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="6a8b8-123">마이그레이션 유형을 SQL Server에서 SQL DB 마이그레이션으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8b8-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="6a8b8-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="6a8b8-125">마이그레이션 유형을 SQL Server에서 SQL DB MI 마이그레이션으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8b8-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a8b8-126">-SourceDatabaseName</span></span>
<span data-ttu-id="6a8b8-127">원본 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-127">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8b8-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="6a8b8-128">-TableMap</span></span>
<span data-ttu-id="6a8b8-129">대상 테이블의 원본 매핑</span><span class="sxs-lookup"><span data-stu-id="6a8b8-129">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8b8-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a8b8-130">-TargetDatabaseName</span></span>
<span data-ttu-id="6a8b8-131">대상 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-131">The name of the target database.</span></span>

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

### <span data-ttu-id="6a8b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8b8-132">CommonParameters</span></span>
<span data-ttu-id="6a8b8-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8b8-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a8b8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8b8-135">입력</span><span class="sxs-lookup"><span data-stu-id="6a8b8-135">INPUTS</span></span>

### <span data-ttu-id="6a8b8-136">DataMigration를 통해 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="6a8b8-137">출력</span><span class="sxs-lookup"><span data-stu-id="6a8b8-137">OUTPUTS</span></span>

### <span data-ttu-id="6a8b8-138">DataMigration. MigrateSqlServerSqlDbDatabaseInput/.</span><span class="sxs-lookup"><span data-stu-id="6a8b8-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="6a8b8-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6a8b8-139">NOTES</span></span>

## <span data-ttu-id="6a8b8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a8b8-140">RELATED LINKS</span></span>
