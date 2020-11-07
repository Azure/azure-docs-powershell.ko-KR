---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 7b18a2f5a030a71de0604604b86ba71d2dbe6e03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702455"
---
# <span data-ttu-id="b2dd7-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b2dd7-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="b2dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2dd7-102">SYNOPSIS</span></span>

<span data-ttu-id="b2dd7-103">리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2dd7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2dd7-104">SYNTAX</span></span>

### <span data-ttu-id="b2dd7-105">ByTagNameValueParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b2dd7-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzureRmResource [[-Name] <String>] [-ResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-TagName <String>] [-TagValue <String>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2dd7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2dd7-106">ByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2dd7-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2dd7-107">ByTagObjectParameterSet</span></span>
```
Get-AzureRmResource [[-Name] <String>] [-ResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2dd7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b2dd7-108">DESCRIPTION</span></span>

<span data-ttu-id="b2dd7-109">**Get-AzureRmResource** Cmdlet은 Azure 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-109">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="b2dd7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b2dd7-110">EXAMPLES</span></span>

### <span data-ttu-id="b2dd7-111">예제 1: 현재 구독의 모든 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b2dd7-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzureRmResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

<span data-ttu-id="b2dd7-112">이 명령은 현재 구독에 있는 모든 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="b2dd7-113">예제 2: 리소스 그룹의 모든 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b2dd7-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzureRmResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="b2dd7-114">이 명령은 리소스 그룹 "testRG"의 모든 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="b2dd7-115">예제 3: 리소스 그룹이 제공 된 와일드 카드와 일치 하는 모든 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b2dd7-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzureRmResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="b2dd7-116">이 명령은 리소스 그룹이 속한 모든 리소스를 일종 "other"를 사용 하 여 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="b2dd7-117">예제 4: 지정 된 이름을 사용 하 여 모든 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b2dd7-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzureRmResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="b2dd7-118">이 명령은 리소스 이름이 "testVM" 인 모든 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="b2dd7-119">예제 5: 이름이 제공 된 와일드 카드와 일치 하는 모든 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b2dd7-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzureRmResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="b2dd7-120">이 명령은 리소스 이름이 "test"로 시작 하는 모든 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="b2dd7-121">예제 6: 지정 된 리소스 형식의 모든 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b2dd7-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="b2dd7-122">이 명령은 현재 구독에서 가상 컴퓨터에 해당 하는 모든 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="b2dd7-123">예제 7: 리소스 id를 기준으로 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b2dd7-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzureRmResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="b2dd7-124">이 명령은 리소스 그룹 "testRG"에 "testVM" 이라는 가상 컴퓨터용 제공 된 리소스 id를 사용 하 여 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="b2dd7-125">변수</span><span class="sxs-lookup"><span data-stu-id="b2dd7-125">PARAMETERS</span></span>

### <span data-ttu-id="b2dd7-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b2dd7-126">-ApiVersion</span></span>

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

### <span data-ttu-id="b2dd7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2dd7-127">-DefaultProfile</span></span>
<span data-ttu-id="b2dd7-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b2dd7-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2dd7-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="b2dd7-129">-ExpandProperties</span></span>
<span data-ttu-id="b2dd7-130">지정 된 경우 리소스의 속성을 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="b2dd7-131">-이름</span><span class="sxs-lookup"><span data-stu-id="b2dd7-131">-Name</span></span>
<span data-ttu-id="b2dd7-132">검색할 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="b2dd7-133">이 매개 변수는 문자열의 시작 및/또는 끝에 와일드 카드를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b2dd7-134">-ODataQuery</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="b2dd7-135">-Pre</span></span>

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

### <span data-ttu-id="b2dd7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2dd7-136">-ResourceGroupName</span></span>
<span data-ttu-id="b2dd7-137">Retireved이 속한 자원 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-137">The resource group the resource(s) that is retireved belongs in.</span></span> <span data-ttu-id="b2dd7-138">이 매개 변수는 문자열의 시작 및/또는 끝에 와일드 카드를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2dd7-139">-ResourceId</span></span>
<span data-ttu-id="b2dd7-140">다음 예제와 같이 정규화 된 리소스 ID를 지정 합니다. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="b2dd7-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b2dd7-141">-ResourceType</span></span>
<span data-ttu-id="b2dd7-142">검색할 리소스의 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="b2dd7-143">예를 들어 Microsoft. Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="b2dd7-143">For example, Microsoft.Compute/virtualMachines</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-144">태그</span><span class="sxs-lookup"><span data-stu-id="b2dd7-144">-Tag</span></span>

<span data-ttu-id="b2dd7-145">지정 된 Azure 태그가 있는 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="b2dd7-146">이름 키 또는 이름 및 값 키를 사용 하 여 해시 테이블을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="b2dd7-147">와일드 카드 문자는 지원 되지 않습니다. "Tag"는 리소스 및 리소스 그룹에 적용할 수 있는 이름-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="b2dd7-148">태그를 사용 하 여 부서나 비용 센터 등의 리소스를 분류 하거나 자원에 대 한 메모 또는 메모를 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="b2dd7-149">리소스에 태그를 추가 하려면 New-AzureRmResource 또는 Set-AzureRmResource cmdlet의 Tag 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-149">To add a tag to a resource, use the Tag parameter of the New-AzureRmResource or Set-AzureRmResource cmdlets.</span></span> <span data-ttu-id="b2dd7-150">미리 정의 된 태그를 만들려면 New-AzureRmTag cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-150">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span> <span data-ttu-id="b2dd7-151">Windows PowerShell의 해시 테이블에 대 한 도움말을 보려면 ' Get-help about_Hashtables '을 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-152">-태그</span><span class="sxs-lookup"><span data-stu-id="b2dd7-152">-TagName</span></span>
<span data-ttu-id="b2dd7-153">검색할 리소스의 태그에 있는 키입니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-153">The key in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="b2dd7-154">-TagValue</span></span>
<span data-ttu-id="b2dd7-155">검색할 리소스의 태그에 있는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-155">The value in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2dd7-156">CommonParameters</span></span>
<span data-ttu-id="b2dd7-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2dd7-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2dd7-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2dd7-159">입력</span><span class="sxs-lookup"><span data-stu-id="b2dd7-159">INPUTS</span></span>

### <span data-ttu-id="b2dd7-160">않아야</span><span class="sxs-lookup"><span data-stu-id="b2dd7-160">None</span></span>

## <span data-ttu-id="b2dd7-161">출력</span><span class="sxs-lookup"><span data-stu-id="b2dd7-161">OUTPUTS</span></span>

### <span data-ttu-id="b2dd7-162">ResourceManagement 리소스에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b2dd7-162">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="b2dd7-163">상속자</span><span class="sxs-lookup"><span data-stu-id="b2dd7-163">NOTES</span></span>

## <span data-ttu-id="b2dd7-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2dd7-164">RELATED LINKS</span></span>

[<span data-ttu-id="b2dd7-165">찾기-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b2dd7-165">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="b2dd7-166">이동-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b2dd7-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="b2dd7-167">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b2dd7-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="b2dd7-168">제거-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b2dd7-168">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="b2dd7-169">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b2dd7-169">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
