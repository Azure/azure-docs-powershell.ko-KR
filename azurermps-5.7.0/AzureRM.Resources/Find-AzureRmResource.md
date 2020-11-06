---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531676"
---
# <span data-ttu-id="ab3fb-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ab3fb-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="ab3fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3fb-103">지정 된 매개 변수를 기준으로 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab3fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab3fb-104">SYNTAX</span></span>

### <span data-ttu-id="ab3fb-105">GetBySpecifiedScope (기본값)</span><span class="sxs-lookup"><span data-stu-id="ab3fb-105">GetBySpecifiedScope (Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab3fb-106">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ab3fb-106">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab3fb-107">GetByMultiSubscriptionQuery</span><span class="sxs-lookup"><span data-stu-id="ab3fb-107">GetByMultiSubscriptionQuery</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab3fb-108">GetByTagObject</span><span class="sxs-lookup"><span data-stu-id="ab3fb-108">GetByTagObject</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab3fb-109">GetByTagNameValue</span><span class="sxs-lookup"><span data-stu-id="ab3fb-109">GetByTagNameValue</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ab3fb-110">설명은</span><span class="sxs-lookup"><span data-stu-id="ab3fb-110">DESCRIPTION</span></span>
<span data-ttu-id="ab3fb-111">**Find-AzureRmResource** cmdlet은 지정 된 매개 변수를 기반으로 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-111">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="ab3fb-112">예제의</span><span class="sxs-lookup"><span data-stu-id="ab3fb-112">EXAMPLES</span></span>

### <span data-ttu-id="ab3fb-113">예제 1: 유형 및 리소스 그룹 이름으로 리소스 검색</span><span class="sxs-lookup"><span data-stu-id="ab3fb-113">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="ab3fb-114">이 명령은 리소스 그룹 아래에서 해당 문자열 ResourceGroup과 일치 하는 이름을 가진 microsoft 웹/사이트 유형의 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-114">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="ab3fb-115">예제 2: 유형 및 리소스 이름으로 리소스 검색</span><span class="sxs-lookup"><span data-stu-id="ab3fb-115">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="ab3fb-116">이 명령은 문자열 테스트와 일치 하는 리소스 이름이 있는 microsoft 웹/사이트 형식의 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-116">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="ab3fb-117">변수</span><span class="sxs-lookup"><span data-stu-id="ab3fb-117">PARAMETERS</span></span>

### <span data-ttu-id="ab3fb-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ab3fb-118">-ApiVersion</span></span>
<span data-ttu-id="ab3fb-119">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ab3fb-120">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ab3fb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab3fb-121">-DefaultProfile</span></span>
<span data-ttu-id="ab3fb-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ab3fb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab3fb-123">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="ab3fb-123">-ExpandProperties</span></span>
<span data-ttu-id="ab3fb-124">이 cmdlet이 리소스의 속성을 확장 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-124">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="ab3fb-125">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="ab3fb-125">-ExtensionResourceType</span></span>
<span data-ttu-id="ab3fb-126">이 cmdlet이 검색 하는 리소스에 대 한 확장 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-126">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="ab3fb-127">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-127">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ab3fb-128">-InformationAction</span></span>
<span data-ttu-id="ab3fb-129">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ab3fb-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ab3fb-131">하기로</span><span class="sxs-lookup"><span data-stu-id="ab3fb-131">Continue</span></span>
- <span data-ttu-id="ab3fb-132">숨기기</span><span class="sxs-lookup"><span data-stu-id="ab3fb-132">Ignore</span></span>
- <span data-ttu-id="ab3fb-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="ab3fb-133">Inquire</span></span>
- <span data-ttu-id="ab3fb-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ab3fb-134">SilentlyContinue</span></span>
- <span data-ttu-id="ab3fb-135">중지가</span><span class="sxs-lookup"><span data-stu-id="ab3fb-135">Stop</span></span>
- <span data-ttu-id="ab3fb-136">대기</span><span class="sxs-lookup"><span data-stu-id="ab3fb-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ab3fb-137">-InformationVariable</span></span>
<span data-ttu-id="ab3fb-138">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ab3fb-139">-ODataQuery</span></span>
<span data-ttu-id="ab3fb-140">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="ab3fb-141">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="ab3fb-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="ab3fb-142">-Pre</span></span>
<span data-ttu-id="ab3fb-143">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ab3fb-144">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="ab3fb-144">-ResourceGroupNameContains</span></span>
<span data-ttu-id="ab3fb-145">리소스 그룹의 일부 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-145">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="ab3fb-146">이 cmdlet은이 값이 하위 문자열 인 리소스 그룹과 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-146">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="ab3fb-147">Cmdlet은 해당 리소스 그룹의 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-147">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-148">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="ab3fb-148">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="ab3fb-149">전체 일치 항목에 대 한 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-149">The resource group name for a full match.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-150">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="ab3fb-150">-ResourceNameContains</span></span>
<span data-ttu-id="ab3fb-151">리소스의 일부 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-151">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="ab3fb-152">Cmdlet은이 값을 하위 문자열로 포함 하는 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-152">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-153">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="ab3fb-153">-ResourceNameEquals</span></span>
<span data-ttu-id="ab3fb-154">전체 일치 항목에 대 한 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-154">The resource name for a full match.</span></span> <span data-ttu-id="ab3fb-155">예를 들어 리소스 이름이 testResource 인 경우 testResource를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-155">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ab3fb-156">-ResourceType</span></span>
<span data-ttu-id="ab3fb-157">자원의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-157">Specifies the type of a resource.</span></span>
<span data-ttu-id="ab3fb-158">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-158">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="ab3fb-159">이 cmdlet은 지정 된 유형의 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-159">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-160">태그</span><span class="sxs-lookup"><span data-stu-id="ab3fb-160">-Tag</span></span>
<span data-ttu-id="ab3fb-161">OData 쿼리의 태그 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-161">The tag filter for the OData query.</span></span> <span data-ttu-id="ab3fb-162">필요한 형식은 @ {tagName = $null} 또는 @ {tagName = ' tagValue '}입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-162">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-163">-태그</span><span class="sxs-lookup"><span data-stu-id="ab3fb-163">-TagName</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-164">-TagValue</span><span class="sxs-lookup"><span data-stu-id="ab3fb-164">-TagValue</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ab3fb-165">-TenantLevel</span></span>
<span data-ttu-id="ab3fb-166">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-167">-위쪽</span><span class="sxs-lookup"><span data-stu-id="ab3fb-167">-Top</span></span>
<span data-ttu-id="ab3fb-168">검색할 리소스의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-168">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3fb-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3fb-169">CommonParameters</span></span>
<span data-ttu-id="ab3fb-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3fb-171">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab3fb-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3fb-172">입력</span><span class="sxs-lookup"><span data-stu-id="ab3fb-172">INPUTS</span></span>

### <span data-ttu-id="ab3fb-173">않아야</span><span class="sxs-lookup"><span data-stu-id="ab3fb-173">None</span></span>
<span data-ttu-id="ab3fb-174">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab3fb-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab3fb-175">출력</span><span class="sxs-lookup"><span data-stu-id="ab3fb-175">OUTPUTS</span></span>

### <span data-ttu-id="ab3fb-176">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="ab3fb-176">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ab3fb-177">상속자</span><span class="sxs-lookup"><span data-stu-id="ab3fb-177">NOTES</span></span>

## <span data-ttu-id="ab3fb-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab3fb-178">RELATED LINKS</span></span>

[<span data-ttu-id="ab3fb-179">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ab3fb-179">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="ab3fb-180">이동-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ab3fb-180">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="ab3fb-181">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ab3fb-181">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ab3fb-182">제거-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ab3fb-182">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="ab3fb-183">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ab3fb-183">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
