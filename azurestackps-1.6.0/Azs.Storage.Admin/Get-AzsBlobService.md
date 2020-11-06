---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d9ff0746de44d2e5c3c67ea95b66dd3bd3902ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523243"
---
# <span data-ttu-id="2f55e-101">Get-AzsBlobService</span><span class="sxs-lookup"><span data-stu-id="2f55e-101">Get-AzsBlobService</span></span>

## <span data-ttu-id="2f55e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f55e-102">SYNOPSIS</span></span>
<span data-ttu-id="2f55e-103">Blob 서비스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f55e-103">Returns the blob service.</span></span>

## <span data-ttu-id="2f55e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f55e-104">SYNTAX</span></span>

```
Get-AzsBlobService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="2f55e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2f55e-105">DESCRIPTION</span></span>
<span data-ttu-id="2f55e-106">Blob 서비스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f55e-106">Returns the blob service.</span></span>

## <span data-ttu-id="2f55e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2f55e-107">EXAMPLES</span></span>

### <span data-ttu-id="2f55e-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2f55e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="2f55e-109">Blob 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2f55e-109">Get the blob service.</span></span>

## <span data-ttu-id="2f55e-110">변수</span><span class="sxs-lookup"><span data-stu-id="2f55e-110">PARAMETERS</span></span>

### <span data-ttu-id="2f55e-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="2f55e-111">-FarmName</span></span>
<span data-ttu-id="2f55e-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="2f55e-112">Farm Id.</span></span>

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

### <span data-ttu-id="2f55e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f55e-113">-ResourceGroupName</span></span>
<span data-ttu-id="2f55e-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f55e-114">Resource group name.</span></span>

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

### <span data-ttu-id="2f55e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f55e-115">CommonParameters</span></span>
<span data-ttu-id="2f55e-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f55e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f55e-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f55e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f55e-118">입력</span><span class="sxs-lookup"><span data-stu-id="2f55e-118">INPUTS</span></span>

## <span data-ttu-id="2f55e-119">출력</span><span class="sxs-lookup"><span data-stu-id="2f55e-119">OUTPUTS</span></span>

### <span data-ttu-id="2f55e-120">Microsoft AzureStack. 관리자. BlobService</span><span class="sxs-lookup"><span data-stu-id="2f55e-120">Microsoft.AzureStack.Management.Storage.Admin.Models.BlobService</span></span>

## <span data-ttu-id="2f55e-121">상속자</span><span class="sxs-lookup"><span data-stu-id="2f55e-121">NOTES</span></span>

## <span data-ttu-id="2f55e-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f55e-122">RELATED LINKS</span></span>

