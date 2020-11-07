---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 607da2e6478d72915497f1476e04ae11f9a69b9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699838"
---
# <span data-ttu-id="755bf-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="755bf-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="755bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="755bf-102">SYNOPSIS</span></span>
<span data-ttu-id="755bf-103">데이터 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="755bf-103">Updates a data source.</span></span>

## <span data-ttu-id="755bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="755bf-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="755bf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="755bf-105">DESCRIPTION</span></span>
<span data-ttu-id="755bf-106">**집합-AzOperationalInsightsDataSource** cmdlet은 데이터 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="755bf-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="755bf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="755bf-107">EXAMPLES</span></span>

## <span data-ttu-id="755bf-108">변수</span><span class="sxs-lookup"><span data-stu-id="755bf-108">PARAMETERS</span></span>

### <span data-ttu-id="755bf-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="755bf-109">-DataSource</span></span>
<span data-ttu-id="755bf-110">이 cmdlet이 업데이트 하는 데이터 원본을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="755bf-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="755bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755bf-111">-DefaultProfile</span></span>
<span data-ttu-id="755bf-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="755bf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="755bf-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755bf-113">CommonParameters</span></span>
<span data-ttu-id="755bf-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="755bf-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755bf-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="755bf-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755bf-116">입력</span><span class="sxs-lookup"><span data-stu-id="755bf-116">INPUTS</span></span>

### <span data-ttu-id="755bf-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="755bf-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="755bf-118">출력</span><span class="sxs-lookup"><span data-stu-id="755bf-118">OUTPUTS</span></span>

### <span data-ttu-id="755bf-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="755bf-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="755bf-120">상속자</span><span class="sxs-lookup"><span data-stu-id="755bf-120">NOTES</span></span>
* <span data-ttu-id="755bf-121">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="755bf-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="755bf-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="755bf-122">RELATED LINKS</span></span>

[<span data-ttu-id="755bf-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="755bf-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="755bf-124">제거-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="755bf-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


