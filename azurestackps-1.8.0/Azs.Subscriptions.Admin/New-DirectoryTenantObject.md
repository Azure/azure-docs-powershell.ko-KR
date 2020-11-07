---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874632"
---
# <span data-ttu-id="0b08d-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="0b08d-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="0b08d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b08d-102">SYNOPSIS</span></span>
<span data-ttu-id="0b08d-103">디렉터리 테 넌 트.</span><span class="sxs-lookup"><span data-stu-id="0b08d-103">Directory tenant.</span></span>

## <span data-ttu-id="0b08d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b08d-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="0b08d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b08d-105">DESCRIPTION</span></span>
<span data-ttu-id="0b08d-106">디렉터리 테 넌 트.</span><span class="sxs-lookup"><span data-stu-id="0b08d-106">Directory tenant.</span></span>

## <span data-ttu-id="0b08d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0b08d-107">EXAMPLES</span></span>

### <span data-ttu-id="0b08d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b08d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0b08d-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="0b08d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="0b08d-110">변수</span><span class="sxs-lookup"><span data-stu-id="0b08d-110">PARAMETERS</span></span>

### <span data-ttu-id="0b08d-111">-Id</span><span class="sxs-lookup"><span data-stu-id="0b08d-111">-Id</span></span>
<span data-ttu-id="0b08d-112">리소스의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="0b08d-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b08d-113">-위치</span><span class="sxs-lookup"><span data-stu-id="0b08d-113">-Location</span></span>
<span data-ttu-id="0b08d-114">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0b08d-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b08d-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0b08d-115">-Name</span></span>
<span data-ttu-id="0b08d-116">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b08d-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b08d-117">태그</span><span class="sxs-lookup"><span data-stu-id="0b08d-117">-Tags</span></span>
<span data-ttu-id="0b08d-118">키-값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0b08d-118">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b08d-119">-TenantId</span><span class="sxs-lookup"><span data-stu-id="0b08d-119">-TenantId</span></span>
<span data-ttu-id="0b08d-120">테 넌 트 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0b08d-120">Tenant unique identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b08d-121">-Type</span><span class="sxs-lookup"><span data-stu-id="0b08d-121">-Type</span></span>
<span data-ttu-id="0b08d-122">리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0b08d-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b08d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b08d-123">CommonParameters</span></span>
<span data-ttu-id="0b08d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b08d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b08d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b08d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b08d-126">입력</span><span class="sxs-lookup"><span data-stu-id="0b08d-126">INPUTS</span></span>

## <span data-ttu-id="0b08d-127">출력</span><span class="sxs-lookup"><span data-stu-id="0b08d-127">OUTPUTS</span></span>

## <span data-ttu-id="0b08d-128">상속자</span><span class="sxs-lookup"><span data-stu-id="0b08d-128">NOTES</span></span>

## <span data-ttu-id="0b08d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b08d-129">RELATED LINKS</span></span>

