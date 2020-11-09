---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308876"
---
# <span data-ttu-id="5dddb-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5dddb-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="5dddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dddb-102">SYNOPSIS</span></span>
<span data-ttu-id="5dddb-103">리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-103">Gets resource groups.</span></span>

## <span data-ttu-id="5dddb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5dddb-104">SYNTAX</span></span>

### <span data-ttu-id="5dddb-105">GetByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="5dddb-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dddb-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="5dddb-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dddb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5dddb-107">DESCRIPTION</span></span>
<span data-ttu-id="5dddb-108">**AzResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="5dddb-109">모든 리소스 그룹을 가져오거나 이름 또는 다른 속성을 기준으로 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="5dddb-110">기본적으로이 cmdlet은 현재 구독의 모든 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="5dddb-111">Azure 리소스 및 Azure 리소스 그룹에 대 한 자세한 내용은 New-AzResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5dddb-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="5dddb-112">예제의</span><span class="sxs-lookup"><span data-stu-id="5dddb-112">EXAMPLES</span></span>

### <span data-ttu-id="5dddb-113">예제 1: 이름별로 리소스 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="5dddb-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="5dddb-114">이 명령은 EngineerBlog 이라는 구독에서 Azure 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="5dddb-115">예제 2: 리소스 그룹의 모든 태그 가져오기</span><span class="sxs-lookup"><span data-stu-id="5dddb-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="5dddb-116">이 명령은 ContosoRG 이라는 리소스 그룹을 가져오고 해당 그룹과 연결 된 태그를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="5dddb-117">예제 3: 태그를 기반으로 리소스 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="5dddb-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="5dddb-118">예제 4: 위치에 따라 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="5dddb-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="5dddb-119">예제 5: 특정 위치에 있는 모든 리소스 그룹의 이름 표시</span><span class="sxs-lookup"><span data-stu-id="5dddb-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="5dddb-120">예제 6: 이름이 WebServer로 시작 하는 리소스 그룹 표시</span><span class="sxs-lookup"><span data-stu-id="5dddb-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="5dddb-121">변수</span><span class="sxs-lookup"><span data-stu-id="5dddb-121">PARAMETERS</span></span>

### <span data-ttu-id="5dddb-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5dddb-122">-ApiVersion</span></span>
<span data-ttu-id="5dddb-123">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5dddb-124">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="5dddb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dddb-125">-DefaultProfile</span></span>
<span data-ttu-id="5dddb-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5dddb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5dddb-127">-Id</span><span class="sxs-lookup"><span data-stu-id="5dddb-127">-Id</span></span>
<span data-ttu-id="5dddb-128">가져올 리소스 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="5dddb-129">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-129">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="5dddb-130">-위치</span><span class="sxs-lookup"><span data-stu-id="5dddb-130">-Location</span></span>
<span data-ttu-id="5dddb-131">가져올 리소스 그룹의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-131">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="5dddb-132">-이름</span><span class="sxs-lookup"><span data-stu-id="5dddb-132">-Name</span></span>
<span data-ttu-id="5dddb-133">가져올 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="5dddb-134">이 매개 변수는 문자열의 시작 및/또는 끝에 있는 와일드 카드를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="5dddb-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="5dddb-135">-Pre</span></span>
<span data-ttu-id="5dddb-136">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5dddb-137">태그</span><span class="sxs-lookup"><span data-stu-id="5dddb-137">-Tag</span></span>
<span data-ttu-id="5dddb-138">리소스 그룹을 필터링 하는 태그 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-138">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="5dddb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dddb-139">CommonParameters</span></span>
<span data-ttu-id="5dddb-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dddb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dddb-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5dddb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dddb-142">입력</span><span class="sxs-lookup"><span data-stu-id="5dddb-142">INPUTS</span></span>

### <span data-ttu-id="5dddb-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5dddb-143">System.String</span></span>

### <span data-ttu-id="5dddb-144">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="5dddb-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5dddb-145">출력</span><span class="sxs-lookup"><span data-stu-id="5dddb-145">OUTPUTS</span></span>

### <span data-ttu-id="5dddb-146">SdkModels PSResourceGroup. m a.</span><span class="sxs-lookup"><span data-stu-id="5dddb-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="5dddb-147">상속자</span><span class="sxs-lookup"><span data-stu-id="5dddb-147">NOTES</span></span>

## <span data-ttu-id="5dddb-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dddb-148">RELATED LINKS</span></span>

[<span data-ttu-id="5dddb-149">새로운 AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5dddb-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="5dddb-150">제거-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5dddb-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="5dddb-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5dddb-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

