---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206032"
---
# <span data-ttu-id="c4e01-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="c4e01-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="c4e01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4e01-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e01-103">사용 가능한 예약 카탈로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e01-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="c4e01-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4e01-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4e01-105">설명</span><span class="sxs-lookup"><span data-stu-id="c4e01-105">DESCRIPTION</span></span>
<span data-ttu-id="c4e01-106">지정된 Azure 구독에 대해 Reserved Instance 구매에 사용할 수 있는 지역 및 SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c4e01-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="c4e01-107">예제</span><span class="sxs-lookup"><span data-stu-id="c4e01-107">EXAMPLES</span></span>

### <span data-ttu-id="c4e01-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4e01-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="c4e01-109">기본 구독에 대한 westus에서 VirtualMachines 카탈로그를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e01-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="c4e01-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="c4e01-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="c4e01-111">지정된 구독에 대한 SuseLinux 카탈로그를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e01-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="c4e01-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4e01-112">PARAMETERS</span></span>

### <span data-ttu-id="c4e01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e01-113">-DefaultProfile</span></span>
<span data-ttu-id="c4e01-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4e01-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4e01-115">-Location</span><span class="sxs-lookup"><span data-stu-id="c4e01-115">-Location</span></span>
<span data-ttu-id="c4e01-116">카탈로그에서 예약된 리소스의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e01-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="c4e01-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="c4e01-117">-ReservedResourceType</span></span>
<span data-ttu-id="c4e01-118">카탈로그에서 예약된 리소스의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e01-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="c4e01-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4e01-119">-SubscriptionId</span></span>
<span data-ttu-id="c4e01-120">구독의 ID</span><span class="sxs-lookup"><span data-stu-id="c4e01-120">Id of the subscription</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e01-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e01-121">CommonParameters</span></span>
<span data-ttu-id="c4e01-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4e01-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e01-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4e01-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e01-124">입력</span><span class="sxs-lookup"><span data-stu-id="c4e01-124">INPUTS</span></span>

### <span data-ttu-id="c4e01-125">없음</span><span class="sxs-lookup"><span data-stu-id="c4e01-125">None</span></span>

## <span data-ttu-id="c4e01-126">출력</span><span class="sxs-lookup"><span data-stu-id="c4e01-126">OUTPUTS</span></span>

### <span data-ttu-id="c4e01-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span><span class="sxs-lookup"><span data-stu-id="c4e01-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="c4e01-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4e01-128">NOTES</span></span>

## <span data-ttu-id="c4e01-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4e01-129">RELATED LINKS</span></span>
