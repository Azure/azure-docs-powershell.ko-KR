---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877577"
---
# <span data-ttu-id="b8685-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="b8685-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="b8685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8685-102">SYNOPSIS</span></span>
<span data-ttu-id="b8685-103">MongoDb 마이그레이션에 따라 마이그레이션에 대 한 컬렉션 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="b8685-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8685-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="b8685-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8685-105">DESCRIPTION</span></span>
<span data-ttu-id="b8685-106">New-AzDataMigrationMongoDbCollectionSetting cmdlet은 처리량 및 삭제 동작을 지정 하는 마이그레이션 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="b8685-107">출력 cmdlet은 컬렉션의 이름과 설정 값이 포함 된 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="b8685-108">출력이 마이그레이션에 대 한 데이터베이스 수준 설정을 어셈블하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="b8685-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b8685-109">EXAMPLES</span></span>

### <span data-ttu-id="b8685-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8685-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="b8685-111">변수</span><span class="sxs-lookup"><span data-stu-id="b8685-111">PARAMETERS</span></span>

### <span data-ttu-id="b8685-112">-이름</span><span class="sxs-lookup"><span data-stu-id="b8685-112">-Name</span></span>
<span data-ttu-id="b8685-113">컬렉션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8685-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="b8685-114">-ShardKey</span></span>
<span data-ttu-id="b8685-115">샤 드 키의 쉼표로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="b8685-116">MongoDb 대상의 경우 "ShardKeyName: Order"의 샤 드 키 순서를 지정할 수 있으며, 여기서 "_id, 전자 메일:-1"과 같이, 해시에 대해 order가 1,-1 이거나 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8685-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="b8685-117">-TargetRequestUnit</span></span>
<span data-ttu-id="b8685-118">전용 컬렉션 요청 단위 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="b8685-119">설정 하지 않은 경우 해당 컬렉션은 공유 데이터베이스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="b8685-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="b8685-120">-CanDelete</span></span>
<span data-ttu-id="b8685-121">대상 데이터를 삭제 해야 하는지 여부, 스위치가 설정 된 경우 마이그레이션하는 동안 정리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="b8685-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8685-122">CommonParameters</span></span>
<span data-ttu-id="b8685-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8685-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8685-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8685-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8685-125">입력</span><span class="sxs-lookup"><span data-stu-id="b8685-125">INPUTS</span></span>

### <span data-ttu-id="b8685-126">않아야</span><span class="sxs-lookup"><span data-stu-id="b8685-126">None</span></span>

## <span data-ttu-id="b8685-127">출력</span><span class="sxs-lookup"><span data-stu-id="b8685-127">OUTPUTS</span></span>

### <span data-ttu-id="b8685-128">DataMigration를 MongoDbCollectionSetting>.</span><span class="sxs-lookup"><span data-stu-id="b8685-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="b8685-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b8685-129">NOTES</span></span>

## <span data-ttu-id="b8685-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8685-130">RELATED LINKS</span></span>
