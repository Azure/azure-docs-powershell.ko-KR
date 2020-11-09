---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308708"
---
# <span data-ttu-id="1f3e6-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f3e6-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="1f3e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3e6-103">리소스 그룹을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-103">Modifies a resource group.</span></span>

## <span data-ttu-id="1f3e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f3e6-104">SYNTAX</span></span>

### <span data-ttu-id="1f3e6-105">SetByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f3e6-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f3e6-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="1f3e6-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f3e6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1f3e6-107">DESCRIPTION</span></span>
<span data-ttu-id="1f3e6-108">**Set-AzResourceGroup** cmdlet은 리소스 그룹의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="1f3e6-109">이 cmdlet을 사용 하 여 리소스 그룹에 적용 된 Azure 태그를 추가, 변경 또는 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="1f3e6-110">*Name* 매개 변수를 지정 하 여 리소스 그룹을 식별 하 고 *Tag* 매개 변수를 지정 하 여 태그를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="1f3e6-111">이 cmdlet을 사용 하 여 리소스 그룹의 이름을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="1f3e6-112">예제의</span><span class="sxs-lookup"><span data-stu-id="1f3e6-112">EXAMPLES</span></span>

### <span data-ttu-id="1f3e6-113">예제 1: 리소스 그룹에 태그 적용</span><span class="sxs-lookup"><span data-stu-id="1f3e6-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="1f3e6-114">이 명령은 해당 값이 포함 된 부서 태그를 기존 태그가 없는 리소스 그룹에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="1f3e6-115">예제 2: 리소스 그룹에 태그 추가</span><span class="sxs-lookup"><span data-stu-id="1f3e6-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="1f3e6-116">이 예제에서는 승인 값이 있는 상태 태그와 기존 태그가 있는 리소스 그룹에 FY2016 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="1f3e6-117">지정 하는 태그가 기존 태그를 대체 하기 때문에 새 태그 컬렉션에 기존 태그를 포함 해야 하며, 그렇지 않은 경우에는 없어집니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="1f3e6-118">첫 번째 명령은 ContosoRG 리소스 그룹을 가져온 다음 도트 메서드를 사용 하 여 해당 태그 속성의 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="1f3e6-119">명령이 $Tags 변수에 태그를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="1f3e6-120">두 번째 명령은 $Tags 변수의 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="1f3e6-121">세 번째 명령은 + = 대입 연산자를 사용 하 여 $Tags 변수의 태그 배열에 Status 및 FY2016 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="1f3e6-122">네 번째 명령은 **Set-AzResourceGroup** 의 *Tag* 매개 변수를 사용 하 여 $Tags 변수의 태그를 ContosoRG 리소스 그룹에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="1f3e6-123">다섯 번째 명령은 ContosoRG 리소스 그룹에 적용 된 모든 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="1f3e6-124">출력에는 리소스 그룹에 부서 태그와 두 개의 새 태그, 상태 및 FY2015이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="1f3e6-125">예제 3: 리소스 그룹에 대 한 모든 태그 삭제</span><span class="sxs-lookup"><span data-stu-id="1f3e6-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="1f3e6-126">이 명령은 ContosoRG 리소스 그룹에서 모든 태그를 삭제 하는 빈 해시 테이블 값을 사용 하 여 *Tag* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="1f3e6-127">변수</span><span class="sxs-lookup"><span data-stu-id="1f3e6-127">PARAMETERS</span></span>

### <span data-ttu-id="1f3e6-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1f3e6-128">-ApiVersion</span></span>
<span data-ttu-id="1f3e6-129">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1f3e6-130">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="1f3e6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3e6-131">-DefaultProfile</span></span>
<span data-ttu-id="1f3e6-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1f3e6-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f3e6-133">-Id</span><span class="sxs-lookup"><span data-stu-id="1f3e6-133">-Id</span></span>
<span data-ttu-id="1f3e6-134">수정할 리소스 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-134">Specifies the ID of the resource group to modify.</span></span>

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

### <span data-ttu-id="1f3e6-135">-이름</span><span class="sxs-lookup"><span data-stu-id="1f3e6-135">-Name</span></span>
<span data-ttu-id="1f3e6-136">수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-136">Specifies the name of the resource group to modify.</span></span>

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

### <span data-ttu-id="1f3e6-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="1f3e6-137">-Pre</span></span>
<span data-ttu-id="1f3e6-138">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1f3e6-139">태그</span><span class="sxs-lookup"><span data-stu-id="1f3e6-139">-Tag</span></span>
<span data-ttu-id="1f3e6-140">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1f3e6-141">예를 들어 @ {key0 = "value0", key1 = $null, key2 = "value2"} 태그는 리소스 및 리소스 그룹을 만들고 적용할 수 있는 이름-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="1f3e6-142">리소스 및 그룹에 태그를 할당 한 후에 Get-AzResourceGroup Get-AzResource의 *tag* 매개 변수를 사용 하 여 태그 이름 또는 이름 및 값을 기준으로 리소스와 그룹을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="1f3e6-143">태그를 사용 하 여 부서나 비용 센터 등의 리소스를 분류 하거나 자원에 대 한 메모 또는 설명을 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="1f3e6-144">태그를 추가 하거나 변경 하려면 리소스 그룹에 대 한 태그 컬렉션을 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="1f3e6-145">태그를 삭제 하려면 삭제 하려는 태그를 제외 하 고 **AzResourceGroup** 에서 리소스 그룹에 현재 적용 된 모든 태그가 있는 해시 테이블을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="1f3e6-146">리소스 그룹에서 모든 태그를 삭제 하려면 빈 해시 테이블 ()을 지정 `@{}` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="1f3e6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3e6-147">CommonParameters</span></span>
<span data-ttu-id="1f3e6-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3e6-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3e6-150">입력</span><span class="sxs-lookup"><span data-stu-id="1f3e6-150">INPUTS</span></span>

### <span data-ttu-id="1f3e6-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f3e6-151">System.String</span></span>

### <span data-ttu-id="1f3e6-152">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="1f3e6-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1f3e6-153">출력</span><span class="sxs-lookup"><span data-stu-id="1f3e6-153">OUTPUTS</span></span>

### <span data-ttu-id="1f3e6-154">SdkModels PSResourceGroup. m a.</span><span class="sxs-lookup"><span data-stu-id="1f3e6-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="1f3e6-155">상속자</span><span class="sxs-lookup"><span data-stu-id="1f3e6-155">NOTES</span></span>

## <span data-ttu-id="1f3e6-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f3e6-156">RELATED LINKS</span></span>

[<span data-ttu-id="1f3e6-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="1f3e6-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="1f3e6-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f3e6-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="1f3e6-159">새로운 AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f3e6-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="1f3e6-160">제거-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f3e6-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
