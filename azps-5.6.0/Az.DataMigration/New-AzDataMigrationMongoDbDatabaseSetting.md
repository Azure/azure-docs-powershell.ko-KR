---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: cf034b01d0cc7bd707d65cb2ddd90e9567003861
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983147"
---
# <span data-ttu-id="bfff9-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="bfff9-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="bfff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfff9-102">SYNOPSIS</span></span>
<span data-ttu-id="bfff9-103">mongoDb 마이그레이션에 대한 마이그레이션에 대한 데이터베이스 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="bfff9-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfff9-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="bfff9-105">설명</span><span class="sxs-lookup"><span data-stu-id="bfff9-105">DESCRIPTION</span></span>
<span data-ttu-id="bfff9-106">New-AzDataMigrationMongoDbDatabaseSetting cmdlet은 처리 시간 및 삭제 동작을 지정하는 마이그레이션 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="bfff9-107">출력은 컬렉션의 이름과 설정 값의 키 값 쌍으로 마이그레이션 작업을 호출하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="bfff9-108">예제</span><span class="sxs-lookup"><span data-stu-id="bfff9-108">EXAMPLES</span></span>

### <span data-ttu-id="bfff9-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="bfff9-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="bfff9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bfff9-110">PARAMETERS</span></span>

### <span data-ttu-id="bfff9-111">-Name</span><span class="sxs-lookup"><span data-stu-id="bfff9-111">-Name</span></span>
<span data-ttu-id="bfff9-112">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="bfff9-112">Name of the database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="bfff9-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="bfff9-113">-TargetRequestUnit</span></span>
<span data-ttu-id="bfff9-114">전용 데이터베이스 수준 요청 단위 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="bfff9-115">설정하지 않은 경우 해당 컬렉션은 공유 데이터베이스 RU를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-115">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfff9-116">-Collections</span><span class="sxs-lookup"><span data-stu-id="bfff9-116">-Collections</span></span>
<span data-ttu-id="bfff9-117">호출에서 반환된 MongoDb 컬렉션 설정 개체의 New-AzureRmDmsMongoDbDatabaseSetting 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfff9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfff9-118">CommonParameters</span></span>
<span data-ttu-id="bfff9-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfff9-120">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bfff9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfff9-121">입력</span><span class="sxs-lookup"><span data-stu-id="bfff9-121">INPUTS</span></span>

### <span data-ttu-id="bfff9-122">없음</span><span class="sxs-lookup"><span data-stu-id="bfff9-122">None</span></span>

## <span data-ttu-id="bfff9-123">출력</span><span class="sxs-lookup"><span data-stu-id="bfff9-123">OUTPUTS</span></span>

### <span data-ttu-id="bfff9-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="bfff9-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="bfff9-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfff9-125">NOTES</span></span>

## <span data-ttu-id="bfff9-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfff9-126">RELATED LINKS</span></span>
