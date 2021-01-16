---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350414"
---
# <span data-ttu-id="b57fc-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="b57fc-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="b57fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b57fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b57fc-103">마이그레이션을 위한 원본 및 대상 데이터베이스에 대한 정보를 포함하는 데이터베이스 입력 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b57fc-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="b57fc-104">구문</span><span class="sxs-lookup"><span data-stu-id="b57fc-104">SYNTAX</span></span>

### <span data-ttu-id="b57fc-105">MigrateSqlServerSqlDb(기본값)</span><span class="sxs-lookup"><span data-stu-id="b57fc-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b57fc-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="b57fc-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b57fc-107">설명</span><span class="sxs-lookup"><span data-stu-id="b57fc-107">DESCRIPTION</span></span>
<span data-ttu-id="b57fc-108">New-AzDataMigrationSelectedDB cmdlet은 마이그레이션을 위한 테이블 매핑뿐만 아니라 원본 및 대상 데이터베이스에 대한 정보를 포함하는 데이터베이스 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b57fc-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="b57fc-109">이 cmdlet은 New-AzDataMigrationTask 매개 변수로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b57fc-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="b57fc-110">예제</span><span class="sxs-lookup"><span data-stu-id="b57fc-110">EXAMPLES</span></span>

### <span data-ttu-id="b57fc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b57fc-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="b57fc-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b57fc-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="b57fc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b57fc-113">PARAMETERS</span></span>

### <span data-ttu-id="b57fc-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="b57fc-114">-BackupFileShare</span></span>
<span data-ttu-id="b57fc-115">이 데이터베이스에 대한 원본 서버 데이터베이스 파일을 백업해야 하는 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="b57fc-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="b57fc-116">이 설정을 사용하여 각 데이터베이스에 대한 파일 공유 정보를 오버라이드합니다.</span><span class="sxs-lookup"><span data-stu-id="b57fc-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="b57fc-117">서버에 대해 정식 도메인 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b57fc-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="b57fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b57fc-118">-DefaultProfile</span></span>
<span data-ttu-id="b57fc-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b57fc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b57fc-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="b57fc-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="b57fc-121">마이그레이션 전에 데이터베이스를 읽기 전용으로 설정</span><span class="sxs-lookup"><span data-stu-id="b57fc-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="b57fc-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="b57fc-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="b57fc-123">마이그레이션 유형을 SQL Server DB SQL 설정</span><span class="sxs-lookup"><span data-stu-id="b57fc-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="b57fc-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="b57fc-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="b57fc-125">마이그레이션 유형을 SQL Server DB MI SQL 설정</span><span class="sxs-lookup"><span data-stu-id="b57fc-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="b57fc-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b57fc-126">-SourceDatabaseName</span></span>
<span data-ttu-id="b57fc-127">원본 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b57fc-127">The name of the source database.</span></span>

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

### <span data-ttu-id="b57fc-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="b57fc-128">-TableMap</span></span>
<span data-ttu-id="b57fc-129">대상 테이블에 원본 매핑</span><span class="sxs-lookup"><span data-stu-id="b57fc-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="b57fc-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b57fc-130">-TargetDatabaseName</span></span>
<span data-ttu-id="b57fc-131">대상 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b57fc-131">The name of the target database.</span></span>

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

### <span data-ttu-id="b57fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57fc-132">CommonParameters</span></span>
<span data-ttu-id="b57fc-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b57fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57fc-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b57fc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57fc-135">입력</span><span class="sxs-lookup"><span data-stu-id="b57fc-135">INPUTS</span></span>

### <span data-ttu-id="b57fc-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="b57fc-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="b57fc-137">출력</span><span class="sxs-lookup"><span data-stu-id="b57fc-137">OUTPUTS</span></span>

### <span data-ttu-id="b57fc-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="b57fc-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="b57fc-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b57fc-139">NOTES</span></span>

## <span data-ttu-id="b57fc-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b57fc-140">RELATED LINKS</span></span>
