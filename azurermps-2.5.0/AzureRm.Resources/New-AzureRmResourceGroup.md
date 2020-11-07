---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: dd115a7d0445a7b07557b884dd2c7413f5269d00
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882486"
---
# <span data-ttu-id="f527d-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f527d-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="f527d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f527d-102">SYNOPSIS</span></span>
<span data-ttu-id="f527d-103">Azure 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f527d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f527d-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f527d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f527d-105">DESCRIPTION</span></span>
<span data-ttu-id="f527d-106">**AzureRmResourceGroup** Cmdlet은 Azure 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="f527d-107">이름과 위치만 사용 하 여 리소스 그룹을 만든 다음 New-AzureRmResource cmdlet을 사용 하 여 리소스 그룹에 추가할 리소스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="f527d-108">기존 리소스 그룹에 배포를 추가 하려면 New-AzureRmResourceGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="f527d-109">기존 리소스 그룹에 리소스를 추가 하려면 **새 AzureRmResource** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="f527d-110">Azure 리소스는 사용자가 관리 하는 Azure 엔터티 (예: 데이터베이스 서버, 데이터베이스 또는 웹 사이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="f527d-111">Azure 리소스 그룹은 하나의 단위로 배포 되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="f527d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f527d-112">EXAMPLES</span></span>

### <span data-ttu-id="f527d-113">예제 1: 빈 리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="f527d-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="f527d-114">이 명령은 리소스가 없는 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="f527d-115">**새로운 AzureRmResource** 또는 **AzureRmResourceGroupDeployment** cmdlet을 사용 하 여 리소스 및 배포를이 리소스 그룹에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="f527d-116">예제 2: 위치 매개 변수를 사용 하 여 빈 리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="f527d-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

<span data-ttu-id="f527d-117">이 명령은 리소스가 없는 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="f527d-118">예제 3: 태그를 사용 하 여 리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="f527d-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="f527d-119">이 명령은 빈 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-119">This command creates an empty resource group.</span></span> <span data-ttu-id="f527d-120">이 명령은 예제 1의 명령과 같으며 리소스 그룹에 태그를 할당 한다는 점이 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="f527d-121">비어 있는 첫 번째 태그는 리소스가 없는 리소스 그룹을 식별 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="f527d-122">두 번째 태그는 부서 라는 이름이 며 마케팅 값이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="f527d-123">이 예제와 같은 태그를 사용 하 여 관리 또는 예산 책정에 대 한 리소스 그룹을 분류할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="f527d-124">변수</span><span class="sxs-lookup"><span data-stu-id="f527d-124">PARAMETERS</span></span>

### <span data-ttu-id="f527d-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f527d-125">-ApiVersion</span></span>
<span data-ttu-id="f527d-126">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f527d-127">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f527d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f527d-128">-DefaultProfile</span></span>
<span data-ttu-id="f527d-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f527d-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f527d-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f527d-130">-Force</span></span>
<span data-ttu-id="f527d-131">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f527d-132">-위치</span><span class="sxs-lookup"><span data-stu-id="f527d-132">-Location</span></span>
<span data-ttu-id="f527d-133">리소스 그룹의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="f527d-134">Azure 데이터 센터 위치 (예: 서쪽 미국 또는 동남 아시아)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="f527d-135">임의의 위치에 리소스 그룹을 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-135">You can place a resource group in any location.</span></span> <span data-ttu-id="f527d-136">리소스 그룹은 Azure 구독에 같은 위치에 있거나 리소스와 같은 위치에 있을 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="f527d-137">각 리소스 형식을 지 원하는 위치를 확인 하려면 *Providernamespace* 매개 변수와 함께 Get-AzureRmResourceProvider cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-137">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f527d-138">-이름</span><span class="sxs-lookup"><span data-stu-id="f527d-138">-Name</span></span>
<span data-ttu-id="f527d-139">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="f527d-140">리소스 이름은 구독에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="f527d-141">해당 이름을 가진 리소스 그룹이 이미 있는 경우 기존 리소스 그룹을 바꾸기 전에 명령에서 확인을 요청 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f527d-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="f527d-142">-Pre</span></span>
<span data-ttu-id="f527d-143">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f527d-144">태그</span><span class="sxs-lookup"><span data-stu-id="f527d-144">-Tag</span></span>
<span data-ttu-id="f527d-145">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f527d-146">예: @ {key0 = "value0", key1 = $null, key2 = "value2"} 태그를 추가 하거나 변경 하려면 리소스 그룹에 대 한 태그 컬렉션을 바꿔야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="f527d-147">리소스 및 그룹에 태그를 할당 한 후에 Get-AzureRmResourceGroup Get-AzureRmResource의 *tag* 매개 변수를 사용 하 여 태그 이름 또는 이름 및 값을 기준으로 리소스와 그룹을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="f527d-148">태그를 사용 하 여 부서나 비용 센터 등의 리소스를 분류 하거나 자원에 대 한 메모 또는 설명을 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="f527d-149">미리 정의 된 태그를 가져오려면 Get-AzureRMTag cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-149">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

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

### <span data-ttu-id="f527d-150">-확인</span><span class="sxs-lookup"><span data-stu-id="f527d-150">-Confirm</span></span>
<span data-ttu-id="f527d-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f527d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f527d-152">-WhatIf</span></span>
<span data-ttu-id="f527d-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f527d-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f527d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f527d-155">CommonParameters</span></span>
<span data-ttu-id="f527d-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f527d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f527d-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f527d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f527d-158">입력</span><span class="sxs-lookup"><span data-stu-id="f527d-158">INPUTS</span></span>

### <span data-ttu-id="f527d-159">않아야</span><span class="sxs-lookup"><span data-stu-id="f527d-159">None</span></span>

## <span data-ttu-id="f527d-160">출력</span><span class="sxs-lookup"><span data-stu-id="f527d-160">OUTPUTS</span></span>

### <span data-ttu-id="f527d-161">ResourceManagement. PSResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f527d-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="f527d-162">상속자</span><span class="sxs-lookup"><span data-stu-id="f527d-162">NOTES</span></span>

## <span data-ttu-id="f527d-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f527d-163">RELATED LINKS</span></span>

[<span data-ttu-id="f527d-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f527d-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="f527d-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f527d-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="f527d-166">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f527d-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="f527d-167">새로운 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f527d-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f527d-168">제거-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f527d-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="f527d-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f527d-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
