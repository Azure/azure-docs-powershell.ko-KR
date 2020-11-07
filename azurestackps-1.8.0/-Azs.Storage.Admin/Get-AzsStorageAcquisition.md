---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874879"
---
# <span data-ttu-id="22d23-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="22d23-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="22d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22d23-102">SYNOPSIS</span></span>
<span data-ttu-id="22d23-103">Blob acquistions 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="22d23-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="22d23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22d23-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="22d23-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22d23-105">DESCRIPTION</span></span>
<span data-ttu-id="22d23-106">Blob acquistions 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="22d23-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="22d23-107">예제의</span><span class="sxs-lookup"><span data-stu-id="22d23-107">EXAMPLES</span></span>

### <span data-ttu-id="22d23-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="22d23-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="22d23-109">Blob acquistions 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22d23-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="22d23-110">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="22d23-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="22d23-111">Blob acquistions 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22d23-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="22d23-112">변수</span><span class="sxs-lookup"><span data-stu-id="22d23-112">PARAMETERS</span></span>

### <span data-ttu-id="22d23-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="22d23-113">-FarmName</span></span>
<span data-ttu-id="22d23-114">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="22d23-114">Farm Id.</span></span>

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

### <span data-ttu-id="22d23-115">-필터</span><span class="sxs-lookup"><span data-stu-id="22d23-115">-Filter</span></span>
<span data-ttu-id="22d23-116">필터 문자열</span><span class="sxs-lookup"><span data-stu-id="22d23-116">Filter string</span></span>

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

### <span data-ttu-id="22d23-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d23-117">-ResourceGroupName</span></span>
<span data-ttu-id="22d23-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22d23-118">Resource group name.</span></span>

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

### <span data-ttu-id="22d23-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d23-119">CommonParameters</span></span>
<span data-ttu-id="22d23-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22d23-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d23-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d23-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d23-122">입력</span><span class="sxs-lookup"><span data-stu-id="22d23-122">INPUTS</span></span>

## <span data-ttu-id="22d23-123">출력</span><span class="sxs-lookup"><span data-stu-id="22d23-123">OUTPUTS</span></span>

## <span data-ttu-id="22d23-124">상속자</span><span class="sxs-lookup"><span data-stu-id="22d23-124">NOTES</span></span>

## <span data-ttu-id="22d23-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22d23-125">RELATED LINKS</span></span>

