---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214824"
---
# <span data-ttu-id="142c9-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="142c9-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="142c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="142c9-102">SYNOPSIS</span></span>
<span data-ttu-id="142c9-103">네트워크 가상 기기 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="142c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="142c9-104">SYNTAX</span></span>

### <span data-ttu-id="142c9-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="142c9-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="142c9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="142c9-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="142c9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="142c9-107">DESCRIPTION</span></span>
<span data-ttu-id="142c9-108">New-AzNetworkVirtualAppliance 명령은 Azure에서 네트워크 가상 어플라이언스 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="142c9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="142c9-109">EXAMPLES</span></span>

### <span data-ttu-id="142c9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="142c9-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="142c9-111">리소스 그룹: testrg에서 새 네트워크 가상 기기 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="142c9-112">변수</span><span class="sxs-lookup"><span data-stu-id="142c9-112">PARAMETERS</span></span>

### <span data-ttu-id="142c9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="142c9-113">-AsJob</span></span>
<span data-ttu-id="142c9-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="142c9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="142c9-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="142c9-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="142c9-116">부트스트랩 구성 blob URL입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="142c9-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="142c9-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="142c9-118">Cloudinit 구성을 일반 텍스트로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="142c9-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="142c9-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="142c9-120">Cloudinit 구성 blob 저장소 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="142c9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="142c9-121">-DefaultProfile</span></span>
<span data-ttu-id="142c9-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="142c9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="142c9-123">-Force</span></span>
<span data-ttu-id="142c9-124">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="142c9-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="142c9-125">-Id</span><span class="sxs-lookup"><span data-stu-id="142c9-125">-Identity</span></span>
<span data-ttu-id="142c9-126">관리 되는 id입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-126">The Managed identity.</span></span>

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

### <span data-ttu-id="142c9-127">-위치</span><span class="sxs-lookup"><span data-stu-id="142c9-127">-Location</span></span>
<span data-ttu-id="142c9-128">공용 IP 주소 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-128">The public IP address location.</span></span>

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

### <span data-ttu-id="142c9-129">-이름</span><span class="sxs-lookup"><span data-stu-id="142c9-129">-Name</span></span>
<span data-ttu-id="142c9-130">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-130">The resource name.</span></span>

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

### <span data-ttu-id="142c9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="142c9-131">-ResourceGroupName</span></span>
<span data-ttu-id="142c9-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-132">The resource group name.</span></span>

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

### <span data-ttu-id="142c9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="142c9-133">-ResourceId</span></span>
<span data-ttu-id="142c9-134">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-134">The resource Id.</span></span>

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

### <span data-ttu-id="142c9-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="142c9-135">-Sku</span></span>
<span data-ttu-id="142c9-136">가상 기기의 Sku입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="142c9-137">태그</span><span class="sxs-lookup"><span data-stu-id="142c9-137">-Tag</span></span>
<span data-ttu-id="142c9-138">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="142c9-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="142c9-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="142c9-140">가상 기기의 ASN 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="142c9-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="142c9-141">-VirtualHubId</span></span>
<span data-ttu-id="142c9-142">가상 허브의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="142c9-143">-확인</span><span class="sxs-lookup"><span data-stu-id="142c9-143">-Confirm</span></span>
<span data-ttu-id="142c9-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="142c9-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="142c9-145">-WhatIf</span></span>
<span data-ttu-id="142c9-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="142c9-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="142c9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="142c9-148">CommonParameters</span></span>
<span data-ttu-id="142c9-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="142c9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="142c9-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="142c9-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="142c9-151">입력</span><span class="sxs-lookup"><span data-stu-id="142c9-151">INPUTS</span></span>

### <span data-ttu-id="142c9-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="142c9-152">System.String</span></span>

### <span data-ttu-id="142c9-153">PSVirtualApplianceSkuProperties에 대 한.</span><span class="sxs-lookup"><span data-stu-id="142c9-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="142c9-154">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="142c9-154">System.Int32</span></span>

### <span data-ttu-id="142c9-155">PSManagedServiceIdentity에 대 한.</span><span class="sxs-lookup"><span data-stu-id="142c9-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="142c9-156">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="142c9-156">System.String[]</span></span>

### <span data-ttu-id="142c9-157">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="142c9-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="142c9-158">출력</span><span class="sxs-lookup"><span data-stu-id="142c9-158">OUTPUTS</span></span>

### <span data-ttu-id="142c9-159">Microsoft. 네트워크 모델. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="142c9-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="142c9-160">상속자</span><span class="sxs-lookup"><span data-stu-id="142c9-160">NOTES</span></span>

## <span data-ttu-id="142c9-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="142c9-161">RELATED LINKS</span></span>
