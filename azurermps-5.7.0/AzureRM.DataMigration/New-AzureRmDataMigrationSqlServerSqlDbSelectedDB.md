---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529848"
---
# <span data-ttu-id="e2add-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span><span class="sxs-lookup"><span data-stu-id="e2add-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span></span>

## <span data-ttu-id="e2add-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2add-102">SYNOPSIS</span></span>
<span data-ttu-id="e2add-103">마이그레이션에 대 한 원본 및 대상 데이터베이스에 대 한 정보를 포함 하는 MigrateSqlServerSqlDbDatabaseInput 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2add-103">Creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2add-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2add-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="e2add-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2add-105">DESCRIPTION</span></span>
<span data-ttu-id="e2add-106">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet은 원본 및 대상 데이터베이스에 대 한 정보 및 테이블 매핑과 마이그레이션에 대 한 정보가 포함 된 MigrateSqlServerSqlDbDatabaseInput 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2add-106">The New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="e2add-107">이 cmdlet은 New-AzureRmDataMigrationTask cmdlet을 사용 하 여 매개 변수로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2add-107">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="e2add-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e2add-108">EXAMPLES</span></span>

### <span data-ttu-id="e2add-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2add-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

<span data-ttu-id="e2add-110">위의 예제에서는 동일한 이름을 사용 하는 SQL Azure 데이터베이스로 **AdventureWorks2016** 데이터베이스를 마이그레이션하기 위한 MigrateSqlServerSqlDbDatabaseInput 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2add-110">The above example creates MigrateSqlServerSqlDbDatabaseInput object for migrating the **AdventureWorks2016** database to a SQL Azure database with the same name.</span></span>

## <span data-ttu-id="e2add-111">변수</span><span class="sxs-lookup"><span data-stu-id="e2add-111">PARAMETERS</span></span>

### <span data-ttu-id="e2add-112">-확인</span><span class="sxs-lookup"><span data-stu-id="e2add-112">-Confirm</span></span>
<span data-ttu-id="e2add-113">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2add-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2add-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2add-114">-DefaultProfile</span></span>
<span data-ttu-id="e2add-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2add-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2add-116">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="e2add-116">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="e2add-117">마이그레이션하기 전에 데이터베이스를 읽기 전용으로 설정</span><span class="sxs-lookup"><span data-stu-id="e2add-117">Set Database to readonly before migration</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2add-118">-이름</span><span class="sxs-lookup"><span data-stu-id="e2add-118">-Name</span></span>
<span data-ttu-id="e2add-119">데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2add-119">The name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2add-120">-TableMap</span><span class="sxs-lookup"><span data-stu-id="e2add-120">-TableMap</span></span>
<span data-ttu-id="e2add-121">대상 테이블의 원본 매핑</span><span class="sxs-lookup"><span data-stu-id="e2add-121">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2add-122">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2add-122">-TargetDatabaseName</span></span>
<span data-ttu-id="e2add-123">대상 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2add-123">The name of the target Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e2add-124">입력</span><span class="sxs-lookup"><span data-stu-id="e2add-124">INPUTS</span></span>

### <span data-ttu-id="e2add-125">않아야</span><span class="sxs-lookup"><span data-stu-id="e2add-125">None</span></span>


## <span data-ttu-id="e2add-126">출력</span><span class="sxs-lookup"><span data-stu-id="e2add-126">OUTPUTS</span></span>

### <span data-ttu-id="e2add-127">DataMigration. MigrateSqlServerSqlDbDatabaseInput/.</span><span class="sxs-lookup"><span data-stu-id="e2add-127">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>


## <span data-ttu-id="e2add-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e2add-128">NOTES</span></span>

## <span data-ttu-id="e2add-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2add-129">RELATED LINKS</span></span>


