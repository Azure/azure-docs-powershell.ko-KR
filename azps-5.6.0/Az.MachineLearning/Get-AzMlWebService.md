---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: 1dcf881fbe0a3a616a7522236099f7698b50a1a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007776"
---
# <span data-ttu-id="f8957-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="f8957-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="f8957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8957-102">SYNOPSIS</span></span>
<span data-ttu-id="f8957-103">하나 이상의 웹 서비스에 대한 요약 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f8957-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="f8957-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8957-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8957-105">설명</span><span class="sxs-lookup"><span data-stu-id="f8957-105">DESCRIPTION</span></span>
<span data-ttu-id="f8957-106">웹 서비스 정의 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f8957-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="f8957-107">전달된 매개 변수에 따라 cmdlet은 특정 웹 서비스에 대한 정의, 현재 구독 내의 지정된 리소스 그룹에 대한 웹 서비스에 대한 정의 컬렉션 또는 현재 구독 내의 웹 서비스에 대한 정의 컬렉션을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f8957-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="f8957-108">예제</span><span class="sxs-lookup"><span data-stu-id="f8957-108">EXAMPLES</span></span>

### <span data-ttu-id="f8957-109">예제 1: 특정 웹 서비스의 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="f8957-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="f8957-110">예제 2: 현재 구독의 모든 웹 서비스 리소스 사용</span><span class="sxs-lookup"><span data-stu-id="f8957-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="f8957-111">예제 3: 현재 구독 및 주어진 리소스 그룹의 모든 웹 서비스 사용</span><span class="sxs-lookup"><span data-stu-id="f8957-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="f8957-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f8957-112">PARAMETERS</span></span>

### <span data-ttu-id="f8957-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8957-113">-DefaultProfile</span></span>
<span data-ttu-id="f8957-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f8957-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8957-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f8957-115">-Name</span></span>
<span data-ttu-id="f8957-116">세부 정보를 검색하는 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8957-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="f8957-117">-Region</span><span class="sxs-lookup"><span data-stu-id="f8957-117">-Region</span></span>
<span data-ttu-id="f8957-118">지역 이름</span><span class="sxs-lookup"><span data-stu-id="f8957-118">The name of region</span></span>

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

### <span data-ttu-id="f8957-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8957-119">-ResourceGroupName</span></span>
<span data-ttu-id="f8957-120">웹 서비스에 대한 세부 정보를 검색하는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f8957-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="f8957-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8957-121">CommonParameters</span></span>
<span data-ttu-id="f8957-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8957-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8957-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f8957-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8957-124">입력</span><span class="sxs-lookup"><span data-stu-id="f8957-124">INPUTS</span></span>

### <span data-ttu-id="f8957-125">없음</span><span class="sxs-lookup"><span data-stu-id="f8957-125">None</span></span>

## <span data-ttu-id="f8957-126">출력</span><span class="sxs-lookup"><span data-stu-id="f8957-126">OUTPUTS</span></span>

### <span data-ttu-id="f8957-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="f8957-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f8957-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8957-128">NOTES</span></span>
<span data-ttu-id="f8957-129">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="f8957-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f8957-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8957-130">RELATED LINKS</span></span>
