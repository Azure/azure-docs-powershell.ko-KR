---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 2926aa351e7e9f1f9251c5a6e6a2292b27ef93b0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398192"
---
# <span data-ttu-id="7ef30-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="7ef30-101">Get-AzResource</span></span>

## <span data-ttu-id="7ef30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ef30-102">SYNOPSIS</span></span>

<span data-ttu-id="7ef30-103">리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-103">Gets resources.</span></span>

## <span data-ttu-id="7ef30-104">구문</span><span class="sxs-lookup"><span data-stu-id="7ef30-104">SYNTAX</span></span>

### <span data-ttu-id="7ef30-105">ByTagNameValueParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7ef30-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ef30-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ef30-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ef30-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ef30-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ef30-108">설명</span><span class="sxs-lookup"><span data-stu-id="7ef30-108">DESCRIPTION</span></span>

<span data-ttu-id="7ef30-109">**Get-AzResource** cmdlet은 Azure 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="7ef30-110">예제</span><span class="sxs-lookup"><span data-stu-id="7ef30-110">EXAMPLES</span></span>

### <span data-ttu-id="7ef30-111">예제 1: 현재 구독의 모든 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="7ef30-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzResource | ft

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

<span data-ttu-id="7ef30-112">이 명령은 현재 구독의 모든 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="7ef30-113">예제 2: 리소스 그룹의 모든 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="7ef30-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="7ef30-114">이 명령은 리소스 그룹 "testRG"의 모든 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="7ef30-115">예제 3: 리소스 그룹이 제공된 와일드카드와 일치하는 모든 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="7ef30-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="7ef30-116">이 명령은 리소스 그룹이 "other"를 사용하여 존재에 속한 모든 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="7ef30-117">예제 4: 지정한 이름으로 모든 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="7ef30-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="7ef30-118">이 명령은 리소스 이름이 "testVM"인 모든 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="7ef30-119">예제 5: 이름이 제공된 와일드카드와 일치하는 모든 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="7ef30-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="7ef30-120">이 명령은 리소스 이름이 "test"로 시작하는 모든 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="7ef30-121">예제 6: 주어진 리소스 유형의 모든 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="7ef30-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="7ef30-122">이 명령은 가상 머신인 현재 구독의 모든 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="7ef30-123">예제 7: 리소스 ID로 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="7ef30-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="7ef30-124">이 명령은 리소스 그룹 "testRG"에서 "testVM"이라는 가상 머신인 제공된 리소스 ID를 사용하여 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="7ef30-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ef30-125">PARAMETERS</span></span>

### <span data-ttu-id="7ef30-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7ef30-126">-ApiVersion</span></span>

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

### <span data-ttu-id="7ef30-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef30-127">-DefaultProfile</span></span>
<span data-ttu-id="7ef30-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7ef30-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ef30-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="7ef30-129">-ExpandProperties</span></span>
<span data-ttu-id="7ef30-130">지정하면 리소스의 속성을 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="7ef30-131">-Name</span><span class="sxs-lookup"><span data-stu-id="7ef30-131">-Name</span></span>
<span data-ttu-id="7ef30-132">검색할 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="7ef30-133">이 매개 변수는 문자열의 시작 및/또는 끝에 와일드카드를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7ef30-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="7ef30-134">-ODataQuery</span></span>

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

### <span data-ttu-id="7ef30-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="7ef30-135">-Pre</span></span>

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

### <span data-ttu-id="7ef30-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ef30-136">-ResourceGroupName</span></span>
<span data-ttu-id="7ef30-137">검색된 리소스가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="7ef30-138">이 매개 변수는 문자열의 시작 및/또는 끝에 와일드카드를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7ef30-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ef30-139">-ResourceId</span></span>
<span data-ttu-id="7ef30-140">다음 예제와 같이 정식 리소스 ID를 지정합니다. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="7ef30-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

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

### <span data-ttu-id="7ef30-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7ef30-141">-ResourceType</span></span>
<span data-ttu-id="7ef30-142">검색할 리소스의 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="7ef30-143">예를 들어 Microsoft.Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="7ef30-143">For example, Microsoft.Compute/virtualMachines</span></span>

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

### <span data-ttu-id="7ef30-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="7ef30-144">-Tag</span></span>

<span data-ttu-id="7ef30-145">지정된 Azure 태그가 있는 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="7ef30-146">이름 키 또는 이름 및 값 키가 있는 해시 테이블을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="7ef30-147">와일드카드 문자는 지원되지 않습니다. "tag"는 리소스 및 리소스 그룹에 적용할 수 있는 이름-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="7ef30-148">태그를 사용하여 부서 또는 비용 센터와 같은 리소스를 분류하거나 리소스에 대한 메모 또는 메모를 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="7ef30-149">리소스에 태그를 추가하기 위해 New-AzResource cmdlet의 tag Set-AzResource 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="7ef30-150">미리 정의된 태그를 만들 경우 New-AzTag cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="7ef30-151">다음에서 해시 테이블에 대한 도움말을 Windows PowerShell 'Get-Help about_Hashtables'를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

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

### <span data-ttu-id="7ef30-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="7ef30-152">-TagName</span></span>
<span data-ttu-id="7ef30-153">검색할 리소스의 태그에 있는 키입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-153">The key in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="7ef30-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="7ef30-154">-TagValue</span></span>
<span data-ttu-id="7ef30-155">검색할 리소스의 태그에 있는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-155">The value in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="7ef30-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef30-156">CommonParameters</span></span>
<span data-ttu-id="7ef30-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef30-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef30-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7ef30-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef30-159">입력</span><span class="sxs-lookup"><span data-stu-id="7ef30-159">INPUTS</span></span>

### <span data-ttu-id="7ef30-160">System.String</span><span class="sxs-lookup"><span data-stu-id="7ef30-160">System.String</span></span>

## <span data-ttu-id="7ef30-161">출력</span><span class="sxs-lookup"><span data-stu-id="7ef30-161">OUTPUTS</span></span>

### <span data-ttu-id="7ef30-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="7ef30-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="7ef30-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7ef30-163">NOTES</span></span>

## <span data-ttu-id="7ef30-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ef30-164">RELATED LINKS</span></span>


[<span data-ttu-id="7ef30-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="7ef30-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="7ef30-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="7ef30-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="7ef30-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="7ef30-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="7ef30-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="7ef30-168">Set-AzResource</span></span>](./Set-AzResource.md)
