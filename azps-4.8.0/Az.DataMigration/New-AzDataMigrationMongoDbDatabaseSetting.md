---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212819"
---
# <span data-ttu-id="f3140-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="f3140-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="f3140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3140-102">SYNOPSIS</span></span>
<span data-ttu-id="f3140-103">MongoDb 마이그레이션의 마이그레이션에 대 한 데이터베이스 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3140-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="f3140-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3140-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="f3140-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f3140-105">DESCRIPTION</span></span>
<span data-ttu-id="f3140-106">New-AzDataMigrationMongoDbDatabaseSetting cmdlet은 처리량 및 삭제 동작을 지정 하는 마이그레이션 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3140-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="f3140-107">출력은 마이그레이션 작업을 호출 하는 데 사용할 수 있는, 컬렉션의 이름과 설정 값이 포함 된 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f3140-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="f3140-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f3140-108">EXAMPLES</span></span>

### <span data-ttu-id="f3140-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3140-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="f3140-110">변수</span><span class="sxs-lookup"><span data-stu-id="f3140-110">PARAMETERS</span></span>

### <span data-ttu-id="f3140-111">-이름</span><span class="sxs-lookup"><span data-stu-id="f3140-111">-Name</span></span>
<span data-ttu-id="f3140-112">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="f3140-112">Name of the database</span></span>

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
### <span data-ttu-id="f3140-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="f3140-113">-TargetRequestUnit</span></span>
<span data-ttu-id="f3140-114">전용 데이터베이스 수준 요청 단위 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f3140-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="f3140-115">설정 하지 않은 경우 해당 컬렉션은 공유 데이터베이스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3140-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="f3140-116">-컬렉션</span><span class="sxs-lookup"><span data-stu-id="f3140-116">-Collections</span></span>
<span data-ttu-id="f3140-117">New-AzureRmDmsMongoDbDatabaseSetting 호출에서 반환 된 MongoDb collection 설정 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f3140-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="f3140-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3140-118">CommonParameters</span></span>
<span data-ttu-id="f3140-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3140-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3140-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3140-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3140-121">입력</span><span class="sxs-lookup"><span data-stu-id="f3140-121">INPUTS</span></span>

### <span data-ttu-id="f3140-122">않아야</span><span class="sxs-lookup"><span data-stu-id="f3140-122">None</span></span>

## <span data-ttu-id="f3140-123">출력</span><span class="sxs-lookup"><span data-stu-id="f3140-123">OUTPUTS</span></span>

### <span data-ttu-id="f3140-124">DataMigration. MongoDbDatabaseSetting/.</span><span class="sxs-lookup"><span data-stu-id="f3140-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="f3140-125">상속자</span><span class="sxs-lookup"><span data-stu-id="f3140-125">NOTES</span></span>

## <span data-ttu-id="f3140-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3140-126">RELATED LINKS</span></span>
