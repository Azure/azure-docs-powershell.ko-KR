---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironmentinboundservices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
ms.openlocfilehash: 68b2957e959365187ad82980bd2be2f055632a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002112"
---
# <span data-ttu-id="493a3-101">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="493a3-101">New-AzAppServiceEnvironmentInboundServices</span></span>

## <span data-ttu-id="493a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="493a3-102">SYNOPSIS</span></span>
<span data-ttu-id="493a3-103">App Service Environment에 대한 인바운드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-103">Creates inbound services for App Service Environment.</span></span> <span data-ttu-id="493a3-104">ASEv2 ILB의 경우 내부 IP에 매핑할 Azure Private DNS 영역과 레코드가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-104">For ASEv2 ILB, this will create an Azure Private DNS Zone and records to map to the internal IP.</span></span> <span data-ttu-id="493a3-105">ASEv3의 경우 서브넷에 네트워크 정책을 사용하지 않도록 설정하고 개인 엔드포인트를 만들 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-105">For ASEv3 it will in addition ensure subnet has Network Policy disabled and will create a private endpoint.</span></span>

## <span data-ttu-id="493a3-106">구문</span><span class="sxs-lookup"><span data-stu-id="493a3-106">SYNTAX</span></span>

### <span data-ttu-id="493a3-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="493a3-107">SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkName <String> -SubnetName <String> [-SkipDns] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="493a3-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="493a3-108">SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String> -SubnetId <String>
 [-SkipDns] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="493a3-109">설명</span><span class="sxs-lookup"><span data-stu-id="493a3-109">DESCRIPTION</span></span>
<span data-ttu-id="493a3-110">**New-AzAppServiceEnvironmentInboundServices** cmdlet은 App Service Environment에 대한 인바운드 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-110">The **New-AzAppServiceEnvironmentInboundServices** cmdlet create inbound services for an App Service Environment.</span></span>

## <span data-ttu-id="493a3-111">예제</span><span class="sxs-lookup"><span data-stu-id="493a3-111">EXAMPLES</span></span>

### <span data-ttu-id="493a3-112">예제 1: ASEv2에 대한 개인 DNS 영역 및 레코드 만들기</span><span class="sxs-lookup"><span data-stu-id="493a3-112">Example 1: Create Private DNS Zone and records for ASEv2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="493a3-113">ASEv2에 대한 개인 DNS 영역 및 레코드 만들기</span><span class="sxs-lookup"><span data-stu-id="493a3-113">Create Private DNS Zone and records for ASEv2</span></span>

### <span data-ttu-id="493a3-114">예제 2: ASEv3에 대한 개인 엔드포인트, 개인 DNS 영역 및 레코드 만들기</span><span class="sxs-lookup"><span data-stu-id="493a3-114">Example 2: Create private endpoint, Private DNS Zone and records for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="493a3-115">ASEv3에 대한 개인 엔드포인트, 개인 DNS 영역 및 레코드 만들기</span><span class="sxs-lookup"><span data-stu-id="493a3-115">Create private endpoint, Private DNS Zone and records for ASEv3</span></span>

### <span data-ttu-id="493a3-116">예제 3: ASEv3용 개인 엔드포인트 만들기</span><span class="sxs-lookup"><span data-stu-id="493a3-116">Example 3: Create private endpoint for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet -SkipDns
```

<span data-ttu-id="493a3-117">ASEv3용 개인 엔드포인트 만들기</span><span class="sxs-lookup"><span data-stu-id="493a3-117">Create private endpoint for ASEv3</span></span>

## <span data-ttu-id="493a3-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="493a3-118">PARAMETERS</span></span>

### <span data-ttu-id="493a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493a3-119">-DefaultProfile</span></span>
<span data-ttu-id="493a3-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="493a3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="493a3-121">-Name</span></span>
<span data-ttu-id="493a3-122">앱 서비스 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-122">The name of the app service environment.</span></span>

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

### <span data-ttu-id="493a3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="493a3-123">-PassThru</span></span>
<span data-ttu-id="493a3-124">상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-124">Return status.</span></span>

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

### <span data-ttu-id="493a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="493a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="493a3-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="493a3-127">-SkipDns</span><span class="sxs-lookup"><span data-stu-id="493a3-127">-SkipDns</span></span>
<span data-ttu-id="493a3-128">Azure Private DNS 영역 및 레코드를 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-128">Do not create Azure Private DNS Zone and records.</span></span>

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

### <span data-ttu-id="493a3-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="493a3-129">-SubnetId</span></span>
<span data-ttu-id="493a3-130">서브넷 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-130">The subnet id.</span></span>

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

### <span data-ttu-id="493a3-131">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="493a3-131">-SubnetName</span></span>
<span data-ttu-id="493a3-132">서브넷 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-132">The subnet name.</span></span> <span data-ttu-id="493a3-133">-VirtualNetworkName과 함께 사용하며 ASE와 동일한 리소스 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-133">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="493a3-134">그렇지 않은 경우 -SubnetId를 사용</span><span class="sxs-lookup"><span data-stu-id="493a3-134">If not, use -SubnetId</span></span>

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

### <span data-ttu-id="493a3-135">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="493a3-135">-VirtualNetworkName</span></span>
<span data-ttu-id="493a3-136">vNet 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-136">The vNet name.</span></span> <span data-ttu-id="493a3-137">-SubnetName과 함께 사용하며 ASE와 동일한 리소스 그룹에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-137">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="493a3-138">그렇지 않은 경우 -SubnetId를 사용</span><span class="sxs-lookup"><span data-stu-id="493a3-138">If not, use -SubnetId</span></span>

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

### <span data-ttu-id="493a3-139">-확인</span><span class="sxs-lookup"><span data-stu-id="493a3-139">-Confirm</span></span>
<span data-ttu-id="493a3-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="493a3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="493a3-141">-WhatIf</span></span>
<span data-ttu-id="493a3-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="493a3-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="493a3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493a3-144">CommonParameters</span></span>
<span data-ttu-id="493a3-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="493a3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493a3-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="493a3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493a3-147">입력</span><span class="sxs-lookup"><span data-stu-id="493a3-147">INPUTS</span></span>

### <span data-ttu-id="493a3-148">없음</span><span class="sxs-lookup"><span data-stu-id="493a3-148">None</span></span>

## <span data-ttu-id="493a3-149">출력</span><span class="sxs-lookup"><span data-stu-id="493a3-149">OUTPUTS</span></span>

### <span data-ttu-id="493a3-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="493a3-150">System.Object</span></span>
## <span data-ttu-id="493a3-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="493a3-151">NOTES</span></span>

## <span data-ttu-id="493a3-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="493a3-152">RELATED LINKS</span></span>

[<span data-ttu-id="493a3-153">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="493a3-153">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="493a3-154">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="493a3-154">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="493a3-155">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="493a3-155">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)