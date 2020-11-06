---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 79fa1522ed0eec95a1e388ed5d113cf98ad7f525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533544"
---
# <span data-ttu-id="1eb5a-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1eb5a-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="1eb5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eb5a-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb5a-103">미리 정의 된 Azure 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eb5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1eb5a-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eb5a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1eb5a-105">DESCRIPTION</span></span>
<span data-ttu-id="1eb5a-106">**AzureRmTag** cmdlet은 구독에서 미리 정의 된 Azure 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="1eb5a-107">이 cmdlet은 태그에 대 한 기본 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="1eb5a-108">모든 출력 개체에는 태그와 값이 적용 된 리소스 및 리소스 그룹 수를 나타내는 Count 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>

<span data-ttu-id="1eb5a-109">**AzureRMTag** 의 일부인 azure tags 모듈은 미리 정의 된 Azure 태그를 관리 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="1eb5a-110">Azure 태그는 사용자가 Azure 리소스 및 리소스 그룹 (예: 부서나 비용 센터)을 분류 하거나 리소스 및 그룹에 대 한 메모 또는 설명을 추적 하는 데 사용할 수 있는 이름-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="1eb5a-111">한 단계에서 태그를 정의 하 고 적용할 수 있지만, 미리 정의 된 태그를 사용 하면 구독의 태그에 대 한 표준, 일관성, 예측 가능한 이름 및 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="1eb5a-112">구독에 미리 정의 된 태그가 포함 되어 있는 경우에는 구독에 있는 리소스나 리소스 그룹에 정의 되지 않은 태그나 값을 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-112">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="1eb5a-113">미리 정의 된 태그를 만들려면 New-AzureRmTag cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-113">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="1eb5a-114">리소스 그룹에 미리 정의 된 태그를 적용 하려면 New-AzureRmTag cmdlet의 *tag* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-114">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="1eb5a-115">특정 태그 이름 또는 이름과 값에 대 한 리소스 그룹을 검색 하려면 Get-AzureRMResourceGroup cmdlet의 *tag* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-115">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="1eb5a-116">예제의</span><span class="sxs-lookup"><span data-stu-id="1eb5a-116">EXAMPLES</span></span>

### <span data-ttu-id="1eb5a-117">예제 1: 미리 정의 된 모든 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="1eb5a-117">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="1eb5a-118">이 명령은 구독에서 미리 정의 된 모든 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-118">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="1eb5a-119">Count 속성에는 구독의 리소스 및 리소스 그룹에 태그가 적용 된 횟수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-119">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="1eb5a-120">예제 2: 이름으로 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="1eb5a-120">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="1eb5a-121">이 명령은 부서 태그 및 해당 값에 대 한 자세한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-121">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="1eb5a-122">Count 속성은 태그 및 각 값이 구독의 리소스 및 리소스 그룹에 적용 된 횟수를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-122">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="1eb5a-123">예제 3: 모든 태그 값 가져오기</span><span class="sxs-lookup"><span data-stu-id="1eb5a-123">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzureRmTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="1eb5a-124">이 명령은 *자세한* 매개 변수를 사용 하 여 구독에 미리 정의 된 모든 태그에 대 한 자세한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-124">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="1eb5a-125">*자세한* 매개 변수를 사용 하는 것은 모든 태그에 *Name* 매개 변수를 사용 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-125">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="1eb5a-126">변수</span><span class="sxs-lookup"><span data-stu-id="1eb5a-126">PARAMETERS</span></span>

### <span data-ttu-id="1eb5a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb5a-127">-DefaultProfile</span></span>
<span data-ttu-id="1eb5a-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1eb5a-129">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="1eb5a-129">-Detailed</span></span>
<span data-ttu-id="1eb5a-130">이 작업이 태그 값에 대 한 정보를 출력에 추가 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-130">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb5a-131">-이름</span><span class="sxs-lookup"><span data-stu-id="1eb5a-131">-Name</span></span>
<span data-ttu-id="1eb5a-132">가져올 태그의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-132">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="1eb5a-133">기본적으로 **AzureRmTag** 에서는 구독에 있는 모든 미리 정의 된 태그에 대 한 기본 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-133">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="1eb5a-134">*Name* 매개 변수를 지정 하면 *Detailed* 매개 변수는 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-134">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb5a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb5a-135">CommonParameters</span></span>
<span data-ttu-id="1eb5a-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb5a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb5a-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eb5a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb5a-138">입력</span><span class="sxs-lookup"><span data-stu-id="1eb5a-138">INPUTS</span></span>

### <span data-ttu-id="1eb5a-139">않아야</span><span class="sxs-lookup"><span data-stu-id="1eb5a-139">None</span></span>

## <span data-ttu-id="1eb5a-140">출력</span><span class="sxs-lookup"><span data-stu-id="1eb5a-140">OUTPUTS</span></span>

### <span data-ttu-id="1eb5a-141">PSTag, Microsoft Azure. Commands.. m a m</span><span class="sxs-lookup"><span data-stu-id="1eb5a-141">Microsoft.Azure.Commands.Tags.Model.PSTag, Microsoft.Azure.Commands.Tags</span></span>

## <span data-ttu-id="1eb5a-142">상속자</span><span class="sxs-lookup"><span data-stu-id="1eb5a-142">NOTES</span></span>

## <span data-ttu-id="1eb5a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1eb5a-143">RELATED LINKS</span></span>

[<span data-ttu-id="1eb5a-144">새로운 AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1eb5a-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="1eb5a-145">제거-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1eb5a-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


