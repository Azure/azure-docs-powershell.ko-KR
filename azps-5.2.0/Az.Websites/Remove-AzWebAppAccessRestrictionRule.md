---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326087"
---
# <span data-ttu-id="71cad-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="71cad-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="71cad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71cad-102">SYNOPSIS</span></span>
<span data-ttu-id="71cad-103">Azure Web App에서 액세스 제한 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="71cad-104">구문</span><span class="sxs-lookup"><span data-stu-id="71cad-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71cad-105">설명</span><span class="sxs-lookup"><span data-stu-id="71cad-105">DESCRIPTION</span></span>
<span data-ttu-id="71cad-106">**Remove-AzWebAppAccessRestrictionRule** cmdlet은 Azure 웹앱에서 액세스 제한 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="71cad-107">예제</span><span class="sxs-lookup"><span data-stu-id="71cad-107">EXAMPLES</span></span>

### <span data-ttu-id="71cad-108">예제 1: 웹앱 액세스 제한 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="71cad-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="71cad-109">이 명령은 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoSite라는 Azure 웹앱에서 IpRule 액세스 제한 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="71cad-110">예제 2: 서비스 태그 웹앱 액세스 제한 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="71cad-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="71cad-111">이 명령은 ServiceTag가 Default-Web-WestUS라는 리소스 그룹에 속하는 ContosoSite라는 Azure 웹앱에서 AzureFrontDoor.Backend와 동일한 액세스 제한 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="71cad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71cad-112">PARAMETERS</span></span>

### <span data-ttu-id="71cad-113">-Action</span><span class="sxs-lookup"><span data-stu-id="71cad-113">-Action</span></span>
<span data-ttu-id="71cad-114">허용 또는 거부 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-114">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="71cad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cad-115">-DefaultProfile</span></span>
<span data-ttu-id="71cad-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71cad-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="71cad-117">-IpAddress</span></span>
<span data-ttu-id="71cad-118">Ip 주소 v4 또는 v6 CIDR 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="71cad-119">예: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="71cad-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="71cad-120">-Name</span><span class="sxs-lookup"><span data-stu-id="71cad-120">-Name</span></span>
<span data-ttu-id="71cad-121">액세스 제한 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="71cad-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="71cad-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71cad-122">-PassThru</span></span>
<span data-ttu-id="71cad-123">액세스 제한 구성 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="71cad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71cad-124">-ResourceGroupName</span></span>
<span data-ttu-id="71cad-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="71cad-125">Resource Group Name</span></span>

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

### <span data-ttu-id="71cad-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="71cad-126">-ServiceTag</span></span>
<span data-ttu-id="71cad-127">서비스 태그의 이름</span><span class="sxs-lookup"><span data-stu-id="71cad-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="71cad-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="71cad-128">-SlotName</span></span>
<span data-ttu-id="71cad-129">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="71cad-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="71cad-130">-SubnetId</span></span>
<span data-ttu-id="71cad-131">서브넷의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="71cad-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="71cad-132">-SubnetName</span></span>
<span data-ttu-id="71cad-133">서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="71cad-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="71cad-134">-TargetScmSite</span></span>
<span data-ttu-id="71cad-135">규칙은 기본 사이트 또는 Scm 사이트를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="71cad-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="71cad-136">-VirtualNetworkName</span></span>
<span data-ttu-id="71cad-137">Virtual Network의 이름(웹앱과 동일한 리소스 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="71cad-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="71cad-138">-WebAppName</span></span>
<span data-ttu-id="71cad-139">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-139">The name of the web app.</span></span>

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

### <span data-ttu-id="71cad-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71cad-140">-Confirm</span></span>
<span data-ttu-id="71cad-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71cad-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71cad-142">-WhatIf</span></span>
<span data-ttu-id="71cad-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="71cad-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71cad-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71cad-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cad-145">CommonParameters</span></span>
<span data-ttu-id="71cad-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71cad-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cad-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71cad-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cad-148">입력</span><span class="sxs-lookup"><span data-stu-id="71cad-148">INPUTS</span></span>

### <span data-ttu-id="71cad-149">System.String</span><span class="sxs-lookup"><span data-stu-id="71cad-149">System.String</span></span>

## <span data-ttu-id="71cad-150">출력</span><span class="sxs-lookup"><span data-stu-id="71cad-150">OUTPUTS</span></span>

### <span data-ttu-id="71cad-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="71cad-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="71cad-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71cad-152">NOTES</span></span>

## <span data-ttu-id="71cad-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71cad-153">RELATED LINKS</span></span>

[<span data-ttu-id="71cad-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="71cad-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="71cad-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="71cad-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="71cad-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="71cad-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
