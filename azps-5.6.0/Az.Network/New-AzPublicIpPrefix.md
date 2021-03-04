---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: c72c4ad67f6096f5ba86924219670be53a725d26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953899"
---
# <span data-ttu-id="5c78e-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c78e-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="5c78e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c78e-102">SYNOPSIS</span></span>
<span data-ttu-id="5c78e-103">공용 IP 프리픽스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="5c78e-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c78e-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c78e-105">설명</span><span class="sxs-lookup"><span data-stu-id="5c78e-105">DESCRIPTION</span></span>
<span data-ttu-id="5c78e-106">**New-AzPublicIpPrefix** cmdlet은 공용 IP 프리픽스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="5c78e-107">예제</span><span class="sxs-lookup"><span data-stu-id="5c78e-107">EXAMPLES</span></span>

### <span data-ttu-id="5c78e-108">예제 1: 새 공용 IP 연결부 만들기</span><span class="sxs-lookup"><span data-stu-id="5c78e-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="5c78e-109">이 명령은 새 공용 IP 연결부 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="5c78e-110">예제 2: 새 전역 공용 IP 연결부 만들기</span><span class="sxs-lookup"><span data-stu-id="5c78e-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="5c78e-111">이 명령은 새 전역 공용 IP 강두사 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="5c78e-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5c78e-112">PARAMETERS</span></span>

### <span data-ttu-id="5c78e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c78e-113">-AsJob</span></span>
<span data-ttu-id="5c78e-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5c78e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c78e-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c78e-115">-CustomIpPrefix</span></span>
<span data-ttu-id="5c78e-116">이 PublicIpPrefix가 연결된 CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c78e-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c78e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c78e-117">-DefaultProfile</span></span>
<span data-ttu-id="5c78e-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c78e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5c78e-119">-Force</span></span>
<span data-ttu-id="5c78e-120">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5c78e-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="5c78e-121">-IpAddressVersion</span></span>
<span data-ttu-id="5c78e-122">공용 IP 주소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-122">The public IP address version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c78e-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="5c78e-123">-IpTag</span></span>
<span data-ttu-id="5c78e-124">IpTag 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-124">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c78e-125">-Location</span><span class="sxs-lookup"><span data-stu-id="5c78e-125">-Location</span></span>
<span data-ttu-id="5c78e-126">공용 IP 연결 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="5c78e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5c78e-127">-Name</span></span>
<span data-ttu-id="5c78e-128">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c78e-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="5c78e-129">-PrefixLength</span></span>
<span data-ttu-id="5c78e-130">PublicIPPrefix 길이</span><span class="sxs-lookup"><span data-stu-id="5c78e-130">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c78e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c78e-131">-ResourceGroupName</span></span>
<span data-ttu-id="5c78e-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-132">The resource group name.</span></span>

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

### <span data-ttu-id="5c78e-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="5c78e-133">-Sku</span></span>
<span data-ttu-id="5c78e-134">공용 IP 프리픽스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-134">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c78e-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="5c78e-135">-Tag</span></span>
<span data-ttu-id="5c78e-136">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5c78e-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="5c78e-137">-Tier</span></span>
<span data-ttu-id="5c78e-138">공용 IP 프리픽스 Sku 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-138">The public IP Prefix Sku tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c78e-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="5c78e-139">-Zone</span></span>
<span data-ttu-id="5c78e-140">리소스에 할당된 IP를 표시하는 가용성 영역 목록이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="5c78e-141">-확인</span><span class="sxs-lookup"><span data-stu-id="5c78e-141">-Confirm</span></span>
<span data-ttu-id="5c78e-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c78e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c78e-143">-WhatIf</span></span>
<span data-ttu-id="5c78e-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c78e-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c78e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c78e-146">CommonParameters</span></span>
<span data-ttu-id="5c78e-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c78e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c78e-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c78e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c78e-149">입력</span><span class="sxs-lookup"><span data-stu-id="5c78e-149">INPUTS</span></span>

### <span data-ttu-id="5c78e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="5c78e-150">System.String</span></span>

### <span data-ttu-id="5c78e-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="5c78e-151">System.UInt16</span></span>

### <span data-ttu-id="5c78e-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="5c78e-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="5c78e-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5c78e-153">System.String[]</span></span>

### <span data-ttu-id="5c78e-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5c78e-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5c78e-155">출력</span><span class="sxs-lookup"><span data-stu-id="5c78e-155">OUTPUTS</span></span>

### <span data-ttu-id="5c78e-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c78e-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="5c78e-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c78e-157">NOTES</span></span>

## <span data-ttu-id="5c78e-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c78e-158">RELATED LINKS</span></span>

[<span data-ttu-id="5c78e-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c78e-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="5c78e-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c78e-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="5c78e-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c78e-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
