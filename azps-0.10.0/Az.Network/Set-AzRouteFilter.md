---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 942669106e70bbb8c5b5b6f059fe934effe9b7fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876552"
---
# <span data-ttu-id="ad88c-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ad88c-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="ad88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad88c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad88c-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="ad88c-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="ad88c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad88c-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad88c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad88c-105">DESCRIPTION</span></span>
<span data-ttu-id="ad88c-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="ad88c-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ad88c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ad88c-107">EXAMPLES</span></span>

### <span data-ttu-id="ad88c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad88c-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ad88c-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="ad88c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ad88c-110">변수</span><span class="sxs-lookup"><span data-stu-id="ad88c-110">PARAMETERS</span></span>

### <span data-ttu-id="ad88c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad88c-111">-AsJob</span></span>
<span data-ttu-id="ad88c-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ad88c-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad88c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad88c-113">-DefaultProfile</span></span>
<span data-ttu-id="ad88c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad88c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad88c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ad88c-115">-Force</span></span>
<span data-ttu-id="ad88c-116">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="ad88c-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad88c-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ad88c-117">-RouteFilter</span></span>
<span data-ttu-id="ad88c-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ad88c-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad88c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ad88c-119">-Confirm</span></span>
<span data-ttu-id="ad88c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad88c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad88c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad88c-121">-WhatIf</span></span>
<span data-ttu-id="ad88c-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad88c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad88c-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad88c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad88c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad88c-124">CommonParameters</span></span>
<span data-ttu-id="ad88c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad88c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad88c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad88c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad88c-127">입력</span><span class="sxs-lookup"><span data-stu-id="ad88c-127">INPUTS</span></span>

### <span data-ttu-id="ad88c-128">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ad88c-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ad88c-129">출력</span><span class="sxs-lookup"><span data-stu-id="ad88c-129">OUTPUTS</span></span>

### <span data-ttu-id="ad88c-130">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ad88c-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ad88c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ad88c-131">NOTES</span></span>

## <span data-ttu-id="ad88c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad88c-132">RELATED LINKS</span></span>

