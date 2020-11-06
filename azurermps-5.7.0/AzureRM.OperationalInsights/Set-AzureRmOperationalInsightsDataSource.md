---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e45dcbfad9b4b92695f310d7d2c56fc46fc57bd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525071"
---
# <span data-ttu-id="bd027-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="bd027-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="bd027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd027-102">SYNOPSIS</span></span>
<span data-ttu-id="bd027-103">데이터 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd027-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd027-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bd027-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd027-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bd027-105">DESCRIPTION</span></span>
<span data-ttu-id="bd027-106">**집합-AzureRmOperationalInsightsDataSource** cmdlet은 데이터 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd027-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="bd027-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bd027-107">EXAMPLES</span></span>

## <span data-ttu-id="bd027-108">변수</span><span class="sxs-lookup"><span data-stu-id="bd027-108">PARAMETERS</span></span>

### <span data-ttu-id="bd027-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="bd027-109">-DataSource</span></span>
<span data-ttu-id="bd027-110">이 cmdlet이 업데이트 하는 데이터 원본을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd027-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: PSDataSource
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd027-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd027-111">-DefaultProfile</span></span>
<span data-ttu-id="bd027-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bd027-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd027-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd027-113">CommonParameters</span></span>
<span data-ttu-id="bd027-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd027-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd027-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd027-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd027-116">입력</span><span class="sxs-lookup"><span data-stu-id="bd027-116">INPUTS</span></span>

### <span data-ttu-id="bd027-117">PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bd027-117">PSDataSource</span></span>
<span data-ttu-id="bd027-118">' DataSource ' 매개 변수는 파이프라인에서 ' PSDataSource ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd027-118">Parameter 'DataSource' accepts value of type 'PSDataSource' from the pipeline</span></span>

## <span data-ttu-id="bd027-119">출력</span><span class="sxs-lookup"><span data-stu-id="bd027-119">OUTPUTS</span></span>

### <span data-ttu-id="bd027-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bd027-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bd027-121">상속자</span><span class="sxs-lookup"><span data-stu-id="bd027-121">NOTES</span></span>
* <span data-ttu-id="bd027-122">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="bd027-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="bd027-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd027-123">RELATED LINKS</span></span>

[<span data-ttu-id="bd027-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="bd027-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="bd027-125">제거-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="bd027-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


