---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491031"
---
# <span data-ttu-id="61187-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="61187-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="61187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61187-102">SYNOPSIS</span></span>
<span data-ttu-id="61187-103">네트워크 가상 어플라이언스 리소스를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="61187-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="61187-104">구문</span><span class="sxs-lookup"><span data-stu-id="61187-104">SYNTAX</span></span>

### <span data-ttu-id="61187-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="61187-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61187-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61187-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61187-107">설명</span><span class="sxs-lookup"><span data-stu-id="61187-107">DESCRIPTION</span></span>
<span data-ttu-id="61187-108">New-AzNetworkVirtualAppliance 명령은 Azure에서 네트워크 가상 어플라이언스 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61187-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="61187-109">예제</span><span class="sxs-lookup"><span data-stu-id="61187-109">EXAMPLES</span></span>

### <span data-ttu-id="61187-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="61187-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="61187-111">리소스 그룹: testrg에 새 네트워크 가상 어플라이언스 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="61187-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="61187-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61187-112">PARAMETERS</span></span>

### <span data-ttu-id="61187-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61187-113">-AsJob</span></span>
<span data-ttu-id="61187-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="61187-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61187-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="61187-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="61187-116">부트스트ap 구성 Blob URL입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-116">The Bootstrap configuration blob URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="61187-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="61187-118">일반 텍스트로 Cloudinit 구성</span><span class="sxs-lookup"><span data-stu-id="61187-118">The Cloudinit configuration as plain text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="61187-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="61187-120">Cloudinit 구성 Blob Storage URL입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-120">The Cloudinit configuration blob storage URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61187-121">-DefaultProfile</span></span>
<span data-ttu-id="61187-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61187-123">-Force</span><span class="sxs-lookup"><span data-stu-id="61187-123">-Force</span></span>
<span data-ttu-id="61187-124">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61187-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="61187-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="61187-125">-Identity</span></span>
<span data-ttu-id="61187-126">관리 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-126">The Managed identity.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-127">-Location</span><span class="sxs-lookup"><span data-stu-id="61187-127">-Location</span></span>
<span data-ttu-id="61187-128">공용 IP 주소 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-128">The public IP address location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-129">-Name</span><span class="sxs-lookup"><span data-stu-id="61187-129">-Name</span></span>
<span data-ttu-id="61187-130">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61187-131">-ResourceGroupName</span></span>
<span data-ttu-id="61187-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61187-133">-ResourceId</span></span>
<span data-ttu-id="61187-134">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="61187-135">-Sku</span></span>
<span data-ttu-id="61187-136">가상 어플라이언스의 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-136">The Sku of the Virtual Appliance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="61187-137">-Tag</span></span>
<span data-ttu-id="61187-138">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-138">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="61187-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="61187-140">가상 어플라이언스의 ASN 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-140">The ASN number of the Virtual Appliance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="61187-141">-VirtualHubId</span></span>
<span data-ttu-id="61187-142">가상 허브의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="61187-142">The Resource Id of the Virtual Hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61187-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61187-143">-Confirm</span></span>
<span data-ttu-id="61187-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="61187-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61187-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61187-145">-WhatIf</span></span>
<span data-ttu-id="61187-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="61187-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61187-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61187-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61187-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61187-148">CommonParameters</span></span>
<span data-ttu-id="61187-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="61187-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61187-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61187-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61187-151">입력</span><span class="sxs-lookup"><span data-stu-id="61187-151">INPUTS</span></span>

### <span data-ttu-id="61187-152">System.String</span><span class="sxs-lookup"><span data-stu-id="61187-152">System.String</span></span>

### <span data-ttu-id="61187-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="61187-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="61187-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="61187-154">System.Int32</span></span>

### <span data-ttu-id="61187-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="61187-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="61187-156">System.String[]</span><span class="sxs-lookup"><span data-stu-id="61187-156">System.String[]</span></span>

### <span data-ttu-id="61187-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="61187-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="61187-158">출력</span><span class="sxs-lookup"><span data-stu-id="61187-158">OUTPUTS</span></span>

### <span data-ttu-id="61187-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="61187-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="61187-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="61187-160">NOTES</span></span>

## <span data-ttu-id="61187-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61187-161">RELATED LINKS</span></span>