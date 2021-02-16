---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187524"
---
# <span data-ttu-id="02f7d-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="02f7d-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="02f7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="02f7d-103">웹 서비스의 키를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="02f7d-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="02f7d-104">구문</span><span class="sxs-lookup"><span data-stu-id="02f7d-104">SYNTAX</span></span>

### <span data-ttu-id="02f7d-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="02f7d-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02f7d-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="02f7d-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02f7d-107">설명</span><span class="sxs-lookup"><span data-stu-id="02f7d-107">DESCRIPTION</span></span>
<span data-ttu-id="02f7d-108">Azure Machine Learning 웹 서비스의 런타임 API에 대한 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="02f7d-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="02f7d-109">예제</span><span class="sxs-lookup"><span data-stu-id="02f7d-109">EXAMPLES</span></span>

### <span data-ttu-id="02f7d-110">예제 1 - 리소스 그룹 및 이름으로 지정된 웹 서비스의 키 얻기</span><span class="sxs-lookup"><span data-stu-id="02f7d-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="02f7d-111">예제 2 - 웹 서비스 인스턴스에 대한 키 얻기</span><span class="sxs-lookup"><span data-stu-id="02f7d-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="02f7d-112">$mlService Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService 형식의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02f7d-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="02f7d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02f7d-113">PARAMETERS</span></span>

### <span data-ttu-id="02f7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f7d-114">-DefaultProfile</span></span>
<span data-ttu-id="02f7d-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="02f7d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02f7d-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="02f7d-116">-MlWebService</span></span>
<span data-ttu-id="02f7d-117">액세스 키를 검색할 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02f7d-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="02f7d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="02f7d-118">-Name</span></span>
<span data-ttu-id="02f7d-119">액세스 키를 검색할 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02f7d-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="02f7d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f7d-120">-ResourceGroupName</span></span>
<span data-ttu-id="02f7d-121">웹 서비스에 대한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="02f7d-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="02f7d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f7d-122">CommonParameters</span></span>
<span data-ttu-id="02f7d-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02f7d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f7d-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="02f7d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f7d-125">입력</span><span class="sxs-lookup"><span data-stu-id="02f7d-125">INPUTS</span></span>

### <span data-ttu-id="02f7d-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="02f7d-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="02f7d-127">출력</span><span class="sxs-lookup"><span data-stu-id="02f7d-127">OUTPUTS</span></span>

### <span data-ttu-id="02f7d-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="02f7d-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="02f7d-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02f7d-129">NOTES</span></span>
<span data-ttu-id="02f7d-130">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="02f7d-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="02f7d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02f7d-131">RELATED LINKS</span></span>
