---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372093"
---
# <span data-ttu-id="5ba01-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5ba01-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="5ba01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ba01-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba01-103">데이터 원본을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba01-103">Updates a data source.</span></span>

## <span data-ttu-id="5ba01-104">구문</span><span class="sxs-lookup"><span data-stu-id="5ba01-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ba01-105">설명</span><span class="sxs-lookup"><span data-stu-id="5ba01-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba01-106">**Set-AzOperationalInsightsDataSource** cmdlet은 데이터 원본을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba01-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="5ba01-107">예제</span><span class="sxs-lookup"><span data-stu-id="5ba01-107">EXAMPLES</span></span>

## <span data-ttu-id="5ba01-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ba01-108">PARAMETERS</span></span>

### <span data-ttu-id="5ba01-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="5ba01-109">-DataSource</span></span>
<span data-ttu-id="5ba01-110">이 cmdlet이 업데이트하는 데이터 원본을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba01-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="5ba01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba01-111">-DefaultProfile</span></span>
<span data-ttu-id="5ba01-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5ba01-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ba01-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba01-113">CommonParameters</span></span>
<span data-ttu-id="5ba01-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5ba01-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba01-115">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5ba01-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba01-116">입력</span><span class="sxs-lookup"><span data-stu-id="5ba01-116">INPUTS</span></span>

### <span data-ttu-id="5ba01-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5ba01-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5ba01-118">출력</span><span class="sxs-lookup"><span data-stu-id="5ba01-118">OUTPUTS</span></span>

### <span data-ttu-id="5ba01-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5ba01-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5ba01-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5ba01-120">NOTES</span></span>
* <span data-ttu-id="5ba01-121">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 운영, 인사이트</span><span class="sxs-lookup"><span data-stu-id="5ba01-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5ba01-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ba01-122">RELATED LINKS</span></span>

[<span data-ttu-id="5ba01-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5ba01-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="5ba01-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5ba01-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


