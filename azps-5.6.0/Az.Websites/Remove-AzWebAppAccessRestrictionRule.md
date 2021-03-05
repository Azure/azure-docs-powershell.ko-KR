---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995820"
---
# <span data-ttu-id="af5d3-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="af5d3-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="af5d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af5d3-102">SYNOPSIS</span></span>
<span data-ttu-id="af5d3-103">Azure Web App에서 액세스 제한 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="af5d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="af5d3-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af5d3-105">설명</span><span class="sxs-lookup"><span data-stu-id="af5d3-105">DESCRIPTION</span></span>
<span data-ttu-id="af5d3-106">**Remove-AzWebAppAccessRestrictionRule** cmdlet은 Azure Web App에서 액세스 제한 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="af5d3-107">예제</span><span class="sxs-lookup"><span data-stu-id="af5d3-107">EXAMPLES</span></span>

### <span data-ttu-id="af5d3-108">예제 1: 웹앱 액세스 제한 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="af5d3-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="af5d3-109">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoSite라는 Azure Web App에서 IpRule 액세스 제한 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="af5d3-110">예제 2: 서비스 태그 웹앱 액세스 제한 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="af5d3-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="af5d3-111">이 명령은 ServiceTag를 사용하여 액세스 제한 규칙을 제거합니다. Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoSite라는 Azure Web App에서 AzureFrontDoor.Backend와 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="af5d3-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="af5d3-112">PARAMETERS</span></span>

### <span data-ttu-id="af5d3-113">-Action</span><span class="sxs-lookup"><span data-stu-id="af5d3-113">-Action</span></span>
<span data-ttu-id="af5d3-114">규칙을 허용하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-114">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af5d3-115">-DefaultProfile</span></span>
<span data-ttu-id="af5d3-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af5d3-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="af5d3-117">-IpAddress</span></span>
<span data-ttu-id="af5d3-118">IP 주소 v4 또는 v6 CIDR 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="af5d3-119">예: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="af5d3-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="af5d3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="af5d3-120">-Name</span></span>
<span data-ttu-id="af5d3-121">액세스 제한 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="af5d3-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="af5d3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af5d3-122">-PassThru</span></span>
<span data-ttu-id="af5d3-123">액세스 제한 구성 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="af5d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af5d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="af5d3-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="af5d3-125">Resource Group Name</span></span>

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

### <span data-ttu-id="af5d3-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="af5d3-126">-ServiceTag</span></span>
<span data-ttu-id="af5d3-127">서비스 태그의 이름</span><span class="sxs-lookup"><span data-stu-id="af5d3-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="af5d3-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="af5d3-128">-SlotName</span></span>
<span data-ttu-id="af5d3-129">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="af5d3-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="af5d3-130">-SubnetId</span></span>
<span data-ttu-id="af5d3-131">Subnet의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="af5d3-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="af5d3-132">-SubnetName</span></span>
<span data-ttu-id="af5d3-133">서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="af5d3-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="af5d3-134">-TargetScmSite</span></span>
<span data-ttu-id="af5d3-135">규칙은 기본 사이트 또는 Scm 사이트를 목표로 합니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="af5d3-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="af5d3-136">-VirtualNetworkName</span></span>
<span data-ttu-id="af5d3-137">Virtual Network의 이름(웹앱과 동일한 리소스 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="af5d3-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="af5d3-138">-WebAppName</span></span>
<span data-ttu-id="af5d3-139">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-139">The name of the web app.</span></span>

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

### <span data-ttu-id="af5d3-140">-확인</span><span class="sxs-lookup"><span data-stu-id="af5d3-140">-Confirm</span></span>
<span data-ttu-id="af5d3-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af5d3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af5d3-142">-WhatIf</span></span>
<span data-ttu-id="af5d3-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af5d3-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af5d3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af5d3-145">CommonParameters</span></span>
<span data-ttu-id="af5d3-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af5d3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af5d3-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af5d3-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af5d3-148">입력</span><span class="sxs-lookup"><span data-stu-id="af5d3-148">INPUTS</span></span>

### <span data-ttu-id="af5d3-149">System.String</span><span class="sxs-lookup"><span data-stu-id="af5d3-149">System.String</span></span>

## <span data-ttu-id="af5d3-150">출력</span><span class="sxs-lookup"><span data-stu-id="af5d3-150">OUTPUTS</span></span>

### <span data-ttu-id="af5d3-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="af5d3-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="af5d3-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af5d3-152">NOTES</span></span>

## <span data-ttu-id="af5d3-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af5d3-153">RELATED LINKS</span></span>

[<span data-ttu-id="af5d3-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="af5d3-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="af5d3-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="af5d3-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="af5d3-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="af5d3-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
