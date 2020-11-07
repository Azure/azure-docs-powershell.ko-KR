---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 1d914509b43dd59d95d32a11c3f5ce3487b03e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875527"
---
# <span data-ttu-id="adc9c-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="adc9c-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="adc9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="adc9c-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="adc9c-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="adc9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adc9c-104">SYNTAX</span></span>

### <span data-ttu-id="adc9c-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="adc9c-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adc9c-106">확장</span><span class="sxs-lookup"><span data-stu-id="adc9c-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adc9c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="adc9c-107">DESCRIPTION</span></span>
<span data-ttu-id="adc9c-108">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="adc9c-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="adc9c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="adc9c-109">EXAMPLES</span></span>

### <span data-ttu-id="adc9c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="adc9c-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="adc9c-111">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="adc9c-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="adc9c-112">변수</span><span class="sxs-lookup"><span data-stu-id="adc9c-112">PARAMETERS</span></span>

### <span data-ttu-id="adc9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc9c-113">-DefaultProfile</span></span>
<span data-ttu-id="adc9c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adc9c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adc9c-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="adc9c-115">-ExpandResource</span></span>
<span data-ttu-id="adc9c-116">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="adc9c-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="adc9c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="adc9c-117">-Name</span></span>
<span data-ttu-id="adc9c-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adc9c-118">The resource name.</span></span>

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

### <span data-ttu-id="adc9c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc9c-119">-ResourceGroupName</span></span>
<span data-ttu-id="adc9c-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adc9c-120">The resource group name.</span></span>

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

### <span data-ttu-id="adc9c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc9c-121">CommonParameters</span></span>
<span data-ttu-id="adc9c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc9c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc9c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adc9c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc9c-124">입력</span><span class="sxs-lookup"><span data-stu-id="adc9c-124">INPUTS</span></span>

### <span data-ttu-id="adc9c-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adc9c-125">System.String</span></span>

## <span data-ttu-id="adc9c-126">출력</span><span class="sxs-lookup"><span data-stu-id="adc9c-126">OUTPUTS</span></span>

### <span data-ttu-id="adc9c-127">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="adc9c-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="adc9c-128">상속자</span><span class="sxs-lookup"><span data-stu-id="adc9c-128">NOTES</span></span>

## <span data-ttu-id="adc9c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adc9c-129">RELATED LINKS</span></span>

