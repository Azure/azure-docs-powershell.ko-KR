---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 952cf5d9f0eff288a65df2dd2917d341582237db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535992"
---
# <span data-ttu-id="ca0b2-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="ca0b2-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="ca0b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0b2-103">IotHub의 할당량 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca0b2-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca0b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca0b2-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca0b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ca0b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ca0b2-106">IotHub의 할당량 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca0b2-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="ca0b2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ca0b2-107">EXAMPLES</span></span>

### <span data-ttu-id="ca0b2-108">예제 1 할당량 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="ca0b2-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ca0b2-109">"Myiothub" IotHub에 대 한 할당량 메트릭 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca0b2-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ca0b2-110">변수</span><span class="sxs-lookup"><span data-stu-id="ca0b2-110">PARAMETERS</span></span>

### <span data-ttu-id="ca0b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca0b2-111">-DefaultProfile</span></span>
<span data-ttu-id="ca0b2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ca0b2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca0b2-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ca0b2-113">-Name</span></span>
<span data-ttu-id="ca0b2-114">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca0b2-114">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0b2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca0b2-115">-ResourceGroupName</span></span>
<span data-ttu-id="ca0b2-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ca0b2-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0b2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0b2-117">CommonParameters</span></span>
<span data-ttu-id="ca0b2-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca0b2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0b2-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca0b2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0b2-120">입력</span><span class="sxs-lookup"><span data-stu-id="ca0b2-120">INPUTS</span></span>

### <span data-ttu-id="ca0b2-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ca0b2-121">System.String</span></span>

## <span data-ttu-id="ca0b2-122">출력</span><span class="sxs-lookup"><span data-stu-id="ca0b2-122">OUTPUTS</span></span>

### <span data-ttu-id="ca0b2-123">PSIotHubQuotaMetric, IotHub, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]] 목록에 List ' 1 [[[;]. 목록이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca0b2-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ca0b2-124">상속자</span><span class="sxs-lookup"><span data-stu-id="ca0b2-124">NOTES</span></span>

## <span data-ttu-id="ca0b2-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca0b2-125">RELATED LINKS</span></span>

