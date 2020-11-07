---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 31201d607d1b9f0825236fe162bf86028b148193
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874424"
---
# <span data-ttu-id="2e91a-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e91a-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="2e91a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e91a-102">SYNOPSIS</span></span>
<span data-ttu-id="2e91a-103">Traffic Manager 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="2e91a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e91a-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e91a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2e91a-105">DESCRIPTION</span></span>
<span data-ttu-id="2e91a-106">**Set-AzTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager의 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="2e91a-107">이 cmdlet은 로컬 끝점 개체에서 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="2e91a-108">*TrafficManagerEndpoint* 매개 변수를 사용 하거나 파이프라인을 사용 하 여 끝점 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="2e91a-109">Get-AzTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 나타내는 로컬 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="2e91a-110">개체를 로컬로 수정한 다음 **Set-AzTrafficManagerEndpoint** 를 사용 하 여 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="2e91a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2e91a-111">EXAMPLES</span></span>

### <span data-ttu-id="2e91a-112">예제 1: 끝점 업데이트</span><span class="sxs-lookup"><span data-stu-id="2e91a-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="2e91a-113">첫 번째 명령은 **AzTrafficManagerEndpoint** cmdlet을 사용 하 여 Azure Traffic Manager 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="2e91a-114">명령은 $TrafficManagerEndpoint 변수에 로컬로 끝점을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="2e91a-115">두 번째 명령은 해당 끝점을 로컬로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="2e91a-116">이 명령은 끝점 가중치를 20으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="2e91a-117">세 번째 명령은 $TrafficManagerEndpoint의 로컬 값과 일치 하도록 Traffic Manager에서 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="2e91a-118">변수</span><span class="sxs-lookup"><span data-stu-id="2e91a-118">PARAMETERS</span></span>

### <span data-ttu-id="2e91a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e91a-119">-DefaultProfile</span></span>
<span data-ttu-id="2e91a-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e91a-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e91a-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="2e91a-122">로컬 **TrafficManagerEndpoint** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="2e91a-123">이 cmdlet은이 로컬 개체와 일치 하도록 Traffic Manager를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="2e91a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e91a-124">CommonParameters</span></span>
<span data-ttu-id="2e91a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e91a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e91a-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e91a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e91a-127">입력</span><span class="sxs-lookup"><span data-stu-id="2e91a-127">INPUTS</span></span>

### <span data-ttu-id="2e91a-128">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="2e91a-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2e91a-129">출력</span><span class="sxs-lookup"><span data-stu-id="2e91a-129">OUTPUTS</span></span>

### <span data-ttu-id="2e91a-130">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="2e91a-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2e91a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="2e91a-131">NOTES</span></span>

## <span data-ttu-id="2e91a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e91a-132">RELATED LINKS</span></span>
