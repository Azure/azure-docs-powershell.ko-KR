---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490383"
---
# <span data-ttu-id="95688-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95688-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="95688-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95688-102">SYNOPSIS</span></span>
<span data-ttu-id="95688-103">Azure 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95688-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="95688-104">구문</span><span class="sxs-lookup"><span data-stu-id="95688-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95688-105">설명</span><span class="sxs-lookup"><span data-stu-id="95688-105">DESCRIPTION</span></span>
<span data-ttu-id="95688-106">**New-AzResourceGroup** cmdlet은 Azure 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95688-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="95688-107">이름 및 위치만 사용하여 리소스 그룹을 만든 다음 New-AzResource cmdlet을 사용하여 리소스 그룹에 추가할 리소스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="95688-108">기존 리소스 그룹에 배포를 추가하기 위해 New-AzResourceGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="95688-109">기존 리소스 그룹에 리소스를 추가하기 위해 **New-AzResource** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="95688-110">Azure 리소스는 데이터베이스 서버, 데이터베이스 또는 웹 사이트와 같은 사용자 관리 Azure 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="95688-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="95688-111">Azure 리소스 그룹은 단위로 배포되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="95688-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="95688-112">예제</span><span class="sxs-lookup"><span data-stu-id="95688-112">EXAMPLES</span></span>

### <span data-ttu-id="95688-113">예제 1: 빈 리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="95688-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="95688-114">이 명령은 리소스가 없는 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95688-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="95688-115">**New-AzResource** 또는 **New-AzResourceGroupDeployment** cmdlet을 사용하여 리소스 및 배포를 이 리소스 그룹에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="95688-116">예제 2: 위치 매개 변수를 사용하여 빈 리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="95688-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="95688-117">이 명령은 리소스가 없는 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95688-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="95688-118">예제 3: 태그가 있는 리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="95688-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="95688-119">이 명령은 빈 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95688-119">This command creates an empty resource group.</span></span> <span data-ttu-id="95688-120">이 명령은 리소스 그룹에 태그를 할당하는 것을 제외하고 예제 1의 명령과 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="95688-121">빈이라는 이름의 첫 번째 태그를 사용하여 리소스가 없는 리소스 그룹을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="95688-122">두 번째 태그는 Department라는 이름의 마케팅 값을 습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="95688-123">이와 같은 태그를 사용하여 관리 또는 예산을 위한 리소스 그룹을 분류할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="95688-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95688-124">PARAMETERS</span></span>

### <span data-ttu-id="95688-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="95688-125">-ApiVersion</span></span>
<span data-ttu-id="95688-126">리소스 공급자가 지원하는 API 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="95688-127">기본 버전과 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="95688-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95688-128">-DefaultProfile</span></span>
<span data-ttu-id="95688-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="95688-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95688-130">-Force</span><span class="sxs-lookup"><span data-stu-id="95688-130">-Force</span></span>
<span data-ttu-id="95688-131">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95688-132">-Location</span><span class="sxs-lookup"><span data-stu-id="95688-132">-Location</span></span>
<span data-ttu-id="95688-133">리소스 그룹의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="95688-134">미국 서부 또는 동남 아시아와 같은 Azure 데이터 센터 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="95688-135">리소스 그룹을 모든 위치에 위치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-135">You can place a resource group in any location.</span></span> <span data-ttu-id="95688-136">리소스 그룹은 Azure 구독과 동일한 위치 또는 리소스와 동일한 위치에 있을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="95688-137">각 리소스 종류를 지원하는 위치를 결정하기 위해 *ProviderNamespace* 매개 Get-AzResourceProvider cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95688-138">-Name</span><span class="sxs-lookup"><span data-stu-id="95688-138">-Name</span></span>
<span data-ttu-id="95688-139">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="95688-140">리소스 이름은 구독에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="95688-141">해당 이름이 있는 리소스 그룹이 이미 있는 경우 명령은 기존 리소스 그룹을 바꾸기 전에 확인을 요청하는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95688-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="95688-142">-Pre</span></span>
<span data-ttu-id="95688-143">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="95688-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="95688-144">-Tag</span></span>
<span data-ttu-id="95688-145">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="95688-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="95688-146">예: @{key0="value0";key1=$null;key2="value2"} 태그를 추가하거나 변경하려면 리소스 그룹에 대한 태그 컬렉션을 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="95688-147">리소스 및 그룹에 태그를 할당한 후  Get-AzResource 및 Get-AzResourceGroup 태그 이름 또는 이름 및 값으로 리소스 및 그룹을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="95688-148">태그를 사용하여 부서 또는 비용 센터와 같은 리소스를 분류하거나 리소스에 대한 메모 또는 메모를 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="95688-149">미리 정의한 태그를 얻습니다. Get-AzTag cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95688-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95688-150">-Confirm</span></span>
<span data-ttu-id="95688-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95688-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95688-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95688-152">-WhatIf</span></span>
<span data-ttu-id="95688-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="95688-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95688-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95688-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95688-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95688-155">CommonParameters</span></span>
<span data-ttu-id="95688-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95688-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95688-157">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="95688-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95688-158">입력</span><span class="sxs-lookup"><span data-stu-id="95688-158">INPUTS</span></span>

### <span data-ttu-id="95688-159">System.String</span><span class="sxs-lookup"><span data-stu-id="95688-159">System.String</span></span>

### <span data-ttu-id="95688-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="95688-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="95688-161">출력</span><span class="sxs-lookup"><span data-stu-id="95688-161">OUTPUTS</span></span>

### <span data-ttu-id="95688-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95688-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="95688-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95688-163">NOTES</span></span>

## <span data-ttu-id="95688-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95688-164">RELATED LINKS</span></span>

[<span data-ttu-id="95688-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="95688-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="95688-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95688-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="95688-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="95688-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="95688-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="95688-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="95688-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95688-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="95688-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95688-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
