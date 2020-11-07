---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 99f621824d10b574c7f64fb7653bc4154ba6766e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702506"
---
# <span data-ttu-id="65d09-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="65d09-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="65d09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65d09-102">SYNOPSIS</span></span>
<span data-ttu-id="65d09-103">Traffic Manager 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65d09-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65d09-105">설명은</span><span class="sxs-lookup"><span data-stu-id="65d09-105">DESCRIPTION</span></span>
<span data-ttu-id="65d09-106">**Set-AzureRmTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager의 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="65d09-107">이 cmdlet은 로컬 끝점 개체에서 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="65d09-108">*TrafficManagerEndpoint* 매개 변수를 사용 하거나 파이프라인을 사용 하 여 끝점 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="65d09-109">Get-AzureRmTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 나타내는 로컬 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="65d09-110">개체를 로컬로 수정한 다음 **Set-AzureRmTrafficManagerEndpoint** 를 사용 하 여 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="65d09-111">예제의</span><span class="sxs-lookup"><span data-stu-id="65d09-111">EXAMPLES</span></span>

### <span data-ttu-id="65d09-112">예제 1: 끝점 업데이트</span><span class="sxs-lookup"><span data-stu-id="65d09-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="65d09-113">첫 번째 명령은 **AzureRmTrafficManagerEndpoint** cmdlet을 사용 하 여 Azure Traffic Manager 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="65d09-114">명령은 $TrafficManagerEndpoint 변수에 로컬로 끝점을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="65d09-115">두 번째 명령은 해당 끝점을 로컬로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="65d09-116">이 명령은 끝점 가중치를 20으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="65d09-117">세 번째 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="65d09-118">변수</span><span class="sxs-lookup"><span data-stu-id="65d09-118">PARAMETERS</span></span>

### <span data-ttu-id="65d09-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d09-119">-DefaultProfile</span></span>
<span data-ttu-id="65d09-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65d09-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="65d09-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="65d09-122">로컬 **TrafficManagerEndpoint** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="65d09-123">이 cmdlet은이 로컬 개체와 일치 하도록 Traffic Manager를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d09-124">CommonParameters</span></span>
<span data-ttu-id="65d09-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d09-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d09-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d09-127">입력</span><span class="sxs-lookup"><span data-stu-id="65d09-127">INPUTS</span></span>

### <span data-ttu-id="65d09-128">TrafficManagerEndpoint (Network.)</span><span class="sxs-lookup"><span data-stu-id="65d09-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="65d09-129">이 cmdlet은 **TrafficManagerEndpoint** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="65d09-130">출력</span><span class="sxs-lookup"><span data-stu-id="65d09-130">OUTPUTS</span></span>

### <span data-ttu-id="65d09-131">TrafficManagerEndpoint (Network.)</span><span class="sxs-lookup"><span data-stu-id="65d09-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="65d09-132">이 cmdlet은 **TrafficManagerEndpoint** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="65d09-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="65d09-133">상속자</span><span class="sxs-lookup"><span data-stu-id="65d09-133">NOTES</span></span>

## <span data-ttu-id="65d09-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65d09-134">RELATED LINKS</span></span>

