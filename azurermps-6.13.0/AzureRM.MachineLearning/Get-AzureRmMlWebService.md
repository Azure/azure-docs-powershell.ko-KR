---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 5632de726797dd36af377f76b5919590c5826606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530245"
---
# <span data-ttu-id="c489b-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="c489b-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="c489b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c489b-102">SYNOPSIS</span></span>
<span data-ttu-id="c489b-103">하나 이상의 웹 서비스에 대 한 요약 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c489b-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c489b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c489b-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c489b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c489b-105">DESCRIPTION</span></span>
<span data-ttu-id="c489b-106">웹 서비스 정의 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c489b-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="c489b-107">Paramenters에 따라 cmdlet은 현재 구독 내의 지정 된 리소스 그룹에 대 한 웹 서비스에 대 한 정의 또는 현재 구독 내의 웹 서비스에 대 한 특별 한 컬렉션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c489b-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="c489b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c489b-108">EXAMPLES</span></span>

### <span data-ttu-id="c489b-109">예제 1: 특정 웹 서비스의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="c489b-109">Example 1: Get details of specific web service</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="c489b-110">예제 2: 현재 구독에서 모든 웹 서비스 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="c489b-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzureRmMlWebService
```

### <span data-ttu-id="c489b-111">예제 3: 현재 구독 및 지정 된 리소스 그룹의 모든 웹 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="c489b-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="c489b-112">변수</span><span class="sxs-lookup"><span data-stu-id="c489b-112">PARAMETERS</span></span>

### <span data-ttu-id="c489b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c489b-113">-DefaultProfile</span></span>
<span data-ttu-id="c489b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c489b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c489b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c489b-115">-Name</span></span>
<span data-ttu-id="c489b-116">세부 정보가 검색 되는 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c489b-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="c489b-117">-지역</span><span class="sxs-lookup"><span data-stu-id="c489b-117">-Region</span></span>
<span data-ttu-id="c489b-118">Regio의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c489b-118">The name of regio</span></span>

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

### <span data-ttu-id="c489b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c489b-119">-ResourceGroupName</span></span>
<span data-ttu-id="c489b-120">웹 서비스에 대 한 세부 정보가 검색 되는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="c489b-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="c489b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c489b-121">CommonParameters</span></span>
<span data-ttu-id="c489b-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c489b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c489b-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c489b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c489b-124">입력</span><span class="sxs-lookup"><span data-stu-id="c489b-124">INPUTS</span></span>

### <span data-ttu-id="c489b-125">않아야</span><span class="sxs-lookup"><span data-stu-id="c489b-125">None</span></span>

## <span data-ttu-id="c489b-126">출력</span><span class="sxs-lookup"><span data-stu-id="c489b-126">OUTPUTS</span></span>

### <span data-ttu-id="c489b-127">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="c489b-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="c489b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="c489b-128">NOTES</span></span>
<span data-ttu-id="c489b-129">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="c489b-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c489b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c489b-130">RELATED LINKS</span></span>