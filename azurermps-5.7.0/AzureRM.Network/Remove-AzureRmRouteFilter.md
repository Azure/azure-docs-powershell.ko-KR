---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
ms.openlocfilehash: 5fcdbeee663873292b463bf774762c9de5418b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704178"
---
# <span data-ttu-id="4f020-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4f020-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="4f020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f020-102">SYNOPSIS</span></span>
<span data-ttu-id="4f020-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="4f020-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f020-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f020-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f020-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4f020-105">DESCRIPTION</span></span>
<span data-ttu-id="4f020-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="4f020-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="4f020-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4f020-107">EXAMPLES</span></span>

### <span data-ttu-id="4f020-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f020-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4f020-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="4f020-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="4f020-110">변수</span><span class="sxs-lookup"><span data-stu-id="4f020-110">PARAMETERS</span></span>

### <span data-ttu-id="4f020-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f020-111">-DefaultProfile</span></span>
<span data-ttu-id="4f020-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f020-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f020-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4f020-113">-Force</span></span>
<span data-ttu-id="4f020-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f020-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4f020-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4f020-115">-Name</span></span>
<span data-ttu-id="4f020-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f020-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f020-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f020-117">-PassThru</span></span>
<span data-ttu-id="4f020-118">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="4f020-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4f020-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f020-119">-ResourceGroupName</span></span>
<span data-ttu-id="4f020-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f020-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f020-121">-확인</span><span class="sxs-lookup"><span data-stu-id="4f020-121">-Confirm</span></span>
<span data-ttu-id="4f020-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f020-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f020-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f020-123">-WhatIf</span></span>
<span data-ttu-id="4f020-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f020-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f020-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f020-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f020-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f020-126">CommonParameters</span></span>
<span data-ttu-id="4f020-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f020-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f020-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f020-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f020-129">입력</span><span class="sxs-lookup"><span data-stu-id="4f020-129">INPUTS</span></span>

### <span data-ttu-id="4f020-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4f020-130">System.String</span></span>

## <span data-ttu-id="4f020-131">출력</span><span class="sxs-lookup"><span data-stu-id="4f020-131">OUTPUTS</span></span>

### <span data-ttu-id="4f020-132">System. 개체</span><span class="sxs-lookup"><span data-stu-id="4f020-132">System.Object</span></span>

## <span data-ttu-id="4f020-133">상속자</span><span class="sxs-lookup"><span data-stu-id="4f020-133">NOTES</span></span>

## <span data-ttu-id="4f020-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f020-134">RELATED LINKS</span></span>

