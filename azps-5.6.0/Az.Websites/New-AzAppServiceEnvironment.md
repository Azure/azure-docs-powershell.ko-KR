---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
ms.openlocfilehash: a922958ec2e15ea9cb4a3b0189f74dda6d71eab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011136"
---
# <span data-ttu-id="c3d71-101">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3d71-101">New-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="c3d71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3d71-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d71-103">권장되는 경로 테이블 및 네트워크 보안 그룹을 포함하여 App Service Environment를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-103">Creates an App Service Environment including the recommended Route Table and Network Security Group</span></span>

## <span data-ttu-id="c3d71-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3d71-104">SYNTAX</span></span>

### <span data-ttu-id="c3d71-105">ASEv2SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d71-105">ASEv2SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> -LoadBalancerMode <String>
 [-SkipRouteTable] [-SkipNetworkSecurityGroup] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d71-106">ASEv3SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d71-106">ASEv3SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d71-107">ASEv2SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d71-107">ASEv2SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> -LoadBalancerMode <String> [-SkipRouteTable] [-SkipNetworkSecurityGroup]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3d71-108">ASEv3SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d71-108">ASEv3SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3d71-109">설명</span><span class="sxs-lookup"><span data-stu-id="c3d71-109">DESCRIPTION</span></span>
<span data-ttu-id="c3d71-110">**New-AzAppServiceEnvironment** cmdlet은 App Service 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-110">The **New-AzAppServiceEnvironment** cmdlet creates an App Service Environment.</span></span>

## <span data-ttu-id="c3d71-111">예제</span><span class="sxs-lookup"><span data-stu-id="c3d71-111">EXAMPLES</span></span>

### <span data-ttu-id="c3d71-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3d71-112">Example 1</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
```

<span data-ttu-id="c3d71-113">권장 경로 테이블 및 네트워크 보안 그룹을 포함하여 MyAseV2라는 App Service Environment 만들기</span><span class="sxs-lookup"><span data-stu-id="c3d71-113">Create App Service Environment named MyAseV2 including recommended Route Table and Network Security Group</span></span>

### <span data-ttu-id="c3d71-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c3d71-114">Example 2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
        -SkipRouteTable -SkipNetworkSecurityGroup
```

<span data-ttu-id="c3d71-115">권장 경로 테이블 및 네트워크 보안 그룹 없이 MyAseV2라는 App Service Environment를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-115">Create App Service Environment named MyAseV2 without recommended Route Table and Network Security Group.</span></span>
<span data-ttu-id="c3d71-116">이러한 인스턴스는 기능 인스턴스를 보장하기 위해 App Service Environment를 프로비전한 직후 또는 직후에 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-116">These should be create before or right after provisioning the App Service Environment to ensure a functional instance.</span></span>

## <span data-ttu-id="c3d71-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c3d71-117">PARAMETERS</span></span>

### <span data-ttu-id="c3d71-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3d71-118">-AsJob</span></span>
<span data-ttu-id="c3d71-119">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c3d71-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d71-120">-DefaultProfile</span></span>
<span data-ttu-id="c3d71-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d71-122">-Kind</span><span class="sxs-lookup"><span data-stu-id="c3d71-122">-Kind</span></span>
<span data-ttu-id="c3d71-123">앱 서비스 환경의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-123">The version of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ASEv2, ASEv3

Required: False
Position: 3
Default value: ASEv2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d71-124">-LoadBalancerMode</span><span class="sxs-lookup"><span data-stu-id="c3d71-124">-LoadBalancerMode</span></span>
<span data-ttu-id="c3d71-125">앱 서비스 환경의 부하 균형 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-125">Load balancer mode of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:
Accepted values: Internal, External

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d71-126">-Location</span><span class="sxs-lookup"><span data-stu-id="c3d71-126">-Location</span></span>
<span data-ttu-id="c3d71-127">앱 서비스 환경의 위치(예: 서유럽).</span><span class="sxs-lookup"><span data-stu-id="c3d71-127">The Location of the app service environment eg: West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d71-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c3d71-128">-Name</span></span>
<span data-ttu-id="c3d71-129">앱 서비스 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-129">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d71-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3d71-130">-PassThru</span></span>
<span data-ttu-id="c3d71-131">앱 서비스 환경 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-131">Return the app service environment object.</span></span>

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

### <span data-ttu-id="c3d71-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d71-132">-ResourceGroupName</span></span>
<span data-ttu-id="c3d71-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d71-134">-SkipNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c3d71-134">-SkipNetworkSecurityGroup</span></span>
<span data-ttu-id="c3d71-135">앱 서비스 환경의 일부로 권장되는 네트워크 보안 그룹을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-135">Do not create the recommended network security group as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d71-136">-SkipRouteTable</span><span class="sxs-lookup"><span data-stu-id="c3d71-136">-SkipRouteTable</span></span>
<span data-ttu-id="c3d71-137">앱 서비스 환경의 일부로 권장 경로 테이블을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-137">Do not create the recommended route table as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d71-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c3d71-138">-SubnetId</span></span>
<span data-ttu-id="c3d71-139">서브넷 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-139">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetIdParameterSet, ASEv3SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d71-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c3d71-140">-SubnetName</span></span>
<span data-ttu-id="c3d71-141">서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-141">The subnet name.</span></span> <span data-ttu-id="c3d71-142">-VirtualNetworkName과 함께 사용하며 ASE와 동일한 리소스 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-142">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="c3d71-143">그렇지 않은 경우 -SubnetId를 사용</span><span class="sxs-lookup"><span data-stu-id="c3d71-143">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d71-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c3d71-144">-VirtualNetworkName</span></span>
<span data-ttu-id="c3d71-145">vNet 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-145">The vNet name.</span></span> <span data-ttu-id="c3d71-146">-SubnetName과 함께 사용하며 ASE와 동일한 리소스 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-146">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="c3d71-147">그렇지 않은 경우 -SubnetId를 사용</span><span class="sxs-lookup"><span data-stu-id="c3d71-147">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d71-148">-확인</span><span class="sxs-lookup"><span data-stu-id="c3d71-148">-Confirm</span></span>
<span data-ttu-id="c3d71-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d71-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d71-150">-WhatIf</span></span>
<span data-ttu-id="c3d71-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d71-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d71-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d71-153">CommonParameters</span></span>
<span data-ttu-id="c3d71-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3d71-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d71-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3d71-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d71-156">입력</span><span class="sxs-lookup"><span data-stu-id="c3d71-156">INPUTS</span></span>

### <span data-ttu-id="c3d71-157">없음</span><span class="sxs-lookup"><span data-stu-id="c3d71-157">None</span></span>

## <span data-ttu-id="c3d71-158">출력</span><span class="sxs-lookup"><span data-stu-id="c3d71-158">OUTPUTS</span></span>

### <span data-ttu-id="c3d71-159">System.Object</span><span class="sxs-lookup"><span data-stu-id="c3d71-159">System.Object</span></span>
## <span data-ttu-id="c3d71-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3d71-160">NOTES</span></span>

## <span data-ttu-id="c3d71-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3d71-161">RELATED LINKS</span></span>

[<span data-ttu-id="c3d71-162">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3d71-162">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="c3d71-163">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="c3d71-163">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="c3d71-164">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3d71-164">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)
