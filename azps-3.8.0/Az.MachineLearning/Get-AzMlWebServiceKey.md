---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878462"
---
# <span data-ttu-id="3d244-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="3d244-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="3d244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d244-102">SYNOPSIS</span></span>
<span data-ttu-id="3d244-103">웹 서비스의 키를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d244-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="3d244-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d244-104">SYNTAX</span></span>

### <span data-ttu-id="3d244-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3d244-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d244-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="3d244-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d244-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3d244-107">DESCRIPTION</span></span>
<span data-ttu-id="3d244-108">Azure 기계 학습 웹 서비스의 런타임 Api에 대 한 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d244-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="3d244-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3d244-109">EXAMPLES</span></span>

### <span data-ttu-id="3d244-110">예제 1-리소스 그룹 및 이름으로 지정 된 웹 서비스의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3d244-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="3d244-111">예제 2-웹 서비스 인스턴스에 대 한 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3d244-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="3d244-112">$mlService는 MachineLearning WebServices. i a m .와 같은 개체를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d244-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="3d244-113">변수</span><span class="sxs-lookup"><span data-stu-id="3d244-113">PARAMETERS</span></span>

### <span data-ttu-id="3d244-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d244-114">-DefaultProfile</span></span>
<span data-ttu-id="3d244-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3d244-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d244-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="3d244-116">-MlWebService</span></span>
<span data-ttu-id="3d244-117">선택 키가 검색 되는 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d244-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d244-118">-이름</span><span class="sxs-lookup"><span data-stu-id="3d244-118">-Name</span></span>
<span data-ttu-id="3d244-119">선택 키가 검색 되는 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d244-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d244-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d244-120">-ResourceGroupName</span></span>
<span data-ttu-id="3d244-121">웹 서비스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3d244-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d244-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d244-122">CommonParameters</span></span>
<span data-ttu-id="3d244-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d244-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d244-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d244-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d244-125">입력</span><span class="sxs-lookup"><span data-stu-id="3d244-125">INPUTS</span></span>

### <span data-ttu-id="3d244-126">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="3d244-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="3d244-127">출력</span><span class="sxs-lookup"><span data-stu-id="3d244-127">OUTPUTS</span></span>

### <span data-ttu-id="3d244-128">MachineLearning. WebServices-. m m m 키</span><span class="sxs-lookup"><span data-stu-id="3d244-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="3d244-129">상속자</span><span class="sxs-lookup"><span data-stu-id="3d244-129">NOTES</span></span>
<span data-ttu-id="3d244-130">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="3d244-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3d244-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d244-131">RELATED LINKS</span></span>
