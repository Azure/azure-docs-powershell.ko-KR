---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: c6e417ade1e411eaaa0b86f8f69ac6c17f228e91
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998046"
---
# <span data-ttu-id="f4129-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="f4129-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="f4129-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4129-102">SYNOPSIS</span></span>
<span data-ttu-id="f4129-103">마이그레이션을 위한 원본 및 대상 데이터베이스에 대한 정보가 포함된 데이터베이스 입력 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="f4129-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4129-104">SYNTAX</span></span>

### <span data-ttu-id="f4129-105">MigrateSqlServerSqlDb(기본값)</span><span class="sxs-lookup"><span data-stu-id="f4129-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4129-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="f4129-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4129-107">설명</span><span class="sxs-lookup"><span data-stu-id="f4129-107">DESCRIPTION</span></span>
<span data-ttu-id="f4129-108">New-AzDataMigrationSelectedDB cmdlet은 마이그레이션을 위한 테이블 매핑뿐만 아니라 원본 및 대상 데이터베이스에 대한 정보를 포함하는 데이터베이스 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="f4129-109">이 cmdlet은 New-AzDataMigrationTask 매개 변수로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="f4129-110">예제</span><span class="sxs-lookup"><span data-stu-id="f4129-110">EXAMPLES</span></span>

### <span data-ttu-id="f4129-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f4129-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="f4129-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="f4129-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="f4129-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f4129-113">PARAMETERS</span></span>

### <span data-ttu-id="f4129-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="f4129-114">-BackupFileShare</span></span>
<span data-ttu-id="f4129-115">이 데이터베이스에 대한 원본 서버 데이터베이스 파일을 백업해야 하는 파일 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="f4129-116">이 설정을 사용하여 각 데이터베이스에 대한 파일 공유 정보를 오버라이드합니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="f4129-117">서버에 대해 완전히 자격을 갖춘 도메인 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="f4129-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4129-118">-DefaultProfile</span></span>
<span data-ttu-id="f4129-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4129-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="f4129-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="f4129-121">마이그레이션 전에 데이터베이스를 읽기 쉽게 설정</span><span class="sxs-lookup"><span data-stu-id="f4129-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="f4129-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="f4129-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="f4129-123">마이그레이션 유형을 SQL Server DB 마이그레이션으로 SQL 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="f4129-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="f4129-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="f4129-125">마이그레이션 형식을 SQL Server DB MI 마이그레이션을 SQL 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="f4129-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4129-126">-SourceDatabaseName</span></span>
<span data-ttu-id="f4129-127">원본 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-127">The name of the source database.</span></span>

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

### <span data-ttu-id="f4129-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="f4129-128">-TableMap</span></span>
<span data-ttu-id="f4129-129">대상 테이블에 원본 매핑</span><span class="sxs-lookup"><span data-stu-id="f4129-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="f4129-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4129-130">-TargetDatabaseName</span></span>
<span data-ttu-id="f4129-131">대상 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-131">The name of the target database.</span></span>

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

### <span data-ttu-id="f4129-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4129-132">CommonParameters</span></span>
<span data-ttu-id="f4129-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4129-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4129-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f4129-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4129-135">입력</span><span class="sxs-lookup"><span data-stu-id="f4129-135">INPUTS</span></span>

### <span data-ttu-id="f4129-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="f4129-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="f4129-137">출력</span><span class="sxs-lookup"><span data-stu-id="f4129-137">OUTPUTS</span></span>

### <span data-ttu-id="f4129-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="f4129-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="f4129-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4129-139">NOTES</span></span>

## <span data-ttu-id="f4129-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4129-140">RELATED LINKS</span></span>
