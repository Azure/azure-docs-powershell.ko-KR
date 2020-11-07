---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 1de2d49d6e914635f8fc0d38ffa81755cc622481
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711110"
---
# <span data-ttu-id="1594f-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="1594f-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="1594f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1594f-102">SYNOPSIS</span></span>
<span data-ttu-id="1594f-103">IotHub의 할당량 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1594f-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1594f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1594f-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1594f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1594f-105">DESCRIPTION</span></span>
<span data-ttu-id="1594f-106">IotHub의 할당량 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1594f-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="1594f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1594f-107">EXAMPLES</span></span>

### <span data-ttu-id="1594f-108">예제 1 할당량 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="1594f-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1594f-109">"Myiothub" IotHub에 대 한 할당량 메트릭 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1594f-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="1594f-110">변수</span><span class="sxs-lookup"><span data-stu-id="1594f-110">PARAMETERS</span></span>

### <span data-ttu-id="1594f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1594f-111">-DefaultProfile</span></span>
<span data-ttu-id="1594f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1594f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1594f-113">-이름</span><span class="sxs-lookup"><span data-stu-id="1594f-113">-Name</span></span>
<span data-ttu-id="1594f-114">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1594f-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1594f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1594f-115">-ResourceGroupName</span></span>
<span data-ttu-id="1594f-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1594f-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1594f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1594f-117">CommonParameters</span></span>
<span data-ttu-id="1594f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1594f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1594f-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1594f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1594f-120">입력</span><span class="sxs-lookup"><span data-stu-id="1594f-120">INPUTS</span></span>

### <span data-ttu-id="1594f-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1594f-121">System.String</span></span>

## <span data-ttu-id="1594f-122">출력</span><span class="sxs-lookup"><span data-stu-id="1594f-122">OUTPUTS</span></span>

### <span data-ttu-id="1594f-123">IotHub. PSIotHubQuotaMetric/. \*</span><span class="sxs-lookup"><span data-stu-id="1594f-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="1594f-124">상속자</span><span class="sxs-lookup"><span data-stu-id="1594f-124">NOTES</span></span>

## <span data-ttu-id="1594f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1594f-125">RELATED LINKS</span></span>
