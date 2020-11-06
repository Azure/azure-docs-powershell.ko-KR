---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 2161c3c4bc81721c0d99b88ab0adfc43beac8eee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529729"
---
# <span data-ttu-id="b6ebb-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b6ebb-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="b6ebb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ebb-103">리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6ebb-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6ebb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6ebb-104">SYNTAX</span></span>

### <span data-ttu-id="b6ebb-105">GetAllResources (기본값)</span><span class="sxs-lookup"><span data-stu-id="b6ebb-105">GetAllResources (Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6ebb-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6ebb-106">GetByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6ebb-107">GetByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="b6ebb-107">GetByTenantLevel</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6ebb-108">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="b6ebb-108">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6ebb-109">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="b6ebb-109">GetByNameAndGroup</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6ebb-110">GetByResourceNameAndType</span><span class="sxs-lookup"><span data-stu-id="b6ebb-110">GetByResourceNameAndType</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6ebb-111">GetByNameGroupAndType</span><span class="sxs-lookup"><span data-stu-id="b6ebb-111">GetByNameGroupAndType</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6ebb-112">GetResourceCollection</span><span class="sxs-lookup"><span data-stu-id="b6ebb-112">GetResourceCollection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6ebb-113">설명은</span><span class="sxs-lookup"><span data-stu-id="b6ebb-113">DESCRIPTION</span></span>
<span data-ttu-id="b6ebb-114">**Get-AzureRmResource** Cmdlet은 Azure 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6ebb-114">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="b6ebb-115">예제의</span><span class="sxs-lookup"><span data-stu-id="b6ebb-115">EXAMPLES</span></span>

### <span data-ttu-id="b6ebb-116">예제 1: 특정 형식의 모든 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6ebb-116">Example 1: Get all the resources of a particular type</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType microsoft.web/sites
```

<span data-ttu-id="b6ebb-117">이 명령은 ResourceGroup11 아래의 microsoft 웹/사이트 종류에 대 한 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6ebb-117">This command gets a resource of the type microsoft.web/sites under ResourceGroup11.</span></span>

### <span data-ttu-id="b6ebb-118">예제 2: 이름으로 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6ebb-118">Example 2: Get a resource by name</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceName ContosoWebsite
```

<span data-ttu-id="b6ebb-119">이 명령은 ResourceGroup11 아래에 ContosoWebsite 이라는 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6ebb-119">This command gets a resource  named ContosoWebsite under ResourceGroup11.</span></span>

### <span data-ttu-id="b6ebb-120">예제 3: 리소스 그룹에 있는 저장소 계정의 모든 상태 표시</span><span class="sxs-lookup"><span data-stu-id="b6ebb-120">Example 3: Show all the status of storage accounts in a Resource Group</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType Microsoft.ClassicStorage/storageAccounts -ExpandProperties |
   Select * -Expand Properties |
   Sort Name |
   Format-Table Name,Status*
```

## <span data-ttu-id="b6ebb-121">변수</span><span class="sxs-lookup"><span data-stu-id="b6ebb-121">PARAMETERS</span></span>

### <span data-ttu-id="b6ebb-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b6ebb-122">-ApiVersion</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ebb-123">-DefaultProfile</span></span>
<span data-ttu-id="b6ebb-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b6ebb-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-125">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="b6ebb-125">-ExpandProperties</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-126">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="b6ebb-126">-ExtensionResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="b6ebb-127">-ExtensionResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-128">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="b6ebb-128">-IsCollection</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-129">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b6ebb-129">-ODataQuery</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="b6ebb-130">-Pre</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ebb-131">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6ebb-132">-ResourceId</span></span>
<span data-ttu-id="b6ebb-133">다음 예제와 같이 구독을 포함 하 여 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ebb-133">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="b6ebb-134">`/subscriptions/`구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b6ebb-134">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="b6ebb-135">이 cmdlet은이 ID가 있는 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6ebb-135">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-136">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="b6ebb-136">-ResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-137">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b6ebb-137">-ResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByResourceNameAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-138">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b6ebb-138">-TenantLevel</span></span>
<span data-ttu-id="b6ebb-139">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b6ebb-139">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-140">-위쪽</span><span class="sxs-lookup"><span data-stu-id="b6ebb-140">-Top</span></span>
```yaml
Type: Int32
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ebb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ebb-141">CommonParameters</span></span>
<span data-ttu-id="b6ebb-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ebb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ebb-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ebb-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ebb-144">입력</span><span class="sxs-lookup"><span data-stu-id="b6ebb-144">INPUTS</span></span>

### <span data-ttu-id="b6ebb-145">않아야</span><span class="sxs-lookup"><span data-stu-id="b6ebb-145">None</span></span>
<span data-ttu-id="b6ebb-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ebb-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6ebb-147">출력</span><span class="sxs-lookup"><span data-stu-id="b6ebb-147">OUTPUTS</span></span>

### <span data-ttu-id="b6ebb-148">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="b6ebb-148">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b6ebb-149">상속자</span><span class="sxs-lookup"><span data-stu-id="b6ebb-149">NOTES</span></span>

## <span data-ttu-id="b6ebb-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6ebb-150">RELATED LINKS</span></span>

[<span data-ttu-id="b6ebb-151">찾기-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b6ebb-151">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="b6ebb-152">이동-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b6ebb-152">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="b6ebb-153">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b6ebb-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="b6ebb-154">제거-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b6ebb-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="b6ebb-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b6ebb-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


