---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: d05b6507ea8e1d5244e23ab7b8b6222848a1d088
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868458"
---
# <span data-ttu-id="3912d-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="3912d-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="3912d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3912d-102">SYNOPSIS</span></span>
<span data-ttu-id="3912d-103">MongoDb 마이그레이션의 마이그레이션에 대 한 데이터베이스 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3912d-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="3912d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3912d-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="3912d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3912d-105">DESCRIPTION</span></span>
<span data-ttu-id="3912d-106">New-AzDataMigrationMongoDbDatabaseSetting cmdlet은 처리량 및 삭제 동작을 지정 하는 마이그레이션 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3912d-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="3912d-107">출력은 마이그레이션 작업을 호출 하는 데 사용할 수 있는, 컬렉션의 이름과 설정 값이 포함 된 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="3912d-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="3912d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="3912d-108">EXAMPLES</span></span>

### <span data-ttu-id="3912d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="3912d-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="3912d-110">변수</span><span class="sxs-lookup"><span data-stu-id="3912d-110">PARAMETERS</span></span>

### <span data-ttu-id="3912d-111">-이름</span><span class="sxs-lookup"><span data-stu-id="3912d-111">-Name</span></span>
<span data-ttu-id="3912d-112">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="3912d-112">Name of the database</span></span>

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
### <span data-ttu-id="3912d-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="3912d-113">-TargetRequestUnit</span></span>
<span data-ttu-id="3912d-114">전용 데이터베이스 수준 요청 단위 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3912d-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="3912d-115">설정 하지 않은 경우 해당 컬렉션은 공유 데이터베이스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3912d-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="3912d-116">-컬렉션</span><span class="sxs-lookup"><span data-stu-id="3912d-116">-Collections</span></span>
<span data-ttu-id="3912d-117">New-AzureRmDmsMongoDbDatabaseSetting 호출에서 반환 된 MongoDb collection 설정 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="3912d-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="3912d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3912d-118">CommonParameters</span></span>
<span data-ttu-id="3912d-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3912d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3912d-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3912d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3912d-121">입력</span><span class="sxs-lookup"><span data-stu-id="3912d-121">INPUTS</span></span>

### <span data-ttu-id="3912d-122">않아야</span><span class="sxs-lookup"><span data-stu-id="3912d-122">None</span></span>

## <span data-ttu-id="3912d-123">출력</span><span class="sxs-lookup"><span data-stu-id="3912d-123">OUTPUTS</span></span>

### <span data-ttu-id="3912d-124">DataMigration. MongoDbDatabaseSetting/.</span><span class="sxs-lookup"><span data-stu-id="3912d-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="3912d-125">상속자</span><span class="sxs-lookup"><span data-stu-id="3912d-125">NOTES</span></span>

## <span data-ttu-id="3912d-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3912d-126">RELATED LINKS</span></span>
