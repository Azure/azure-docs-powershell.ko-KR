---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 945af88df11e210c3af3a11bd69123dd32befe4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536479"
---
# <span data-ttu-id="6a20f-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="6a20f-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="6a20f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a20f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a20f-103">미리 정의 된 Azure 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a20f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a20f-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a20f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6a20f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a20f-106">**AzureRmTag** cmdlet은 구독에서 미리 정의 된 Azure 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="6a20f-107">이 cmdlet은 태그에 대 한 기본 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="6a20f-108">모든 출력 개체에는 태그와 값이 적용 된 리소스 및 리소스 그룹 수를 나타내는 Count 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="6a20f-109">**AzureRMTag** 의 일부인 azure tags 모듈은 미리 정의 된 Azure 태그를 관리 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="6a20f-110">Azure 태그는 사용자가 Azure 리소스 및 리소스 그룹 (예: 부서나 비용 센터)을 분류 하거나 리소스 및 그룹에 대 한 메모 또는 설명을 추적 하는 데 사용할 수 있는 이름-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="6a20f-111">한 단계에서 태그를 정의 하 고 적용할 수 있지만, 미리 정의 된 태그를 사용 하면 구독의 태그에 대 한 표준, 일관성, 예측 가능한 이름 및 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="6a20f-112">미리 정의 된 태그를 만들려면 New-AzureRmTag cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-112">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="6a20f-113">리소스 그룹에 미리 정의 된 태그를 적용 하려면 New-AzureRmTag cmdlet의 *tag* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="6a20f-114">특정 태그 이름 또는 이름과 값에 대 한 리소스 그룹을 검색 하려면 Get-AzureRMResourceGroup cmdlet의 *tag* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="6a20f-115">예제의</span><span class="sxs-lookup"><span data-stu-id="6a20f-115">EXAMPLES</span></span>

### <span data-ttu-id="6a20f-116">예제 1: 미리 정의 된 모든 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="6a20f-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="6a20f-117">이 명령은 구독에서 미리 정의 된 모든 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="6a20f-118">Count 속성에는 구독의 리소스 및 리소스 그룹에 태그가 적용 된 횟수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="6a20f-119">예제 2: 이름으로 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="6a20f-119">Example 2: Get a tag by name</span></span>
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

<span data-ttu-id="6a20f-120">이 명령은 부서 태그 및 해당 값에 대 한 자세한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="6a20f-121">Count 속성은 태그 및 각 값이 구독의 리소스 및 리소스 그룹에 적용 된 횟수를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="6a20f-122">예제 3: 모든 태그 값 가져오기</span><span class="sxs-lookup"><span data-stu-id="6a20f-122">Example 3: Get values of all tags</span></span>
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

<span data-ttu-id="6a20f-123">이 명령은 *자세한* 매개 변수를 사용 하 여 구독에 미리 정의 된 모든 태그에 대 한 자세한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="6a20f-124">*자세한* 매개 변수를 사용 하는 것은 모든 태그에 *Name* 매개 변수를 사용 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="6a20f-125">변수</span><span class="sxs-lookup"><span data-stu-id="6a20f-125">PARAMETERS</span></span>

### <span data-ttu-id="6a20f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a20f-126">-DefaultProfile</span></span>
<span data-ttu-id="6a20f-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a20f-128">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="6a20f-128">-Detailed</span></span>
<span data-ttu-id="6a20f-129">이 작업이 태그 값에 대 한 정보를 출력에 추가 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-129">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a20f-130">-이름</span><span class="sxs-lookup"><span data-stu-id="6a20f-130">-Name</span></span>
<span data-ttu-id="6a20f-131">가져올 태그의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="6a20f-132">기본적으로 **AzureRmTag** 에서는 구독에 있는 모든 미리 정의 된 태그에 대 한 기본 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-132">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="6a20f-133">*Name* 매개 변수를 지정 하면 *Detailed* 매개 변수는 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a20f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a20f-134">CommonParameters</span></span>
<span data-ttu-id="6a20f-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a20f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a20f-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a20f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a20f-137">입력</span><span class="sxs-lookup"><span data-stu-id="6a20f-137">INPUTS</span></span>

### <span data-ttu-id="6a20f-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6a20f-138">System.String</span></span>

### <span data-ttu-id="6a20f-139">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6a20f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6a20f-140">출력</span><span class="sxs-lookup"><span data-stu-id="6a20f-140">OUTPUTS</span></span>

### <span data-ttu-id="6a20f-141">PSTag를 통해 서의 일반.</span><span class="sxs-lookup"><span data-stu-id="6a20f-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="6a20f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="6a20f-142">NOTES</span></span>

## <span data-ttu-id="6a20f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a20f-143">RELATED LINKS</span></span>

[<span data-ttu-id="6a20f-144">새로운 AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="6a20f-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="6a20f-145">제거-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="6a20f-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


