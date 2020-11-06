---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 01b3c055873276a265859683e07cd9150ffedafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523479"
---
# <span data-ttu-id="9b8d6-101">Get-AzsTableService</span><span class="sxs-lookup"><span data-stu-id="9b8d6-101">Get-AzsTableService</span></span>

## <span data-ttu-id="9b8d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8d6-103">테이블 서비스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b8d6-103">Returns the table service.</span></span>

## <span data-ttu-id="9b8d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b8d6-104">SYNTAX</span></span>

```
Get-AzsTableService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="9b8d6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9b8d6-105">DESCRIPTION</span></span>
<span data-ttu-id="9b8d6-106">테이블 서비스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b8d6-106">Returns the table service.</span></span>

## <span data-ttu-id="9b8d6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9b8d6-107">EXAMPLES</span></span>

### <span data-ttu-id="9b8d6-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9b8d6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="9b8d6-109">테이블 servie를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b8d6-109">Get the table servie.</span></span>

## <span data-ttu-id="9b8d6-110">변수</span><span class="sxs-lookup"><span data-stu-id="9b8d6-110">PARAMETERS</span></span>

### <span data-ttu-id="9b8d6-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9b8d6-111">-FarmName</span></span>
<span data-ttu-id="9b8d6-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="9b8d6-112">Farm Id.</span></span>

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

### <span data-ttu-id="9b8d6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b8d6-113">-ResourceGroupName</span></span>
<span data-ttu-id="9b8d6-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b8d6-114">Resource group name.</span></span>

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

### <span data-ttu-id="9b8d6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8d6-115">CommonParameters</span></span>
<span data-ttu-id="9b8d6-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b8d6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8d6-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b8d6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8d6-118">입력</span><span class="sxs-lookup"><span data-stu-id="9b8d6-118">INPUTS</span></span>

## <span data-ttu-id="9b8d6-119">출력</span><span class="sxs-lookup"><span data-stu-id="9b8d6-119">OUTPUTS</span></span>

### <span data-ttu-id="9b8d6-120">TableService. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="9b8d6-120">Microsoft.AzureStack.Management.Storage.Admin.Models.TableService</span></span>

## <span data-ttu-id="9b8d6-121">상속자</span><span class="sxs-lookup"><span data-stu-id="9b8d6-121">NOTES</span></span>

## <span data-ttu-id="9b8d6-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b8d6-122">RELATED LINKS</span></span>

