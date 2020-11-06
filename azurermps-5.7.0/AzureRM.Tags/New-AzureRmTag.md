---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: 77bf93905b0cba4e8f8a23cb9f3cb8945fff74f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533543"
---
# <span data-ttu-id="b38ad-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="b38ad-101">New-AzureRmTag</span></span>

## <span data-ttu-id="b38ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b38ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b38ad-103">미리 정의 된 Azure 태그를 만들거나 기존 태그에 값을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b38ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b38ad-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b38ad-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b38ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b38ad-106">**AzureRmTag** cmdlet은 미리 정의 된 선택적 값을 사용 하 여 미리 정의 되어 있는 Azure 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="b38ad-107">또한 기존에 미리 정의 된 태그에 다른 값을 추가 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="b38ad-108">미리 정의 된 태그를 만들려면 고유한 태그 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="b38ad-109">미리 정의 된 기존 태그에 값을 추가 하려면 기존 태그의 이름과 새 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>

<span data-ttu-id="b38ad-110">이 cmdlet은 새 태그 또는 수정 된 태그가 해당 값과 적용 된 리소스 수를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>

<span data-ttu-id="b38ad-111">**새로운 AzureRmTag** 의 일부인 azure tags 모듈은 미리 정의 된 Azure 태그를 관리 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="b38ad-112">Azure 태그는 사용자가 Azure 리소스 및 리소스 그룹 (예: 부서나 비용 센터)을 분류 하거나 리소스 및 그룹에 대 한 메모 또는 설명을 추적 하는 데 사용할 수 있는 이름-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="b38ad-113">한 단계에서 태그를 정의 하 고 적용할 수 있지만, 미리 정의 된 태그를 사용 하면 구독의 태그에 대 한 표준, 일관성, 예측 가능한 이름 및 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="b38ad-114">구독에 미리 정의 된 태그가 포함 되어 있는 경우에는 구독에 있는 리소스나 리소스 그룹에 정의 되지 않은 태그나 값을 적용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-114">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="b38ad-115">리소스 또는 리소스 그룹에 미리 정의 된 태그를 적용 하려면 New-AzureRmTag cmdlet의 *tag* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-115">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="b38ad-116">지정 된 태그 이름이 나 이름 및 값을 사용 하 여 리소스 그룹을 검색 하려면 Get-AzureRMResourceGroup cmdlet의 *tag* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-116">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

<span data-ttu-id="b38ad-117">모든 태그에는 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-117">Every tag has a name.</span></span>
<span data-ttu-id="b38ad-118">값은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-118">The values are optional.</span></span>
<span data-ttu-id="b38ad-119">미리 정의 된 Azure 태그에는 여러 값이 포함 될 수 있지만 리소스 또는 리소스 그룹에 태그를 적용 하는 경우 태그 이름과 해당 값 중 하나만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-119">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="b38ad-120">예를 들어 재무, 인적 자원 등의 각 부서에 대 한 값을 사용 하 여 미리 정의 된 부서 태그를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-120">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="b38ad-121">자원에 부서 태그를 적용 하는 경우 재무와 같은 미리 정의 된 값을 하나만 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-121">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="b38ad-122">예제의</span><span class="sxs-lookup"><span data-stu-id="b38ad-122">EXAMPLES</span></span>

### <span data-ttu-id="b38ad-123">예제 1: 미리 정의 된 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="b38ad-123">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="b38ad-124">이 명령은 FY2015 이라는 미리 정의 된 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-124">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="b38ad-125">이 태그에는 값이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-125">This tag has no values.</span></span>
<span data-ttu-id="b38ad-126">값이 없는 태그를 리소스나 리소스 그룹에 적용 하거나, **New-AzureRmTag** 를 사용 하 여 태그에 값을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-126">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="b38ad-127">리소스 또는 리소스 그룹에 태그를 적용 하는 경우 값을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-127">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="b38ad-128">예제 2: 값을 사용 하 여 미리 정의 된 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="b38ad-128">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="b38ad-129">이 명령은 재무 값이 포함 된 부서별 이라는 미리 정의 된 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-129">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="b38ad-130">예제 3: 미리 정의 된 태그에 값 추가</span><span class="sxs-lookup"><span data-stu-id="b38ad-130">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="b38ad-131">이러한 명령을 사용 하면 두 값이 있는 부서별 이라는 미리 정의 된 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-131">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="b38ad-132">태그 이름이 있으면 새 항목을 만드는 대신 **AzureRmTag** 에서 기존 태그에 값을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-132">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="b38ad-133">예제 4: 미리 정의 된 태그 사용</span><span class="sxs-lookup"><span data-stu-id="b38ad-133">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="b38ad-134">이 예제의 명령은 미리 정의 된 태그를 만들고 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-134">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="b38ad-135">변수</span><span class="sxs-lookup"><span data-stu-id="b38ad-135">PARAMETERS</span></span>

### <span data-ttu-id="b38ad-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38ad-136">-DefaultProfile</span></span>
<span data-ttu-id="b38ad-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b38ad-138">-이름</span><span class="sxs-lookup"><span data-stu-id="b38ad-138">-Name</span></span>
<span data-ttu-id="b38ad-139">태그 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-139">Specifies the tag name.</span></span>
<span data-ttu-id="b38ad-140">미리 정의 된 새 태그를 만들려면 고유한 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-140">To create a new predefined tag, enter a unique name.</span></span>

<span data-ttu-id="b38ad-141">기존 태그에 값을 추가 하려면 기존 태그의 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-141">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="b38ad-142">미리 정의 된 기존 태그에 지정 된 이름이 있는 경우 새 태그를 만드는 대신 해당 이름의 태그에 지정 된 값이 있는 경우 **AzureRmTag** 를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-142">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b38ad-143">-값</span><span class="sxs-lookup"><span data-stu-id="b38ad-143">-Value</span></span>
<span data-ttu-id="b38ad-144">태그 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-144">Specifies a tag value.</span></span>
<span data-ttu-id="b38ad-145">미리 정의 된 태그에 여러 값이 있을 수 있지만 각 명령에 하나의 값만 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-145">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="b38ad-146">태그에 값이 없는 이름이 있을 수 있으므로이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-146">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b38ad-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38ad-147">CommonParameters</span></span>
<span data-ttu-id="b38ad-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b38ad-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38ad-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b38ad-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38ad-150">입력</span><span class="sxs-lookup"><span data-stu-id="b38ad-150">INPUTS</span></span>

### <span data-ttu-id="b38ad-151">않아야</span><span class="sxs-lookup"><span data-stu-id="b38ad-151">None</span></span>

## <span data-ttu-id="b38ad-152">출력</span><span class="sxs-lookup"><span data-stu-id="b38ad-152">OUTPUTS</span></span>

### <span data-ttu-id="b38ad-153">PSTag에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b38ad-153">Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="b38ad-154">상속자</span><span class="sxs-lookup"><span data-stu-id="b38ad-154">NOTES</span></span>

## <span data-ttu-id="b38ad-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b38ad-155">RELATED LINKS</span></span>

[<span data-ttu-id="b38ad-156">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="b38ad-156">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="b38ad-157">제거-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="b38ad-157">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


