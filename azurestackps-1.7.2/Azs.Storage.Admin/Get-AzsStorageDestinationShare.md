---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47ac85406955592cba566df505900e6c42befb7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873953"
---
# <span data-ttu-id="433f0-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="433f0-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="433f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="433f0-102">SYNOPSIS</span></span>
<span data-ttu-id="433f0-103">시스템에서 마이그레이션에 가장 적합 한 후보로 간주 하는 대상 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="433f0-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="433f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="433f0-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="433f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="433f0-105">DESCRIPTION</span></span>
<span data-ttu-id="433f0-106">시스템에서 마이그레이션에 가장 적합 한 후보로 간주 하는 대상 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="433f0-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="433f0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="433f0-107">EXAMPLES</span></span>

### <span data-ttu-id="433f0-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="433f0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="433f0-109">시스템에서 마이그레이션에 가장 적합 한 후보로 간주 하는 대상 공유 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="433f0-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="433f0-110">변수</span><span class="sxs-lookup"><span data-stu-id="433f0-110">PARAMETERS</span></span>

### <span data-ttu-id="433f0-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="433f0-111">-FarmName</span></span>
<span data-ttu-id="433f0-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="433f0-112">Farm Id.</span></span>

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

### <span data-ttu-id="433f0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433f0-113">-ResourceGroupName</span></span>
<span data-ttu-id="433f0-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433f0-114">Resource group name.</span></span>

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

### <span data-ttu-id="433f0-115">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="433f0-115">-SourceShareName</span></span>
<span data-ttu-id="433f0-116">마이그레이션할 컨테이너를 보유 한 공유의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433f0-116">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="433f0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433f0-117">CommonParameters</span></span>
<span data-ttu-id="433f0-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="433f0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433f0-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="433f0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433f0-120">입력</span><span class="sxs-lookup"><span data-stu-id="433f0-120">INPUTS</span></span>

## <span data-ttu-id="433f0-121">출력</span><span class="sxs-lookup"><span data-stu-id="433f0-121">OUTPUTS</span></span>

## <span data-ttu-id="433f0-122">상속자</span><span class="sxs-lookup"><span data-stu-id="433f0-122">NOTES</span></span>

## <span data-ttu-id="433f0-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="433f0-123">RELATED LINKS</span></span>

