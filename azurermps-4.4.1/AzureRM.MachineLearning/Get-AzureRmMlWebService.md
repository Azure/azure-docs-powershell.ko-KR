---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537143"
---
# <span data-ttu-id="7f7db-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="7f7db-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="7f7db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f7db-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7db-103">하나 이상의 웹 서비스에 대 한 요약 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f7db-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f7db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f7db-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f7db-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7f7db-105">DESCRIPTION</span></span>
<span data-ttu-id="7f7db-106">웹 서비스 정의 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f7db-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="7f7db-107">Paramenters에 따라 cmdlet은 현재 구독 내의 지정 된 리소스 그룹에 대 한 웹 서비스에 대 한 정의 또는 현재 구독 내의 웹 서비스에 대 한 특별 한 컬렉션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f7db-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="7f7db-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7f7db-108">EXAMPLES</span></span>

### <span data-ttu-id="7f7db-109">--------------------------예제 1: 특정 웹 서비스에 대 한 세부 정보 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f7db-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
<span data-ttu-id="7f7db-110">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7f7db-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="7f7db-111">--------------------------예제 2: 현재 구독에서 모든 웹 서비스 리소스 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f7db-111">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
<span data-ttu-id="7f7db-112">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7f7db-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService
```

### <span data-ttu-id="7f7db-113">--------------------------예제 3: 현재 구독 및 지정 된 리소스 그룹의 모든 웹 서비스 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f7db-113">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="7f7db-114">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7f7db-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="7f7db-115">변수</span><span class="sxs-lookup"><span data-stu-id="7f7db-115">PARAMETERS</span></span>

### <span data-ttu-id="7f7db-116">-이름</span><span class="sxs-lookup"><span data-stu-id="7f7db-116">-Name</span></span>
<span data-ttu-id="7f7db-117">세부 정보가 검색 되는 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f7db-117">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="7f7db-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f7db-118">-ResourceGroupName</span></span>
<span data-ttu-id="7f7db-119">웹 서비스에 대 한 세부 정보가 검색 되는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="7f7db-119">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="7f7db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7db-120">-DefaultProfile</span></span>
<span data-ttu-id="7f7db-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f7db-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f7db-122">-지역</span><span class="sxs-lookup"><span data-stu-id="7f7db-122">-Region</span></span>
<span data-ttu-id="7f7db-123">지역 이름</span><span class="sxs-lookup"><span data-stu-id="7f7db-123">The name of region</span></span>

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

### <span data-ttu-id="7f7db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7db-124">CommonParameters</span></span>
<span data-ttu-id="7f7db-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f7db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7db-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f7db-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7db-127">입력</span><span class="sxs-lookup"><span data-stu-id="7f7db-127">INPUTS</span></span>

## <span data-ttu-id="7f7db-128">출력</span><span class="sxs-lookup"><span data-stu-id="7f7db-128">OUTPUTS</span></span>

### <span data-ttu-id="7f7db-129">않아야</span><span class="sxs-lookup"><span data-stu-id="7f7db-129">None</span></span>

## <span data-ttu-id="7f7db-130">상속자</span><span class="sxs-lookup"><span data-stu-id="7f7db-130">NOTES</span></span>
<span data-ttu-id="7f7db-131">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="7f7db-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7f7db-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f7db-132">RELATED LINKS</span></span>

