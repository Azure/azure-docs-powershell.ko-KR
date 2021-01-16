---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351705"
---
# <span data-ttu-id="2a66a-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a66a-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="2a66a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a66a-102">SYNOPSIS</span></span>
<span data-ttu-id="2a66a-103">리소스 그룹을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-103">Modifies a resource group.</span></span>

## <span data-ttu-id="2a66a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2a66a-104">SYNTAX</span></span>

### <span data-ttu-id="2a66a-105">SetByResourceGroupName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2a66a-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a66a-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="2a66a-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a66a-107">설명</span><span class="sxs-lookup"><span data-stu-id="2a66a-107">DESCRIPTION</span></span>
<span data-ttu-id="2a66a-108">**Set-AzResourceGroup** cmdlet은 리소스 그룹의 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="2a66a-109">이 cmdlet을 사용하여 리소스 그룹에 적용된 Azure 태그를 추가, 변경 또는 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="2a66a-110">이름 매개 *변수를* 지정하여 리소스 그룹 및 *태그* 매개 변수를 식별하여 태그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="2a66a-111">이 cmdlet을 사용하여 리소스 그룹의 이름을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="2a66a-112">예제</span><span class="sxs-lookup"><span data-stu-id="2a66a-112">EXAMPLES</span></span>

### <span data-ttu-id="2a66a-113">예제 1: 리소스 그룹에 태그 적용</span><span class="sxs-lookup"><span data-stu-id="2a66a-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="2a66a-114">이 명령은 IT 값이 있는 부서 태그를 기존 태그가 없는 리소스 그룹에 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="2a66a-115">예제 2: 리소스 그룹에 태그 추가</span><span class="sxs-lookup"><span data-stu-id="2a66a-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="2a66a-116">이 예제에서는 Approved 값과 FY2016 태그가 있는 상태 태그를 기존 태그가 있는 리소스 그룹에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="2a66a-117">지정한 태그가 기존 태그를 대체하기 때문에 새 태그 컬렉션에 기존 태그를 포함해야 합니다. 또는 태그가 손실됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="2a66a-118">첫 번째 명령은 ContosoRG 리소스 그룹을 얻게 하여 dot 메서드를 사용하여 태그 속성의 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="2a66a-119">이 명령은 태그를 $Tags 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="2a66a-120">두 번째 명령은 $Tags 변수에서 태그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="2a66a-121">세 번째 명령은 += 할당 연산자를 사용하여 상태 및 FY2016 태그를 변수 변수의 태그 배열에 $Tags 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="2a66a-122">네 번째 명령은 **Set-AzResourceGroup의** *Tag* 매개 변수를 사용하여 $Tags 변수의 태그를 ContosoRG 리소스 그룹에 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="2a66a-123">다섯 번째 명령은 ContosoRG 리소스 그룹에 적용된 모든 태그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="2a66a-124">출력은 리소스 그룹에 Department 태그와 두 개의 새 태그인 상태 및 FY2015가 있는 것으로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="2a66a-125">예제 3: 리소스 그룹에 대한 모든 태그 삭제</span><span class="sxs-lookup"><span data-stu-id="2a66a-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="2a66a-126">이 명령은 ContosoRG 리소스 그룹에서 모든 태그를 삭제하는 빈 해시 테이블 값이 있는 Tag 매개 변수를 지정합니다. </span><span class="sxs-lookup"><span data-stu-id="2a66a-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="2a66a-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a66a-127">PARAMETERS</span></span>

### <span data-ttu-id="2a66a-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2a66a-128">-ApiVersion</span></span>
<span data-ttu-id="2a66a-129">리소스 공급자가 지원하는 API 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2a66a-130">기본 버전과 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2a66a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a66a-131">-DefaultProfile</span></span>
<span data-ttu-id="2a66a-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2a66a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a66a-133">-Id</span><span class="sxs-lookup"><span data-stu-id="2a66a-133">-Id</span></span>
<span data-ttu-id="2a66a-134">수정할 리소스 그룹의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a66a-135">-Name</span><span class="sxs-lookup"><span data-stu-id="2a66a-135">-Name</span></span>
<span data-ttu-id="2a66a-136">수정할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a66a-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="2a66a-137">-Pre</span></span>
<span data-ttu-id="2a66a-138">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a66a-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a66a-139">-Tag</span></span>
<span data-ttu-id="2a66a-140">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2a66a-141">예: @{key0="value0";key1=$null;key2="value2"} 태그는 리소스 및 리소스 그룹에 만들고 적용할 수 있는 이름-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="2a66a-142">리소스 및 그룹에 태그를 할당한 후  Get-AzResource 및 Get-AzResourceGroup 태그 이름 및 값으로 리소스 및 그룹을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="2a66a-143">태그를 사용하여 부서 또는 비용 센터와 같은 리소스를 분류하거나 리소스에 대한 메모 또는 메모를 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="2a66a-144">태그를 추가하거나 변경하려면 리소스 그룹에 대한 태그 컬렉션을 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="2a66a-145">태그를 삭제하려면 삭제하려는 태그를 제외하고 **Get-AzResourceGroup에서** 리소스 그룹에 현재 적용된 모든 태그가 있는 해시 테이블을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup**, except for the tag you want to delete.</span></span> <span data-ttu-id="2a66a-146">리소스 그룹에서 모든 태그를 삭제하려면 빈 해시 테이블을 `@{}` 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a66a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a66a-147">CommonParameters</span></span>
<span data-ttu-id="2a66a-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2a66a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a66a-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2a66a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a66a-150">입력</span><span class="sxs-lookup"><span data-stu-id="2a66a-150">INPUTS</span></span>

### <span data-ttu-id="2a66a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="2a66a-151">System.String</span></span>

### <span data-ttu-id="2a66a-152">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2a66a-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2a66a-153">출력</span><span class="sxs-lookup"><span data-stu-id="2a66a-153">OUTPUTS</span></span>

### <span data-ttu-id="2a66a-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a66a-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="2a66a-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2a66a-155">NOTES</span></span>

## <span data-ttu-id="2a66a-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a66a-156">RELATED LINKS</span></span>

[<span data-ttu-id="2a66a-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="2a66a-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="2a66a-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a66a-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="2a66a-159">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a66a-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="2a66a-160">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a66a-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
