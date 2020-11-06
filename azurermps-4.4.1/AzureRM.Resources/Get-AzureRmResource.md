---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 01e4e6b990a35b8573a9ea1d2f2803f6d6fabc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533003"
---
# <span data-ttu-id="d3744-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3744-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="d3744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3744-102">SYNOPSIS</span></span>
<span data-ttu-id="d3744-103">리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3744-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3744-104">SYNTAX</span></span>

### <span data-ttu-id="d3744-105">모든 리소스 목록 표시 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="d3744-105">The list all resources parameter set.</span></span> <span data-ttu-id="d3744-106">기본값</span><span class="sxs-lookup"><span data-stu-id="d3744-106">(Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3744-107">Id를 기준으로 단일 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-107">Get a single resource by its Id.</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3744-108">테 넌 트 수준에서 단일 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-108">Get a single resource at the tenant level.</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3744-109">테 넌 트 수준에서 지정 된 범위를 기반으로 리소스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-109">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3744-110">이름 및 그룹별로 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3744-110">Get resource by name and group</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3744-111">이름 및 유형별로 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-111">Get a resource by name and type.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3744-112">이름, 그룹 및 유형별로 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3744-112">Get resource by name, group and type</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3744-113">리소스 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3744-113">Get resource collection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3744-114">설명은</span><span class="sxs-lookup"><span data-stu-id="d3744-114">DESCRIPTION</span></span>
<span data-ttu-id="d3744-115">**Get-AzureRmResource** Cmdlet은 Azure 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-115">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="d3744-116">예제의</span><span class="sxs-lookup"><span data-stu-id="d3744-116">EXAMPLES</span></span>

### <span data-ttu-id="d3744-117">예제 1: 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3744-117">Example 1: Get a resource</span></span>
```
PS C:\>Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoWebsite"
```

<span data-ttu-id="d3744-118">이 명령은 ResourceGroup11 아래에 ContosoWebsite 이라는 유형의 microsoft 웹/사이트의 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-118">This command gets a resource of the type microsoft.web/sites, named ContosoWebsite under ResourceGroup11.</span></span>

## <span data-ttu-id="d3744-119">변수</span><span class="sxs-lookup"><span data-stu-id="d3744-119">PARAMETERS</span></span>

### <span data-ttu-id="d3744-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d3744-120">-ApiVersion</span></span>
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

### <span data-ttu-id="d3744-121">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="d3744-121">-ExpandProperties</span></span>
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

### <span data-ttu-id="d3744-122">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="d3744-122">-ExtensionResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3744-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="d3744-123">-ExtensionResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3744-124">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="d3744-124">-IsCollection</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3744-125">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d3744-125">-ODataQuery</span></span>
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

### <span data-ttu-id="d3744-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="d3744-126">-Pre</span></span>
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

### <span data-ttu-id="d3744-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3744-127">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Get resource by name and group
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3744-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3744-128">-ResourceId</span></span>
<span data-ttu-id="d3744-129">다음 예제와 같이 구독을 포함 하 여 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-129">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="d3744-130">`/subscriptions/`구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="d3744-130">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="d3744-131">이 cmdlet은이 ID가 있는 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-131">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a single resource by its Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3744-132">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="d3744-132">-ResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3744-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d3744-133">-ResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resource by name and type.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3744-134">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d3744-134">-TenantLevel</span></span>
<span data-ttu-id="d3744-135">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-135">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3744-136">-위쪽</span><span class="sxs-lookup"><span data-stu-id="d3744-136">-Top</span></span>
```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3744-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3744-137">-DefaultProfile</span></span>
<span data-ttu-id="d3744-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3744-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3744-139">CommonParameters</span></span>
<span data-ttu-id="d3744-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3744-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3744-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3744-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3744-142">입력</span><span class="sxs-lookup"><span data-stu-id="d3744-142">INPUTS</span></span>

## <span data-ttu-id="d3744-143">출력</span><span class="sxs-lookup"><span data-stu-id="d3744-143">OUTPUTS</span></span>

### <span data-ttu-id="d3744-144">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="d3744-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d3744-145">상속자</span><span class="sxs-lookup"><span data-stu-id="d3744-145">NOTES</span></span>

## <span data-ttu-id="d3744-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3744-146">RELATED LINKS</span></span>

[<span data-ttu-id="d3744-147">찾기-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3744-147">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="d3744-148">이동-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3744-148">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="d3744-149">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3744-149">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="d3744-150">제거-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3744-150">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="d3744-151">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d3744-151">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


