---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537135"
---
# <span data-ttu-id="9ba41-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="9ba41-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="9ba41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ba41-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba41-103">웹 서비스의 키를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ba41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ba41-104">SYNTAX</span></span>

### <span data-ttu-id="9ba41-105">이름과 리소스 그룹이 지정 된 Azure ML 웹 서비스의 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-105">Get an Azure ML web service's access keys given its name and resource group.</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ba41-106">지정 된 웹 서비스 인스턴스에 대 한 access kesy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-106">Get the access kesy for the given web service instance.</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ba41-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9ba41-107">DESCRIPTION</span></span>
<span data-ttu-id="9ba41-108">Azure 기계 학습 웹 서비스의 런타임 Api에 대 한 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="9ba41-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9ba41-109">EXAMPLES</span></span>

### <span data-ttu-id="9ba41-110">--------------------------예제 1-리소스 그룹 및 이름으로 지정 된 웹 서비스의 키 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="9ba41-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
<span data-ttu-id="9ba41-111">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="9ba41-111">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="9ba41-112">--------------------------예제 2-웹 서비스 인스턴스에 대 한 키 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="9ba41-112">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
<span data-ttu-id="9ba41-113">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="9ba41-113">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="9ba41-114">$mlService는 MachineLearning WebServices. i a m .와 같은 개체를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-114">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="9ba41-115">변수</span><span class="sxs-lookup"><span data-stu-id="9ba41-115">PARAMETERS</span></span>

### <span data-ttu-id="9ba41-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="9ba41-116">-MlWebService</span></span>
<span data-ttu-id="9ba41-117">선택 키가 검색 되는 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba41-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9ba41-118">-Name</span></span>
<span data-ttu-id="9ba41-119">선택 키가 검색 되는 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba41-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba41-120">-ResourceGroupName</span></span>
<span data-ttu-id="9ba41-121">웹 서비스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba41-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba41-122">-DefaultProfile</span></span>
<span data-ttu-id="9ba41-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ba41-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba41-124">CommonParameters</span></span>
<span data-ttu-id="9ba41-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba41-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ba41-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba41-127">입력</span><span class="sxs-lookup"><span data-stu-id="9ba41-127">INPUTS</span></span>

### <span data-ttu-id="9ba41-128">용</span><span class="sxs-lookup"><span data-stu-id="9ba41-128">WebService</span></span>
<span data-ttu-id="9ba41-129">' MlWebService ' 매개 변수는 파이프라인에서 ' WebService ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba41-129">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="9ba41-130">출력</span><span class="sxs-lookup"><span data-stu-id="9ba41-130">OUTPUTS</span></span>

### <span data-ttu-id="9ba41-131">않아야</span><span class="sxs-lookup"><span data-stu-id="9ba41-131">None</span></span>

## <span data-ttu-id="9ba41-132">상속자</span><span class="sxs-lookup"><span data-stu-id="9ba41-132">NOTES</span></span>
<span data-ttu-id="9ba41-133">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="9ba41-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="9ba41-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ba41-134">RELATED LINKS</span></span>

