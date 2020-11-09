---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308819"
---
# <span data-ttu-id="68144-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="68144-101">Get-AzTag</span></span>

## <span data-ttu-id="68144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68144-102">SYNOPSIS</span></span>
<span data-ttu-id="68144-103">미리 정의 된 Azure 태그를 가져옵니다. | 리소스나 구독에 대 한 전체 태그 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68144-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="68144-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68144-104">SYNTAX</span></span>

### <span data-ttu-id="68144-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="68144-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68144-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68144-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68144-107">설명은</span><span class="sxs-lookup"><span data-stu-id="68144-107">DESCRIPTION</span></span>

<span data-ttu-id="68144-108">**GetPredefinedTagSet** : **Get-AzTag** cmdlet은 구독에서 미리 정의 된 Azure 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68144-108">**GetPredefinedTagSet** : The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="68144-109">이 cmdlet은 태그에 대 한 기본 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="68144-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="68144-110">모든 출력 개체에는 태그와 값이 적용 된 리소스 및 리소스 그룹 수를 나타내는 Count 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68144-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="68144-111">**AzTag** 의 일부인 azure tags 모듈은 미리 정의 된 Azure 태그를 관리 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68144-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="68144-112">Azure 태그는 사용자가 Azure 리소스 및 리소스 그룹 (예: 부서나 비용 센터)을 분류 하거나 리소스 및 그룹에 대 한 메모 또는 설명을 추적 하는 데 사용할 수 있는 이름-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="68144-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="68144-113">한 단계에서 태그를 정의 하 고 적용할 수 있지만, 미리 정의 된 태그를 사용 하면 구독의 태그에 대 한 표준, 일관성, 예측 가능한 이름 및 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68144-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="68144-114">미리 정의 된 태그를 만들려면 New-AzTag cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="68144-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="68144-115">리소스 그룹에 미리 정의 된 태그를 적용 하려면 New-AzTag cmdlet의 *tag* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="68144-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="68144-116">특정 태그 이름 또는 이름과 값에 대 한 리소스 그룹을 검색 하려면 Get-AzResourceGroup cmdlet의 *tag* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="68144-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="68144-117">**GetByResourceIdParameterSet** : **ResourceId** 가 있는 **Get-AzTag** cmdlet은 리소스 또는 구독에 대 한 전체 태그 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68144-117">**GetByResourceIdParameterSet** : The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="68144-118">예제의</span><span class="sxs-lookup"><span data-stu-id="68144-118">EXAMPLES</span></span>

### <span data-ttu-id="68144-119">예제 1: 미리 정의 된 모든 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="68144-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="68144-120">이 명령은 구독에서 미리 정의 된 모든 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68144-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="68144-121">Count 속성에는 구독의 리소스 및 리소스 그룹에 태그가 적용 된 횟수가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68144-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="68144-122">예제 2: 이름으로 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="68144-122">Example 2: Get a tag by name</span></span>
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="68144-123">이 명령은 부서 태그 및 해당 값에 대 한 자세한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68144-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="68144-124">Count 속성은 태그 및 각 값이 구독의 리소스 및 리소스 그룹에 적용 된 횟수를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68144-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="68144-125">예제 3: 모든 태그 값 가져오기</span><span class="sxs-lookup"><span data-stu-id="68144-125">Example 3: Get values of all tags</span></span>
```powershell
PS C:\>Get-AzTag -Detailed

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

<span data-ttu-id="68144-126">이 명령은 *자세한* 매개 변수를 사용 하 여 구독에 미리 정의 된 모든 태그에 대 한 자세한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68144-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="68144-127">*자세한* 매개 변수를 사용 하는 것은 모든 태그에 *Name* 매개 변수를 사용 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="68144-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="68144-128">예제 4: 구독에 대 한 전체 태그 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="68144-128">Example 4: Get the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="68144-129">이 명령은 {subId}를 사용 하 여 구독에 대 한 전체 태그 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68144-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="68144-130">예제 5: 리소스에 대 한 전체 태그 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="68144-130">Example 5: Get the entire set of tags on a resource</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="68144-131">이 명령은 {resourceId}를 사용 하 여 리소스에 대 한 전체 태그 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68144-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="68144-132">변수</span><span class="sxs-lookup"><span data-stu-id="68144-132">PARAMETERS</span></span>

### <span data-ttu-id="68144-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68144-133">-DefaultProfile</span></span>
<span data-ttu-id="68144-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68144-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68144-135">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="68144-135">-Detailed</span></span>
<span data-ttu-id="68144-136">이 작업이 태그 값에 대 한 정보를 출력에 추가 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="68144-136">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68144-137">-이름</span><span class="sxs-lookup"><span data-stu-id="68144-137">-Name</span></span>
<span data-ttu-id="68144-138">미리 정의 된 태그의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68144-138">Name of the predefined tag.</span></span>
<span data-ttu-id="68144-139">기본적으로 **AzTag** 에서는 구독에 있는 모든 미리 정의 된 태그에 대 한 기본 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68144-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="68144-140">*Name* 매개 변수를 지정 하면 *Detailed* 매개 변수는 아무런 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68144-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68144-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68144-141">-ResourceId</span></span>
<span data-ttu-id="68144-142">태그가 지정 된 엔터티의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="68144-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="68144-143">리소스, 리소스 그룹 또는 구독에 태그가 지정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68144-143">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68144-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68144-144">CommonParameters</span></span>
<span data-ttu-id="68144-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68144-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68144-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68144-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68144-147">입력</span><span class="sxs-lookup"><span data-stu-id="68144-147">INPUTS</span></span>

### <span data-ttu-id="68144-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68144-148">System.String</span></span>

### <span data-ttu-id="68144-149">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="68144-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68144-150">출력</span><span class="sxs-lookup"><span data-stu-id="68144-150">OUTPUTS</span></span>

### <span data-ttu-id="68144-151">PSTag |을 (를) 보세요. PSTagResource에 대 한.</span><span class="sxs-lookup"><span data-stu-id="68144-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="68144-152">상속자</span><span class="sxs-lookup"><span data-stu-id="68144-152">NOTES</span></span>

## <span data-ttu-id="68144-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68144-153">RELATED LINKS</span></span>

[<span data-ttu-id="68144-154">새로운 AzTag</span><span class="sxs-lookup"><span data-stu-id="68144-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="68144-155">제거-AzTag</span><span class="sxs-lookup"><span data-stu-id="68144-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="68144-156">업데이트-AzTag</span><span class="sxs-lookup"><span data-stu-id="68144-156">Update-AzTag</span></span>](./Update-AzTag.md)
