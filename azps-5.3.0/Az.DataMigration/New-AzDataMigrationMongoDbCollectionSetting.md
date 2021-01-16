---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387563"
---
# <span data-ttu-id="82057-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="82057-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="82057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82057-102">SYNOPSIS</span></span>
<span data-ttu-id="82057-103">mongoDb 마이그레이션에 따라 마이그레이션에 대한 컬렉션 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82057-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="82057-104">구문</span><span class="sxs-lookup"><span data-stu-id="82057-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="82057-105">설명</span><span class="sxs-lookup"><span data-stu-id="82057-105">DESCRIPTION</span></span>
<span data-ttu-id="82057-106">New-AzDataMigrationMongoDbCollectionSetting cmdlet은 처리 및 삭제 동작을 지정하는 마이그레이션 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82057-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="82057-107">cmdlet의 출력은 컬렉션의 이름과 설정 값이 있는 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="82057-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="82057-108">출력은 마이그레이션을 위한 데이터베이스 수준 설정을 어셈블하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="82057-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="82057-109">예제</span><span class="sxs-lookup"><span data-stu-id="82057-109">EXAMPLES</span></span>

### <span data-ttu-id="82057-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="82057-110">Example 1</span></span>
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

## <span data-ttu-id="82057-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82057-111">PARAMETERS</span></span>

### <span data-ttu-id="82057-112">-Name</span><span class="sxs-lookup"><span data-stu-id="82057-112">-Name</span></span>
<span data-ttu-id="82057-113">컬렉션의 이름</span><span class="sxs-lookup"><span data-stu-id="82057-113">Name of the collection</span></span>

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

### <span data-ttu-id="82057-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="82057-114">-ShardKey</span></span>
<span data-ttu-id="82057-115">콤마로 구분된 Shard 키 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="82057-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="82057-116">mongoDb 대상의 경우 "shardKeyName:Order"의 공유 키 순서를 지정할 수 있습니다. 여기서 순서는 해시에 대해 1, -1 또는 비어 있습니다(예: "_id,email:-1").</span><span class="sxs-lookup"><span data-stu-id="82057-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="82057-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="82057-117">-TargetRequestUnit</span></span>
<span data-ttu-id="82057-118">전용 컬렉션 요청 단위 값입니다.</span><span class="sxs-lookup"><span data-stu-id="82057-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="82057-119">설정되지 않은 경우 해당 컬렉션은 공유 데이터베이스 RU를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="82057-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="82057-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="82057-120">-CanDelete</span></span>
<span data-ttu-id="82057-121">대상 데이터를 삭제해야 하는지 여부, 스위치가 설정된 경우 마이그레이션 시 정리됩니다.</span><span class="sxs-lookup"><span data-stu-id="82057-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="82057-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82057-122">CommonParameters</span></span>
<span data-ttu-id="82057-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82057-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82057-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="82057-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82057-125">입력</span><span class="sxs-lookup"><span data-stu-id="82057-125">INPUTS</span></span>

### <span data-ttu-id="82057-126">없음</span><span class="sxs-lookup"><span data-stu-id="82057-126">None</span></span>

## <span data-ttu-id="82057-127">출력</span><span class="sxs-lookup"><span data-stu-id="82057-127">OUTPUTS</span></span>

### <span data-ttu-id="82057-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="82057-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="82057-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82057-129">NOTES</span></span>

## <span data-ttu-id="82057-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82057-130">RELATED LINKS</span></span>
