---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 007f020d97d0c46f5db5031f4163d669d976f642
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882918"
---
# <span data-ttu-id="4caf3-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4caf3-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="4caf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4caf3-102">SYNOPSIS</span></span>
<span data-ttu-id="4caf3-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="4caf3-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4caf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4caf3-104">SYNTAX</span></span>

### <span data-ttu-id="4caf3-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="4caf3-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4caf3-106">확장</span><span class="sxs-lookup"><span data-stu-id="4caf3-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4caf3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4caf3-107">DESCRIPTION</span></span>
<span data-ttu-id="4caf3-108">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="4caf3-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="4caf3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4caf3-109">EXAMPLES</span></span>

### <span data-ttu-id="4caf3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4caf3-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4caf3-111">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="4caf3-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="4caf3-112">변수</span><span class="sxs-lookup"><span data-stu-id="4caf3-112">PARAMETERS</span></span>

### <span data-ttu-id="4caf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4caf3-113">-DefaultProfile</span></span>
<span data-ttu-id="4caf3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4caf3-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4caf3-115">-ExpandResource</span></span>
<span data-ttu-id="4caf3-116">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf3-116">The resource reference to be expanded.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4caf3-117">-이름</span><span class="sxs-lookup"><span data-stu-id="4caf3-117">-Name</span></span>
<span data-ttu-id="4caf3-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf3-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4caf3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4caf3-119">-ResourceGroupName</span></span>
<span data-ttu-id="4caf3-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4caf3-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4caf3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4caf3-121">CommonParameters</span></span>
<span data-ttu-id="4caf3-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4caf3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4caf3-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4caf3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4caf3-124">입력</span><span class="sxs-lookup"><span data-stu-id="4caf3-124">INPUTS</span></span>

### <span data-ttu-id="4caf3-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4caf3-125">System.String</span></span>

## <span data-ttu-id="4caf3-126">출력</span><span class="sxs-lookup"><span data-stu-id="4caf3-126">OUTPUTS</span></span>

### <span data-ttu-id="4caf3-127">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4caf3-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4caf3-128">상속자</span><span class="sxs-lookup"><span data-stu-id="4caf3-128">NOTES</span></span>

## <span data-ttu-id="4caf3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4caf3-129">RELATED LINKS</span></span>

