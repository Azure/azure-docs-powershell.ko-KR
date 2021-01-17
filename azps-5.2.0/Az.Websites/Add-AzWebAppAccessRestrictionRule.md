---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354722"
---
# <span data-ttu-id="ce319-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="ce319-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="ce319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce319-102">SYNOPSIS</span></span>
<span data-ttu-id="ce319-103">Azure Web App에 Access Restiction 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="ce319-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce319-104">SYNTAX</span></span>

### <span data-ttu-id="ce319-105">IpAddressParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ce319-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce319-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce319-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce319-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce319-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce319-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce319-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce319-109">설명</span><span class="sxs-lookup"><span data-stu-id="ce319-109">DESCRIPTION</span></span>
<span data-ttu-id="ce319-110">**Add-AzWebAppAccessRestrictionRule** cmdlet은 Azure Web App에 액세스 제한 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="ce319-111">예제</span><span class="sxs-lookup"><span data-stu-id="ce319-111">EXAMPLES</span></span>

### <span data-ttu-id="ce319-112">예제 1: 웹앱에 IpAddress 액세스 제한 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="ce319-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="ce319-113">이 명령은 우선 순위 200 및 ip 범위가 있는 액세스 제한 규칙을 리소스 그룹 Default-Web-WestUS에 속하는 ContosoSite라는 웹앱에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="ce319-114">예제 2: 웹앱에 서브넷 서비스 엔드포인트 액세스 제한 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="ce319-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="ce319-115">이 명령은 우선 순위가 300인 액세스 제한 규칙을 corp-vnet의 서브넷 appgw-subnet을 사용하여 리소스 그룹 Default-Web-WestUS에 속하는 ContosoSite라는 웹앱에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="ce319-116">예제 3: 웹앱에 ServiceTag 액세스 제한 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="ce319-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="ce319-117">이 명령은 우선 순위가 200인 액세스 제한 규칙과 Azure Front Door의 IP 범위를 나타내는 서비스 태그를 리소스 그룹 Default-Web-WestUS에 속하는 ContosoSite라는 웹앱에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="ce319-118">예제 4: 웹앱에 다중 주소 액세스 제한 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="ce319-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="ce319-119">이 명령은 리소스 그룹 Default-Web-WestUS에 속하는 ContosoSite라는 웹앱에 우선 순위 200 및 두 개의 IP 범위가 있는 액세스 제한 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="ce319-120">예제 5: 웹앱에 http 헤더를 사용하는 액세스 제한 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="ce319-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="ce319-121">이 명령은 서비스 태그 AzureFrontDoor.Backend에 대해 우선 순위가 400인 액세스 제한 규칙을 추가하고, 특정 값의 http 헤더에 대한 액세스를 리소스 그룹 Default-Web-WestUS에 속하는 ContosoSite라는 웹앱으로만 추가로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ce319-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce319-122">PARAMETERS</span></span>

### <span data-ttu-id="ce319-123">-Action</span><span class="sxs-lookup"><span data-stu-id="ce319-123">-Action</span></span>
<span data-ttu-id="ce319-124">허용 또는 거부 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-124">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce319-125">-DefaultProfile</span></span>
<span data-ttu-id="ce319-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce319-127">-Description</span><span class="sxs-lookup"><span data-stu-id="ce319-127">-Description</span></span>
<span data-ttu-id="ce319-128">액세스 제한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="ce319-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="ce319-129">-HttpHeader</span></span>
<span data-ttu-id="ce319-130">Http 헤더 제한.</span><span class="sxs-lookup"><span data-stu-id="ce319-130">Http header restrictions.</span></span> <span data-ttu-id="ce319-131">예: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span><span class="sxs-lookup"><span data-stu-id="ce319-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce319-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="ce319-133">서브넷에서 서비스 엔드포인트 등록의 유효성을 검사해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="ce319-134">-IpAddress</span></span>
<span data-ttu-id="ce319-135">Ip 주소 v4 또는 v6 CIDR 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="ce319-136">예: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="ce319-136">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-137">-Name</span><span class="sxs-lookup"><span data-stu-id="ce319-137">-Name</span></span>
<span data-ttu-id="ce319-138">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="ce319-138">Rule Name</span></span>

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

### <span data-ttu-id="ce319-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce319-139">-PassThru</span></span>
<span data-ttu-id="ce319-140">액세스 제한 구성 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="ce319-141">-Priority</span><span class="sxs-lookup"><span data-stu-id="ce319-141">-Priority</span></span>
<span data-ttu-id="ce319-142">액세스 제한 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-142">Access Restriction priority.</span></span> <span data-ttu-id="ce319-143">예: 500</span><span class="sxs-lookup"><span data-stu-id="ce319-143">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce319-144">-ResourceGroupName</span></span>
<span data-ttu-id="ce319-145">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ce319-145">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="ce319-146">-ServiceTag</span></span>
<span data-ttu-id="ce319-147">서비스 태그의 이름</span><span class="sxs-lookup"><span data-stu-id="ce319-147">Name of Service Tag</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="ce319-148">-SlotName</span></span>
<span data-ttu-id="ce319-149">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="ce319-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ce319-150">-SubnetId</span></span>
<span data-ttu-id="ce319-151">서브넷의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-151">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ce319-152">-SubnetName</span></span>
<span data-ttu-id="ce319-153">서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-153">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="ce319-154">-TargetScmSite</span></span>
<span data-ttu-id="ce319-155">규칙은 기본 사이트 또는 Scm 사이트를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="ce319-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ce319-156">-VirtualNetworkName</span></span>
<span data-ttu-id="ce319-157">Virtual Network의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-157">Name of Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="ce319-158">-WebAppName</span></span>
<span data-ttu-id="ce319-159">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-159">The name of the web app.</span></span>

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

### <span data-ttu-id="ce319-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce319-160">-Confirm</span></span>
<span data-ttu-id="ce319-161">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce319-162">-WhatIf</span></span>
<span data-ttu-id="ce319-163">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ce319-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce319-164">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-164">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce319-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce319-165">CommonParameters</span></span>
<span data-ttu-id="ce319-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce319-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce319-167">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ce319-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce319-168">입력</span><span class="sxs-lookup"><span data-stu-id="ce319-168">INPUTS</span></span>

### <span data-ttu-id="ce319-169">System.String</span><span class="sxs-lookup"><span data-stu-id="ce319-169">System.String</span></span>

## <span data-ttu-id="ce319-170">출력</span><span class="sxs-lookup"><span data-stu-id="ce319-170">OUTPUTS</span></span>

### <span data-ttu-id="ce319-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="ce319-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="ce319-172">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce319-172">NOTES</span></span>

## <span data-ttu-id="ce319-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce319-173">RELATED LINKS</span></span>

[<span data-ttu-id="ce319-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="ce319-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="ce319-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="ce319-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="ce319-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="ce319-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
