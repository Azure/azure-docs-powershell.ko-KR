---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34d5c967154f08526a0002f187b8cb869d933d39
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046890"
---
# <span data-ttu-id="b0734-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b0734-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="b0734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0734-102">SYNOPSIS</span></span>
<span data-ttu-id="b0734-103">지정 된 공유에서 마이그레이션될 수 있는 컨테이너 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0734-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="b0734-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0734-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b0734-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0734-105">DESCRIPTION</span></span>
<span data-ttu-id="b0734-106">지정 된 공유에서 마이그레이션될 수 있는 컨테이너 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0734-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="b0734-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0734-107">EXAMPLES</span></span>

### <span data-ttu-id="b0734-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0734-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="b0734-109">지정 된 공유에서 마이그레이션될 수 있는 컨테이너 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0734-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="b0734-110">변수</span><span class="sxs-lookup"><span data-stu-id="b0734-110">PARAMETERS</span></span>

### <span data-ttu-id="b0734-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="b0734-111">-FarmName</span></span>
<span data-ttu-id="b0734-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b0734-112">Farm Id.</span></span>

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

### <span data-ttu-id="b0734-113">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b0734-113">-ShareName</span></span>
<span data-ttu-id="b0734-114">저장소 컨테이너를 보유 하는 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0734-114">Share name which holds the storage containers.</span></span>

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

### <span data-ttu-id="b0734-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0734-115">-ResourceGroupName</span></span>
<span data-ttu-id="b0734-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0734-116">Resource group name.</span></span>

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

### <span data-ttu-id="b0734-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b0734-117">-MaxCount</span></span>
<span data-ttu-id="b0734-118">컨테이너의 최대 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="b0734-118">The max count of containers.</span></span>

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

### <span data-ttu-id="b0734-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="b0734-119">-StartIndex</span></span>
<span data-ttu-id="b0734-120">Get 컨테이너의 시작 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="b0734-120">The start index of get containers.</span></span>

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

### <span data-ttu-id="b0734-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0734-121">CommonParameters</span></span>
<span data-ttu-id="b0734-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0734-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0734-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0734-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0734-124">입력</span><span class="sxs-lookup"><span data-stu-id="b0734-124">INPUTS</span></span>

## <span data-ttu-id="b0734-125">출력</span><span class="sxs-lookup"><span data-stu-id="b0734-125">OUTPUTS</span></span>

## <span data-ttu-id="b0734-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b0734-126">NOTES</span></span>

## <span data-ttu-id="b0734-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0734-127">RELATED LINKS</span></span>
