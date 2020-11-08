---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a53b5af4cf77ec961e65f8c0c0d84b05b4adfa1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046892"
---
# <span data-ttu-id="8e111-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="8e111-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="8e111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e111-102">SYNOPSIS</span></span>
<span data-ttu-id="8e111-103">Blob acquistions 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e111-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="8e111-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e111-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e111-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8e111-105">DESCRIPTION</span></span>
<span data-ttu-id="8e111-106">Blob acquistions 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e111-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="8e111-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8e111-107">EXAMPLES</span></span>

### <span data-ttu-id="8e111-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e111-108">EXAMPLE 1</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="8e111-109">Blob acquistions 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e111-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="8e111-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="8e111-110">EXAMPLE 2</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="8e111-111">Blob acquistions 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e111-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="8e111-112">변수</span><span class="sxs-lookup"><span data-stu-id="8e111-112">PARAMETERS</span></span>

### <span data-ttu-id="8e111-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="8e111-113">-FarmName</span></span>
<span data-ttu-id="8e111-114">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8e111-114">Farm Id.</span></span>

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

### <span data-ttu-id="8e111-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e111-115">-ResourceGroupName</span></span>
<span data-ttu-id="8e111-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e111-116">Resource group name.</span></span>

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

### <span data-ttu-id="8e111-117">-필터</span><span class="sxs-lookup"><span data-stu-id="8e111-117">-Filter</span></span>
<span data-ttu-id="8e111-118">필터 문자열</span><span class="sxs-lookup"><span data-stu-id="8e111-118">Filter string</span></span>

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

### <span data-ttu-id="8e111-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e111-119">CommonParameters</span></span>
<span data-ttu-id="8e111-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e111-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e111-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e111-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e111-122">입력</span><span class="sxs-lookup"><span data-stu-id="8e111-122">INPUTS</span></span>

## <span data-ttu-id="8e111-123">출력</span><span class="sxs-lookup"><span data-stu-id="8e111-123">OUTPUTS</span></span>

## <span data-ttu-id="8e111-124">상속자</span><span class="sxs-lookup"><span data-stu-id="8e111-124">NOTES</span></span>

## <span data-ttu-id="8e111-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e111-125">RELATED LINKS</span></span>
