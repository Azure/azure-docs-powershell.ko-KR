---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
ms.openlocfilehash: d52bc8737392bf6fce004a90b1f2fe5207cffea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711331"
---
# <span data-ttu-id="e3a32-101">New-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e3a32-101">New-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="e3a32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3a32-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a32-103">공용 IP 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-103">Creates a Public IP Prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3a32-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3a32-104">SYNTAX</span></span>

```
New-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a32-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e3a32-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a32-106">**새 AzureRmPublicIpPrefix** cmdlet은 공용 IP 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-106">The **New-AzureRmPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="e3a32-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e3a32-107">EXAMPLES</span></span>

### <span data-ttu-id="e3a32-108">1: 새 공용 Ip 접두사 만들기</span><span class="sxs-lookup"><span data-stu-id="e3a32-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="e3a32-109">이 명령은 새 공용 IP 접두사 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="e3a32-110">변수</span><span class="sxs-lookup"><span data-stu-id="e3a32-110">PARAMETERS</span></span>

### <span data-ttu-id="e3a32-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3a32-111">-AsJob</span></span>
<span data-ttu-id="e3a32-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e3a32-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3a32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a32-113">-DefaultProfile</span></span>
<span data-ttu-id="e3a32-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3a32-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e3a32-115">-Force</span></span>
<span data-ttu-id="e3a32-116">리소스를 overrite 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="e3a32-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="e3a32-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e3a32-117">-IpAddressVersion</span></span>
<span data-ttu-id="e3a32-118">공용 IP 주소 버전.</span><span class="sxs-lookup"><span data-stu-id="e3a32-118">The public IP address version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="e3a32-119">-IpTag</span></span>
<span data-ttu-id="e3a32-120">IpTag 목록.</span><span class="sxs-lookup"><span data-stu-id="e3a32-120">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-121">-위치</span><span class="sxs-lookup"><span data-stu-id="e3a32-121">-Location</span></span>
<span data-ttu-id="e3a32-122">공용 IP 접두사 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-122">The public IP prefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-123">-이름</span><span class="sxs-lookup"><span data-stu-id="e3a32-123">-Name</span></span>
<span data-ttu-id="e3a32-124">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="e3a32-125">-PrefixLength</span></span>
<span data-ttu-id="e3a32-126">PublicIPPrefix 길이</span><span class="sxs-lookup"><span data-stu-id="e3a32-126">The PublicIPPrefix length</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a32-127">-ResourceGroupName</span></span>
<span data-ttu-id="e3a32-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="e3a32-129">-Sku</span></span>
<span data-ttu-id="e3a32-130">공용 IP 접두사 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-131">태그</span><span class="sxs-lookup"><span data-stu-id="e3a32-131">-Tag</span></span>
<span data-ttu-id="e3a32-132">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="e3a32-133">-Zone</span></span>
<span data-ttu-id="e3a32-134">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-135">-확인</span><span class="sxs-lookup"><span data-stu-id="e3a32-135">-Confirm</span></span>
<span data-ttu-id="e3a32-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a32-137">-WhatIf</span></span>
<span data-ttu-id="e3a32-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a32-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a32-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a32-140">CommonParameters</span></span>
<span data-ttu-id="e3a32-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3a32-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e3a32-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a32-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a32-143">입력</span><span class="sxs-lookup"><span data-stu-id="e3a32-143">INPUTS</span></span>

### <span data-ttu-id="e3a32-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3a32-144">System.String</span></span>
<span data-ttu-id="e3a32-145">4.0.0.0에서 목록 `1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List` 1 [[시스템 문자열, mscorlib, Version =, Culture = 중립, PublicKeyToken = b77a5c561934e089]] system.webserver. 컬렉션</span><span class="sxs-lookup"><span data-stu-id="e3a32-145">System.UInt16 System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="e3a32-146">출력</span><span class="sxs-lookup"><span data-stu-id="e3a32-146">OUTPUTS</span></span>

### <span data-ttu-id="e3a32-147">PSPublicIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e3a32-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="e3a32-148">상속자</span><span class="sxs-lookup"><span data-stu-id="e3a32-148">NOTES</span></span>

## <span data-ttu-id="e3a32-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3a32-149">RELATED LINKS</span></span>
