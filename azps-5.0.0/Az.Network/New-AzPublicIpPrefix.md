---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: cc00afb5dcdd4cc11c61cf96f2ae8ac3bb201bb5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215973"
---
# <span data-ttu-id="89d8d-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="89d8d-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="89d8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="89d8d-103">공용 IP 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="89d8d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89d8d-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89d8d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89d8d-105">DESCRIPTION</span></span>
<span data-ttu-id="89d8d-106">**새 AzPublicIpPrefix** cmdlet은 공용 IP 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="89d8d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="89d8d-107">EXAMPLES</span></span>

### <span data-ttu-id="89d8d-108">예제 1: 새 공용 Ip 접두사 만들기</span><span class="sxs-lookup"><span data-stu-id="89d8d-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="89d8d-109">이 명령은 새 공용 IP 접두사 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="89d8d-110">변수</span><span class="sxs-lookup"><span data-stu-id="89d8d-110">PARAMETERS</span></span>

### <span data-ttu-id="89d8d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89d8d-111">-AsJob</span></span>
<span data-ttu-id="89d8d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="89d8d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89d8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d8d-113">-DefaultProfile</span></span>
<span data-ttu-id="89d8d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89d8d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="89d8d-115">-Force</span></span>
<span data-ttu-id="89d8d-116">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="89d8d-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="89d8d-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="89d8d-117">-IpAddressVersion</span></span>
<span data-ttu-id="89d8d-118">공용 IP 주소 버전.</span><span class="sxs-lookup"><span data-stu-id="89d8d-118">The public IP address version.</span></span>

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

### <span data-ttu-id="89d8d-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="89d8d-119">-IpTag</span></span>
<span data-ttu-id="89d8d-120">IpTag 목록.</span><span class="sxs-lookup"><span data-stu-id="89d8d-120">IpTag List.</span></span>

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

### <span data-ttu-id="89d8d-121">-위치</span><span class="sxs-lookup"><span data-stu-id="89d8d-121">-Location</span></span>
<span data-ttu-id="89d8d-122">공용 IP 접두사 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="89d8d-123">-이름</span><span class="sxs-lookup"><span data-stu-id="89d8d-123">-Name</span></span>
<span data-ttu-id="89d8d-124">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-124">The resource name.</span></span>

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

### <span data-ttu-id="89d8d-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="89d8d-125">-PrefixLength</span></span>
<span data-ttu-id="89d8d-126">PublicIPPrefix 길이</span><span class="sxs-lookup"><span data-stu-id="89d8d-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="89d8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89d8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="89d8d-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-128">The resource group name.</span></span>

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

### <span data-ttu-id="89d8d-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="89d8d-129">-Sku</span></span>
<span data-ttu-id="89d8d-130">공용 IP 접두사 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="89d8d-131">태그</span><span class="sxs-lookup"><span data-stu-id="89d8d-131">-Tag</span></span>
<span data-ttu-id="89d8d-132">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="89d8d-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="89d8d-133">-Zone</span></span>
<span data-ttu-id="89d8d-134">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="89d8d-135">-확인</span><span class="sxs-lookup"><span data-stu-id="89d8d-135">-Confirm</span></span>
<span data-ttu-id="89d8d-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89d8d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89d8d-137">-WhatIf</span></span>
<span data-ttu-id="89d8d-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89d8d-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89d8d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d8d-140">CommonParameters</span></span>
<span data-ttu-id="89d8d-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d8d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d8d-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89d8d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d8d-143">입력</span><span class="sxs-lookup"><span data-stu-id="89d8d-143">INPUTS</span></span>

### <span data-ttu-id="89d8d-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89d8d-144">System.String</span></span>

### <span data-ttu-id="89d8d-145">시스템 UInt16</span><span class="sxs-lookup"><span data-stu-id="89d8d-145">System.UInt16</span></span>

### <span data-ttu-id="89d8d-146">PSPublicIpPrefixTag [] (으)로</span><span class="sxs-lookup"><span data-stu-id="89d8d-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="89d8d-147">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="89d8d-147">System.String[]</span></span>

### <span data-ttu-id="89d8d-148">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="89d8d-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="89d8d-149">출력</span><span class="sxs-lookup"><span data-stu-id="89d8d-149">OUTPUTS</span></span>

### <span data-ttu-id="89d8d-150">PSPublicIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="89d8d-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="89d8d-151">상속자</span><span class="sxs-lookup"><span data-stu-id="89d8d-151">NOTES</span></span>

## <span data-ttu-id="89d8d-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89d8d-152">RELATED LINKS</span></span>

[<span data-ttu-id="89d8d-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="89d8d-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="89d8d-154">제거-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="89d8d-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="89d8d-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="89d8d-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
