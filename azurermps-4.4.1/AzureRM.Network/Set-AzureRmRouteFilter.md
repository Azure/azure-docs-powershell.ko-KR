---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 56f0c3ec3a69819ad7faa28b10d33a3cf751c48f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529265"
---
# <span data-ttu-id="417c8-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="417c8-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="417c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="417c8-102">SYNOPSIS</span></span>
<span data-ttu-id="417c8-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="417c8-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="417c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="417c8-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="417c8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="417c8-105">DESCRIPTION</span></span>
<span data-ttu-id="417c8-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="417c8-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="417c8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="417c8-107">EXAMPLES</span></span>

### <span data-ttu-id="417c8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="417c8-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="417c8-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="417c8-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="417c8-110">변수</span><span class="sxs-lookup"><span data-stu-id="417c8-110">PARAMETERS</span></span>

### <span data-ttu-id="417c8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="417c8-111">-Force</span></span>
<span data-ttu-id="417c8-112">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="417c8-112">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417c8-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="417c8-113">-RouteFilter</span></span>
<span data-ttu-id="417c8-114">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="417c8-114">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="417c8-115">-확인</span><span class="sxs-lookup"><span data-stu-id="417c8-115">-Confirm</span></span>
<span data-ttu-id="417c8-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c8-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417c8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="417c8-117">-WhatIf</span></span>
<span data-ttu-id="417c8-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="417c8-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="417c8-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="417c8-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417c8-120">-DefaultProfile</span></span>
<span data-ttu-id="417c8-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="417c8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417c8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417c8-122">CommonParameters</span></span>
<span data-ttu-id="417c8-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417c8-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="417c8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417c8-125">입력</span><span class="sxs-lookup"><span data-stu-id="417c8-125">INPUTS</span></span>

### <span data-ttu-id="417c8-126">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="417c8-126">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="417c8-127">출력</span><span class="sxs-lookup"><span data-stu-id="417c8-127">OUTPUTS</span></span>

### <span data-ttu-id="417c8-128">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="417c8-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="417c8-129">상속자</span><span class="sxs-lookup"><span data-stu-id="417c8-129">NOTES</span></span>

## <span data-ttu-id="417c8-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="417c8-130">RELATED LINKS</span></span>

