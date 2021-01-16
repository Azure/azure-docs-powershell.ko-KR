---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340569"
---
# <span data-ttu-id="e6942-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e6942-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="e6942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6942-102">SYNOPSIS</span></span>
<span data-ttu-id="e6942-103">리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-103">Gets resource groups.</span></span>

## <span data-ttu-id="e6942-104">구문</span><span class="sxs-lookup"><span data-stu-id="e6942-104">SYNTAX</span></span>

### <span data-ttu-id="e6942-105">GetByResourceGroupName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e6942-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6942-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e6942-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6942-107">설명</span><span class="sxs-lookup"><span data-stu-id="e6942-107">DESCRIPTION</span></span>
<span data-ttu-id="e6942-108">**Get-AzResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="e6942-109">모든 리소스 그룹을 얻거나 이름 또는 다른 속성으로 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="e6942-110">기본적으로 이 cmdlet은 현재 구독의 모든 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="e6942-111">Azure 리소스 및 Azure 리소스 그룹에 대한 자세한 내용은 New-AzResourceGroup 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e6942-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="e6942-112">예제</span><span class="sxs-lookup"><span data-stu-id="e6942-112">EXAMPLES</span></span>

### <span data-ttu-id="e6942-113">예제 1: 이름으로 리소스 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="e6942-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="e6942-114">이 명령은 EngineerBlog라는 구독에서 Azure 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="e6942-115">예제 2: 리소스 그룹의 모든 태그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="e6942-116">이 명령은 ContosoRG라는 리소스 그룹을 얻게 하여 해당 그룹과 연결된 태그를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="e6942-117">예제 3: 태그를 기반으로 리소스 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="e6942-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="e6942-118">예제 4: 위치로 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="e6942-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="e6942-119">예제 5: 특정 위치에 있는 모든 리소스 그룹의 이름 표시</span><span class="sxs-lookup"><span data-stu-id="e6942-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="e6942-120">예제 6: 이름이 WebServer로 시작하는 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="e6942-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="e6942-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6942-121">PARAMETERS</span></span>

### <span data-ttu-id="e6942-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e6942-122">-ApiVersion</span></span>
<span data-ttu-id="e6942-123">리소스 공급자가 지원하는 API 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e6942-124">기본 버전과 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e6942-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6942-125">-DefaultProfile</span></span>
<span data-ttu-id="e6942-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e6942-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6942-127">-Id</span><span class="sxs-lookup"><span data-stu-id="e6942-127">-Id</span></span>
<span data-ttu-id="e6942-128">얻을 리소스 그룹의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="e6942-129">와일드카드 문자는 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6942-130">-Location</span><span class="sxs-lookup"><span data-stu-id="e6942-130">-Location</span></span>
<span data-ttu-id="e6942-131">얻을 리소스 그룹의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-131">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6942-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e6942-132">-Name</span></span>
<span data-ttu-id="e6942-133">얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="e6942-134">이 매개 변수는 문자열의 시작 및/또는 끝에 와일드카드를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e6942-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="e6942-135">-Pre</span></span>
<span data-ttu-id="e6942-136">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e6942-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6942-137">-Tag</span></span>
<span data-ttu-id="e6942-138">리소스 그룹을 필터링할 태그 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-138">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6942-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6942-139">CommonParameters</span></span>
<span data-ttu-id="e6942-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6942-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6942-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6942-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6942-142">입력</span><span class="sxs-lookup"><span data-stu-id="e6942-142">INPUTS</span></span>

### <span data-ttu-id="e6942-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e6942-143">System.String</span></span>

### <span data-ttu-id="e6942-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6942-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e6942-145">출력</span><span class="sxs-lookup"><span data-stu-id="e6942-145">OUTPUTS</span></span>

### <span data-ttu-id="e6942-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e6942-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="e6942-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6942-147">NOTES</span></span>

## <span data-ttu-id="e6942-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6942-148">RELATED LINKS</span></span>

[<span data-ttu-id="e6942-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e6942-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="e6942-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e6942-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="e6942-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e6942-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

