---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214945"
---
# <span data-ttu-id="aab6b-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="aab6b-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="aab6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aab6b-102">SYNOPSIS</span></span>
<span data-ttu-id="aab6b-103">PSHeaderAction 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aab6b-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="aab6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aab6b-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aab6b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aab6b-105">DESCRIPTION</span></span>
<span data-ttu-id="aab6b-106">PSRulesEngineAction 개체를 만들기 위한 PSHeaderAction 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aab6b-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="aab6b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aab6b-107">EXAMPLES</span></span>

### <span data-ttu-id="aab6b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="aab6b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="aab6b-109">변수</span><span class="sxs-lookup"><span data-stu-id="aab6b-109">PARAMETERS</span></span>

### <span data-ttu-id="aab6b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab6b-110">-DefaultProfile</span></span>
<span data-ttu-id="aab6b-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aab6b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab6b-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="aab6b-112">-HeaderActionType</span></span>
<span data-ttu-id="aab6b-113">헤더에 적용 되는 조작 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="aab6b-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab6b-114">-인원 Ername</span><span class="sxs-lookup"><span data-stu-id="aab6b-114">-HeaderName</span></span>
<span data-ttu-id="aab6b-115">이 작업이 적용 되는 머리글의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aab6b-115">The name of the header this action will apply to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab6b-116">-값</span><span class="sxs-lookup"><span data-stu-id="aab6b-116">-Value</span></span>
<span data-ttu-id="aab6b-117">지정 된 헤더 이름을 업데이트할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="aab6b-117">The value to update the given header name with.</span></span>
<span data-ttu-id="aab6b-118">이 값은 actionType이 Delete 인 경우에는 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aab6b-118">This value is not used if the actionType is Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab6b-119">CommonParameters</span></span>
<span data-ttu-id="aab6b-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aab6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab6b-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aab6b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab6b-122">입력</span><span class="sxs-lookup"><span data-stu-id="aab6b-122">INPUTS</span></span>

### <span data-ttu-id="aab6b-123">않아야</span><span class="sxs-lookup"><span data-stu-id="aab6b-123">None</span></span>

## <span data-ttu-id="aab6b-124">출력</span><span class="sxs-lookup"><span data-stu-id="aab6b-124">OUTPUTS</span></span>

### <span data-ttu-id="aab6b-125">FrontDoor. PSHeaderAction/.</span><span class="sxs-lookup"><span data-stu-id="aab6b-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="aab6b-126">상속자</span><span class="sxs-lookup"><span data-stu-id="aab6b-126">NOTES</span></span>

## <span data-ttu-id="aab6b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aab6b-127">RELATED LINKS</span></span>
