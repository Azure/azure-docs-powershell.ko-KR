---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689093"
---
# <span data-ttu-id="f28fa-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="f28fa-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="f28fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f28fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f28fa-103">업데이트 위치 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f28fa-103">Get the list of update locations.</span></span>

## <span data-ttu-id="f28fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f28fa-104">SYNTAX</span></span>

### <span data-ttu-id="f28fa-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f28fa-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f28fa-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="f28fa-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f28fa-107">리소스</span><span class="sxs-lookup"><span data-stu-id="f28fa-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f28fa-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f28fa-108">DESCRIPTION</span></span>
<span data-ttu-id="f28fa-109">업데이트 위치 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f28fa-109">Get the list of update locations.</span></span> <span data-ttu-id="f28fa-110">반환 된 위치를 사용 하 여 AzsUpdate를 사용 하 여 특정 위치에서 사용 가능한 업데이트를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f28fa-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="f28fa-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f28fa-111">EXAMPLES</span></span>

### <span data-ttu-id="f28fa-112">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f28fa-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="f28fa-113">업데이트 위치 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f28fa-113">Get the list of update locations.</span></span>

## <span data-ttu-id="f28fa-114">변수</span><span class="sxs-lookup"><span data-stu-id="f28fa-114">PARAMETERS</span></span>

### <span data-ttu-id="f28fa-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f28fa-115">-Name</span></span>
<span data-ttu-id="f28fa-116">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f28fa-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f28fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="f28fa-118">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f28fa-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f28fa-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f28fa-119">-ResourceId</span></span>
<span data-ttu-id="f28fa-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f28fa-120">The resource id.</span></span>

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

### <span data-ttu-id="f28fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28fa-121">CommonParameters</span></span>
<span data-ttu-id="f28fa-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f28fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28fa-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f28fa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28fa-124">입력</span><span class="sxs-lookup"><span data-stu-id="f28fa-124">INPUTS</span></span>

## <span data-ttu-id="f28fa-125">출력</span><span class="sxs-lookup"><span data-stu-id="f28fa-125">OUTPUTS</span></span>

### <span data-ttu-id="f28fa-126">Update.exe. a. 관리자. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="f28fa-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="f28fa-127">상속자</span><span class="sxs-lookup"><span data-stu-id="f28fa-127">NOTES</span></span>

## <span data-ttu-id="f28fa-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f28fa-128">RELATED LINKS</span></span>

