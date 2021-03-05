---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: 6fa95473091afe991eac90ad87d7321b8401a8be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996800"
---
# <span data-ttu-id="c8ddb-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="c8ddb-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="c8ddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ddb-103">마이그레이션 작업에 사용할 동기화 시나리오에 특정 데이터베이스 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c8ddb-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="c8ddb-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8ddb-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8ddb-105">설명</span><span class="sxs-lookup"><span data-stu-id="c8ddb-105">DESCRIPTION</span></span>

<span data-ttu-id="c8ddb-106">New-AzDataMigrationSyncSelectedDB cmdlet은 원본 및 대상 데이터베이스에 대한 정보를 포함하는 동기화 시나리오에 특정 데이터베이스 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c8ddb-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="c8ddb-107">예제</span><span class="sxs-lookup"><span data-stu-id="c8ddb-107">EXAMPLES</span></span>

### <span data-ttu-id="c8ddb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c8ddb-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="c8ddb-109">이 예제에서는 데이터베이스에 대한 마이그레이션 설정을 설명하는 데이터베이스 메타데이터 개체를 $DatabaseName $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="c8ddb-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="c8ddb-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c8ddb-110">PARAMETERS</span></span>

### <span data-ttu-id="c8ddb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ddb-111">-DefaultProfile</span></span>
<span data-ttu-id="c8ddb-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8ddb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8ddb-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="c8ddb-113">-MigrationSetting</span></span>
<span data-ttu-id="c8ddb-114">마이그레이션 동작을 조정하는 마이그레이션 설정</span><span class="sxs-lookup"><span data-stu-id="c8ddb-114">Migration settings which tune the migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8ddb-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c8ddb-115">-SchemaName</span></span>
<span data-ttu-id="c8ddb-116">마이그레이션할 Schema 이름</span><span class="sxs-lookup"><span data-stu-id="c8ddb-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="c8ddb-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8ddb-117">-SourceDatabaseName</span></span>
<span data-ttu-id="c8ddb-118">원본 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8ddb-118">The name of the source database.</span></span>

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

### <span data-ttu-id="c8ddb-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="c8ddb-119">-SourceSetting</span></span>
<span data-ttu-id="c8ddb-120">원본 엔드포인트 마이그레이션 동작을 조정하는 원본 설정</span><span class="sxs-lookup"><span data-stu-id="c8ddb-120">Source settings to tune source endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8ddb-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="c8ddb-121">-TableMap</span></span>
<span data-ttu-id="c8ddb-122">대상 테이블에 원본 매핑</span><span class="sxs-lookup"><span data-stu-id="c8ddb-122">Mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8ddb-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8ddb-123">-TargetDatabaseName</span></span>
<span data-ttu-id="c8ddb-124">대상 데이터베이스의 이름</span><span class="sxs-lookup"><span data-stu-id="c8ddb-124">The name of the target database</span></span>

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

### <span data-ttu-id="c8ddb-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="c8ddb-125">-TargetSetting</span></span>
<span data-ttu-id="c8ddb-126">대상 엔드포인트 마이그레이션 동작을 조정하는 대상 설정</span><span class="sxs-lookup"><span data-stu-id="c8ddb-126">Target settings to tune target endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8ddb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ddb-127">CommonParameters</span></span>
<span data-ttu-id="c8ddb-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c8ddb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ddb-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c8ddb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ddb-130">입력</span><span class="sxs-lookup"><span data-stu-id="c8ddb-130">INPUTS</span></span>

### <span data-ttu-id="c8ddb-131">없음</span><span class="sxs-lookup"><span data-stu-id="c8ddb-131">None</span></span>

## <span data-ttu-id="c8ddb-132">출력</span><span class="sxs-lookup"><span data-stu-id="c8ddb-132">OUTPUTS</span></span>

### <span data-ttu-id="c8ddb-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="c8ddb-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="c8ddb-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c8ddb-134">NOTES</span></span>

## <span data-ttu-id="c8ddb-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8ddb-135">RELATED LINKS</span></span>
