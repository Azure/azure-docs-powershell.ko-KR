---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874768"
---
# <span data-ttu-id="af17e-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="af17e-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="af17e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af17e-102">SYNOPSIS</span></span>
<span data-ttu-id="af17e-103">업데이트 위치 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af17e-103">Get the list of update locations.</span></span>

## <span data-ttu-id="af17e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af17e-104">SYNTAX</span></span>

### <span data-ttu-id="af17e-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="af17e-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="af17e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="af17e-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="af17e-107">리소스</span><span class="sxs-lookup"><span data-stu-id="af17e-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="af17e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="af17e-108">DESCRIPTION</span></span>
<span data-ttu-id="af17e-109">업데이트 위치 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af17e-109">Get the list of update locations.</span></span> <span data-ttu-id="af17e-110">반환 된 위치를 사용 하 여 AzsUpdate를 사용 하 여 특정 위치에서 사용 가능한 업데이트를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af17e-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="af17e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="af17e-111">EXAMPLES</span></span>

### <span data-ttu-id="af17e-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="af17e-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="af17e-113">업데이트 위치 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af17e-113">Get the list of update locations.</span></span>

## <span data-ttu-id="af17e-114">변수</span><span class="sxs-lookup"><span data-stu-id="af17e-114">PARAMETERS</span></span>

### <span data-ttu-id="af17e-115">-위치</span><span class="sxs-lookup"><span data-stu-id="af17e-115">-Location</span></span>
<span data-ttu-id="af17e-116">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af17e-116">Name of the Location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af17e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af17e-117">-ResourceGroupName</span></span>
<span data-ttu-id="af17e-118">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="af17e-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af17e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af17e-119">-ResourceId</span></span>
<span data-ttu-id="af17e-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="af17e-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af17e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af17e-121">CommonParameters</span></span>
<span data-ttu-id="af17e-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af17e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af17e-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af17e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af17e-124">입력</span><span class="sxs-lookup"><span data-stu-id="af17e-124">INPUTS</span></span>

## <span data-ttu-id="af17e-125">출력</span><span class="sxs-lookup"><span data-stu-id="af17e-125">OUTPUTS</span></span>

### <span data-ttu-id="af17e-126">Update.exe. a. 관리자. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="af17e-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="af17e-127">상속자</span><span class="sxs-lookup"><span data-stu-id="af17e-127">NOTES</span></span>

## <span data-ttu-id="af17e-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af17e-128">RELATED LINKS</span></span>
