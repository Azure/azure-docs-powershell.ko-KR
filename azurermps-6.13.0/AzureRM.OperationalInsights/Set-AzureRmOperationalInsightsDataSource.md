---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5bf4f178ee3343b5100dad87836c3215fba4cfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534220"
---
# <span data-ttu-id="fc45a-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="fc45a-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="fc45a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc45a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc45a-103">데이터 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc45a-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc45a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc45a-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc45a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fc45a-105">DESCRIPTION</span></span>
<span data-ttu-id="fc45a-106">**집합-AzureRmOperationalInsightsDataSource** cmdlet은 데이터 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc45a-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="fc45a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fc45a-107">EXAMPLES</span></span>

## <span data-ttu-id="fc45a-108">변수</span><span class="sxs-lookup"><span data-stu-id="fc45a-108">PARAMETERS</span></span>

### <span data-ttu-id="fc45a-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="fc45a-109">-DataSource</span></span>
<span data-ttu-id="fc45a-110">이 cmdlet이 업데이트 하는 데이터 원본을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc45a-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc45a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc45a-111">-DefaultProfile</span></span>
<span data-ttu-id="fc45a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fc45a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc45a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc45a-113">CommonParameters</span></span>
<span data-ttu-id="fc45a-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc45a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc45a-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc45a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc45a-116">입력</span><span class="sxs-lookup"><span data-stu-id="fc45a-116">INPUTS</span></span>

### <span data-ttu-id="fc45a-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fc45a-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>
<span data-ttu-id="fc45a-118">매개 변수: DataSource (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fc45a-118">Parameters: DataSource (ByValue)</span></span>

## <span data-ttu-id="fc45a-119">출력</span><span class="sxs-lookup"><span data-stu-id="fc45a-119">OUTPUTS</span></span>

### <span data-ttu-id="fc45a-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fc45a-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fc45a-121">상속자</span><span class="sxs-lookup"><span data-stu-id="fc45a-121">NOTES</span></span>
* <span data-ttu-id="fc45a-122">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="fc45a-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="fc45a-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc45a-123">RELATED LINKS</span></span>

[<span data-ttu-id="fc45a-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="fc45a-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="fc45a-125">제거-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="fc45a-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


