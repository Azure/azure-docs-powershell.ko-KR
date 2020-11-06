---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529170"
---
# <span data-ttu-id="daddb-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="daddb-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="daddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daddb-102">SYNOPSIS</span></span>
<span data-ttu-id="daddb-103">지정 된 매개 변수를 기준으로 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daddb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="daddb-104">SYNTAX</span></span>

### <span data-ttu-id="daddb-105">지정 된 범위를 기반으로 리소스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-105">Lists the resources based on the specified scope.</span></span> <span data-ttu-id="daddb-106">기본값</span><span class="sxs-lookup"><span data-stu-id="daddb-106">(Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="daddb-107">테 넌 트 수준에서 지정 된 범위를 기반으로 리소스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-107">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="daddb-108">다중 구독 쿼리를 사용 하 여 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-108">Get a resources using a multi-subscription query.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="daddb-109">Hashset으로 지정 된 tag 개체를 기준으로 리소스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-109">Lists resources by a tag object specified as a hashset.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="daddb-110">개별 이름 및 값 매개 변수로 지정 된 태그를 기준으로 리소스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-110">Lists resources by a tag specified as a individual name and value parameters.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="daddb-111">설명은</span><span class="sxs-lookup"><span data-stu-id="daddb-111">DESCRIPTION</span></span>
<span data-ttu-id="daddb-112">**Find-AzureRmResource** cmdlet은 지정 된 매개 변수를 기반으로 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-112">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="daddb-113">예제의</span><span class="sxs-lookup"><span data-stu-id="daddb-113">EXAMPLES</span></span>

### <span data-ttu-id="daddb-114">예제 1: 유형 및 리소스 그룹 이름으로 리소스 검색</span><span class="sxs-lookup"><span data-stu-id="daddb-114">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="daddb-115">이 명령은 리소스 그룹 아래에서 해당 문자열 ResourceGroup과 일치 하는 이름을 가진 microsoft 웹/사이트 유형의 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-115">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="daddb-116">예제 2: 유형 및 리소스 이름으로 리소스 검색</span><span class="sxs-lookup"><span data-stu-id="daddb-116">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="daddb-117">이 명령은 문자열 테스트와 일치 하는 리소스 이름이 있는 microsoft 웹/사이트 형식의 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-117">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="daddb-118">변수</span><span class="sxs-lookup"><span data-stu-id="daddb-118">PARAMETERS</span></span>

### <span data-ttu-id="daddb-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="daddb-119">-ApiVersion</span></span>
<span data-ttu-id="daddb-120">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="daddb-121">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="daddb-122">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="daddb-122">-ExpandProperties</span></span>
<span data-ttu-id="daddb-123">이 cmdlet이 리소스의 속성을 확장 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-123">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="daddb-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="daddb-124">-ExtensionResourceType</span></span>
<span data-ttu-id="daddb-125">이 cmdlet이 검색 하는 리소스에 대 한 확장 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-125">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="daddb-126">예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-126">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="daddb-127">-InformationAction</span></span>
<span data-ttu-id="daddb-128">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="daddb-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="daddb-130">하기로</span><span class="sxs-lookup"><span data-stu-id="daddb-130">Continue</span></span>
- <span data-ttu-id="daddb-131">숨기기</span><span class="sxs-lookup"><span data-stu-id="daddb-131">Ignore</span></span>
- <span data-ttu-id="daddb-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="daddb-132">Inquire</span></span>
- <span data-ttu-id="daddb-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="daddb-133">SilentlyContinue</span></span>
- <span data-ttu-id="daddb-134">중지가</span><span class="sxs-lookup"><span data-stu-id="daddb-134">Stop</span></span>
- <span data-ttu-id="daddb-135">대기</span><span class="sxs-lookup"><span data-stu-id="daddb-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="daddb-136">-InformationVariable</span></span>
<span data-ttu-id="daddb-137">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="daddb-138">-ODataQuery</span></span>
<span data-ttu-id="daddb-139">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="daddb-140">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="daddb-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="daddb-141">-Pre</span></span>
<span data-ttu-id="daddb-142">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="daddb-143">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="daddb-143">-ResourceGroupNameContains</span></span>
<span data-ttu-id="daddb-144">리소스 그룹의 일부 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-144">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="daddb-145">이 cmdlet은이 값이 하위 문자열 인 리소스 그룹과 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-145">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="daddb-146">Cmdlet은 해당 리소스 그룹의 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-146">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-147">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="daddb-147">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="daddb-148">전체 일치 항목에 대 한 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-148">The resource group name for a full match.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-149">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="daddb-149">-ResourceNameContains</span></span>
<span data-ttu-id="daddb-150">리소스의 일부 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-150">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="daddb-151">Cmdlet은이 값을 하위 문자열로 포함 하는 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-151">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-152">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="daddb-152">-ResourceNameEquals</span></span>
<span data-ttu-id="daddb-153">전체 일치 항목에 대 한 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-153">The resource name for a full match.</span></span> <span data-ttu-id="daddb-154">예를 들어 리소스 이름이 testResource 인 경우 testResource를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-154">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-155">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="daddb-155">-ResourceType</span></span>
<span data-ttu-id="daddb-156">자원의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-156">Specifies the type of a resource.</span></span>
<span data-ttu-id="daddb-157">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-157">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="daddb-158">이 cmdlet은 지정 된 유형의 리소스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-158">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-159">태그</span><span class="sxs-lookup"><span data-stu-id="daddb-159">-Tag</span></span>
<span data-ttu-id="daddb-160">OData 쿼리의 태그 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-160">The tag filter for the OData query.</span></span> <span data-ttu-id="daddb-161">필요한 형식은 @ {tagName = $null} 또는 @ {tagName = ' tagValue '}입니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-161">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-162">-태그</span><span class="sxs-lookup"><span data-stu-id="daddb-162">-TagName</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-163">-TagValue</span><span class="sxs-lookup"><span data-stu-id="daddb-163">-TagValue</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-164">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="daddb-164">-TenantLevel</span></span>
<span data-ttu-id="daddb-165">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-165">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-166">-위쪽</span><span class="sxs-lookup"><span data-stu-id="daddb-166">-Top</span></span>
<span data-ttu-id="daddb-167">검색할 리소스의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-167">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daddb-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daddb-168">-DefaultProfile</span></span>
<span data-ttu-id="daddb-169">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daddb-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daddb-170">CommonParameters</span></span>
<span data-ttu-id="daddb-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="daddb-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daddb-172">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daddb-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daddb-173">입력</span><span class="sxs-lookup"><span data-stu-id="daddb-173">INPUTS</span></span>

## <span data-ttu-id="daddb-174">출력</span><span class="sxs-lookup"><span data-stu-id="daddb-174">OUTPUTS</span></span>

### <span data-ttu-id="daddb-175">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="daddb-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="daddb-176">상속자</span><span class="sxs-lookup"><span data-stu-id="daddb-176">NOTES</span></span>

## <span data-ttu-id="daddb-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="daddb-177">RELATED LINKS</span></span>

[<span data-ttu-id="daddb-178">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="daddb-178">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="daddb-179">이동-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="daddb-179">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="daddb-180">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="daddb-180">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="daddb-181">제거-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="daddb-181">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="daddb-182">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="daddb-182">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
