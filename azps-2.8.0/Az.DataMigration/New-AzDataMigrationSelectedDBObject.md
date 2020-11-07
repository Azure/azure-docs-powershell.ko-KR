---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 502e64ba553f20983bd437fea40d5247cf04548f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696765"
---
# <span data-ttu-id="4615d-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="4615d-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="4615d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4615d-102">SYNOPSIS</span></span>
<span data-ttu-id="4615d-103">마이그레이션에 대 한 원본 및 대상 데이터베이스에 대 한 정보가 포함 된 데이터베이스 입력 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="4615d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4615d-104">SYNTAX</span></span>

### <span data-ttu-id="4615d-105">MigrateSqlServerSqlDb (기본값)</span><span class="sxs-lookup"><span data-stu-id="4615d-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4615d-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="4615d-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4615d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4615d-107">DESCRIPTION</span></span>
<span data-ttu-id="4615d-108">New-AzDataMigrationSelectedDB cmdlet은 원본 및 대상 데이터베이스에 대 한 정보 및 테이블 매핑과 마이그레이션에 대 한 정보가 포함 된 데이터베이스 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="4615d-109">이 cmdlet은 New-AzDataMigrationTask cmdlet을 사용 하 여 매개 변수로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="4615d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4615d-110">EXAMPLES</span></span>

### <span data-ttu-id="4615d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4615d-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="4615d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="4615d-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="4615d-113">변수</span><span class="sxs-lookup"><span data-stu-id="4615d-113">PARAMETERS</span></span>

### <span data-ttu-id="4615d-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="4615d-114">-BackupFileShare</span></span>
<span data-ttu-id="4615d-115">이 데이터베이스의 원본 서버 데이터베이스 파일을 백업할 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="4615d-116">이 설정을 사용 하 여 각 데이터베이스에 대 한 파일 공유 정보를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="4615d-117">서버에 정규화 된 도메인 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="4615d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4615d-118">-DefaultProfile</span></span>
<span data-ttu-id="4615d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4615d-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="4615d-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="4615d-121">마이그레이션하기 전에 데이터베이스를 읽기 전용으로 설정</span><span class="sxs-lookup"><span data-stu-id="4615d-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="4615d-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="4615d-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="4615d-123">마이그레이션 유형을 SQL Server에서 SQL DB 마이그레이션으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="4615d-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="4615d-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="4615d-125">마이그레이션 유형을 SQL Server에서 SQL DB MI 마이그레이션으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="4615d-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4615d-126">-SourceDatabaseName</span></span>
<span data-ttu-id="4615d-127">원본 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-127">The name of the source database.</span></span>

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

### <span data-ttu-id="4615d-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="4615d-128">-TableMap</span></span>
<span data-ttu-id="4615d-129">대상 테이블의 원본 매핑</span><span class="sxs-lookup"><span data-stu-id="4615d-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="4615d-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4615d-130">-TargetDatabaseName</span></span>
<span data-ttu-id="4615d-131">대상 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-131">The name of the target database.</span></span>

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

### <span data-ttu-id="4615d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4615d-132">CommonParameters</span></span>
<span data-ttu-id="4615d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4615d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4615d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4615d-135">입력</span><span class="sxs-lookup"><span data-stu-id="4615d-135">INPUTS</span></span>

### <span data-ttu-id="4615d-136">DataMigration를 통해 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="4615d-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="4615d-137">출력</span><span class="sxs-lookup"><span data-stu-id="4615d-137">OUTPUTS</span></span>

### <span data-ttu-id="4615d-138">DataMigration. MigrateSqlServerSqlDbDatabaseInput/.</span><span class="sxs-lookup"><span data-stu-id="4615d-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="4615d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="4615d-139">NOTES</span></span>

## <span data-ttu-id="4615d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4615d-140">RELATED LINKS</span></span>