---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: a0019b418fbf71a9b8010b4256a062a943244a9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531045"
---
# <span data-ttu-id="dc606-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="dc606-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="dc606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc606-102">SYNOPSIS</span></span>
<span data-ttu-id="dc606-103">웹 서비스의 키를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc606-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc606-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc606-104">SYNTAX</span></span>

### <span data-ttu-id="dc606-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dc606-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc606-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="dc606-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc606-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dc606-107">DESCRIPTION</span></span>
<span data-ttu-id="dc606-108">Azure 기계 학습 웹 서비스의 런타임 Api에 대 한 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc606-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="dc606-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dc606-109">EXAMPLES</span></span>

### <span data-ttu-id="dc606-110">--------------------------예제 1-리소스 그룹 및 이름으로 지정 된 웹 서비스의 키 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="dc606-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="dc606-111">--------------------------예제 2-웹 서비스 인스턴스에 대 한 키 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="dc606-111">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="dc606-112">$mlService는 MachineLearning WebServices. i a m .와 같은 개체를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc606-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="dc606-113">변수</span><span class="sxs-lookup"><span data-stu-id="dc606-113">PARAMETERS</span></span>

### <span data-ttu-id="dc606-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc606-114">-DefaultProfile</span></span>
<span data-ttu-id="dc606-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dc606-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc606-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="dc606-116">-MlWebService</span></span>
<span data-ttu-id="dc606-117">선택 키가 검색 되는 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc606-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: WebService
Parameter Sets: GetByInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc606-118">-이름</span><span class="sxs-lookup"><span data-stu-id="dc606-118">-Name</span></span>
<span data-ttu-id="dc606-119">선택 키가 검색 되는 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc606-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc606-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc606-120">-ResourceGroupName</span></span>
<span data-ttu-id="dc606-121">웹 서비스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="dc606-121">The resource group for the web service.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc606-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc606-122">CommonParameters</span></span>
<span data-ttu-id="dc606-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc606-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc606-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc606-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc606-125">입력</span><span class="sxs-lookup"><span data-stu-id="dc606-125">INPUTS</span></span>

### <span data-ttu-id="dc606-126">용</span><span class="sxs-lookup"><span data-stu-id="dc606-126">WebService</span></span>
<span data-ttu-id="dc606-127">' MlWebService ' 매개 변수는 파이프라인에서 ' WebService ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc606-127">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="dc606-128">출력</span><span class="sxs-lookup"><span data-stu-id="dc606-128">OUTPUTS</span></span>

### <span data-ttu-id="dc606-129">않아야</span><span class="sxs-lookup"><span data-stu-id="dc606-129">None</span></span>

## <span data-ttu-id="dc606-130">상속자</span><span class="sxs-lookup"><span data-stu-id="dc606-130">NOTES</span></span>
<span data-ttu-id="dc606-131">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="dc606-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dc606-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc606-132">RELATED LINKS</span></span>

