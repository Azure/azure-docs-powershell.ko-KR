---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4847310f65a0b652d15321cd49583212ef5844d8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874877"
---
# <span data-ttu-id="a7a46-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a7a46-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="a7a46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7a46-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a46-103">지정 된 공유에서 마이그레이션될 수 있는 컨테이너 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a46-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="a7a46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7a46-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a7a46-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7a46-105">DESCRIPTION</span></span>
<span data-ttu-id="a7a46-106">지정 된 공유에서 마이그레이션될 수 있는 컨테이너 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a46-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="a7a46-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a7a46-107">EXAMPLES</span></span>

### <span data-ttu-id="a7a46-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7a46-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="a7a46-109">지정 된 공유에서 마이그레이션될 수 있는 컨테이너 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7a46-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="a7a46-110">변수</span><span class="sxs-lookup"><span data-stu-id="a7a46-110">PARAMETERS</span></span>

### <span data-ttu-id="a7a46-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="a7a46-111">-FarmName</span></span>
<span data-ttu-id="a7a46-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a7a46-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a46-113">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a7a46-113">-MaxCount</span></span>
<span data-ttu-id="a7a46-114">컨테이너의 최대 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="a7a46-114">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a46-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a46-115">-ResourceGroupName</span></span>
<span data-ttu-id="a7a46-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7a46-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a46-117">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a7a46-117">-ShareName</span></span>
<span data-ttu-id="a7a46-118">저장소 컨테이너를 보유 하는 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7a46-118">Share name which holds the storage containers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a46-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="a7a46-119">-StartIndex</span></span>
<span data-ttu-id="a7a46-120">Get 컨테이너의 시작 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="a7a46-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a46-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a46-121">CommonParameters</span></span>
<span data-ttu-id="a7a46-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7a46-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a46-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a46-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a46-124">입력</span><span class="sxs-lookup"><span data-stu-id="a7a46-124">INPUTS</span></span>

## <span data-ttu-id="a7a46-125">출력</span><span class="sxs-lookup"><span data-stu-id="a7a46-125">OUTPUTS</span></span>

## <span data-ttu-id="a7a46-126">상속자</span><span class="sxs-lookup"><span data-stu-id="a7a46-126">NOTES</span></span>

## <span data-ttu-id="a7a46-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7a46-127">RELATED LINKS</span></span>

