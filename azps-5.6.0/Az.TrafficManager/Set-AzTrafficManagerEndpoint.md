---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987238"
---
# <span data-ttu-id="3a340-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a340-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="3a340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a340-102">SYNOPSIS</span></span>
<span data-ttu-id="3a340-103">Traffic Manager 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="3a340-104">구문</span><span class="sxs-lookup"><span data-stu-id="3a340-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a340-105">설명</span><span class="sxs-lookup"><span data-stu-id="3a340-105">DESCRIPTION</span></span>
<span data-ttu-id="3a340-106">**Set-AzTrafficManagerEndpoint** cmdlet은 Azure Traffic Manager의 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="3a340-107">이 cmdlet은 로컬 엔드포인트 개체의 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="3a340-108">*TrafficManagerEndpoint* 매개 변수를 사용하거나 파이프라인을 사용하여 엔드포인트 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="3a340-109">Get-AzTrafficManagerEndpoint cmdlet을 사용하여 엔드포인트를 나타내는 로컬 개체를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="3a340-110">개체를 로컬로 수정한 다음 **Set-AzTrafficManagerEndpoint를** 사용하여 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="3a340-111">예제</span><span class="sxs-lookup"><span data-stu-id="3a340-111">EXAMPLES</span></span>

### <span data-ttu-id="3a340-112">예제 1: 엔드포인트 업데이트</span><span class="sxs-lookup"><span data-stu-id="3a340-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="3a340-113">첫 번째 명령은 **Get-AzTrafficManagerEndpoint** cmdlet을 사용하여 Azure Traffic Manager 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="3a340-114">명령은 엔드포인트를 로컬로 $TrafficManagerEndpoint 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="3a340-115">두 번째 명령은 로컬로 엔드포인트를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="3a340-116">이 명령은 엔드포인트 가중치를 20으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="3a340-117">세 번째 명령은 Traffic Manager의 엔드포인트를 업데이트하여 로컬 값과 $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3a340-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="3a340-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3a340-118">PARAMETERS</span></span>

### <span data-ttu-id="3a340-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a340-119">-DefaultProfile</span></span>
<span data-ttu-id="3a340-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a340-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a340-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="3a340-122">로컬 **TrafficManagerEndpoint 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="3a340-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="3a340-123">이 cmdlet은 Traffic Manager를 업데이트하여 이 로컬 개체와 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a340-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a340-124">CommonParameters</span></span>
<span data-ttu-id="3a340-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a340-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a340-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3a340-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a340-127">입력</span><span class="sxs-lookup"><span data-stu-id="3a340-127">INPUTS</span></span>

### <span data-ttu-id="3a340-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a340-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="3a340-129">출력</span><span class="sxs-lookup"><span data-stu-id="3a340-129">OUTPUTS</span></span>

### <span data-ttu-id="3a340-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a340-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="3a340-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a340-131">NOTES</span></span>

## <span data-ttu-id="3a340-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a340-132">RELATED LINKS</span></span>
