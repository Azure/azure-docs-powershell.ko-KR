---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 817a4c8469d1d3652dade426857f88f9249f82b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966571"
---
# <span data-ttu-id="6cc96-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="6cc96-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="6cc96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cc96-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc96-103">mongoDb 마이그레이션에 따라 마이그레이션에 대한 컬렉션 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cc96-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="6cc96-104">구문</span><span class="sxs-lookup"><span data-stu-id="6cc96-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="6cc96-105">설명</span><span class="sxs-lookup"><span data-stu-id="6cc96-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc96-106">New-AzDataMigrationMongoDbCollectionSetting cmdlet은 처리 시간 및 삭제 동작을 지정하는 마이그레이션 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6cc96-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="6cc96-107">cmdlet의 출력은 컬렉션의 이름과 설정 값이 있는 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="6cc96-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="6cc96-108">출력은 마이그레이션에 대한 데이터베이스 수준 설정을 어셈블하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6cc96-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="6cc96-109">예제</span><span class="sxs-lookup"><span data-stu-id="6cc96-109">EXAMPLES</span></span>

### <span data-ttu-id="6cc96-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6cc96-110">Example 1</span></span>
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

## <span data-ttu-id="6cc96-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6cc96-111">PARAMETERS</span></span>

### <span data-ttu-id="6cc96-112">-Name</span><span class="sxs-lookup"><span data-stu-id="6cc96-112">-Name</span></span>
<span data-ttu-id="6cc96-113">컬렉션 이름</span><span class="sxs-lookup"><span data-stu-id="6cc96-113">Name of the collection</span></span>

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

### <span data-ttu-id="6cc96-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="6cc96-114">-ShardKey</span></span>
<span data-ttu-id="6cc96-115">콤마가 분리된 셰이드 키 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6cc96-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="6cc96-116">mongoDb 대상의 경우 "shardKeyName:Order"의 샤드 키 순서(예: "_id,email:-1")를 해시에 대해 1, -1 또는 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cc96-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="6cc96-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="6cc96-117">-TargetRequestUnit</span></span>
<span data-ttu-id="6cc96-118">전용 컬렉션 요청 단위 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6cc96-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="6cc96-119">설정하지 않은 경우 해당 컬렉션은 공유 데이터베이스 RU를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc96-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="6cc96-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="6cc96-120">-CanDelete</span></span>
<span data-ttu-id="6cc96-121">대상 데이터를 삭제해야 하는지 여부, 스위치가 설정된 경우 마이그레이션 시 정리됩니다.</span><span class="sxs-lookup"><span data-stu-id="6cc96-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="6cc96-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc96-122">CommonParameters</span></span>
<span data-ttu-id="6cc96-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6cc96-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc96-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6cc96-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc96-125">입력</span><span class="sxs-lookup"><span data-stu-id="6cc96-125">INPUTS</span></span>

### <span data-ttu-id="6cc96-126">없음</span><span class="sxs-lookup"><span data-stu-id="6cc96-126">None</span></span>

## <span data-ttu-id="6cc96-127">출력</span><span class="sxs-lookup"><span data-stu-id="6cc96-127">OUTPUTS</span></span>

### <span data-ttu-id="6cc96-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="6cc96-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="6cc96-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6cc96-129">NOTES</span></span>

## <span data-ttu-id="6cc96-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cc96-130">RELATED LINKS</span></span>
