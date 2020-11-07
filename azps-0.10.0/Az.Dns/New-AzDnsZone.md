---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 0b41ff25823e44b31c7ff7677678a332782e7615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876761"
---
# <span data-ttu-id="8ea95-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8ea95-101">New-AzDnsZone</span></span>

## <span data-ttu-id="8ea95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ea95-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea95-103">새 DNS 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="8ea95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ea95-104">SYNTAX</span></span>

```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ea95-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ea95-105">DESCRIPTION</span></span>
<span data-ttu-id="8ea95-106">**AzDnsZone** cmdlet은 지정 된 리소스 그룹에 새 DNS (Domain Name System) 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-106">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="8ea95-107">*Name* 매개 변수에 대해 고유한 DNS 영역 이름을 지정 해야 하며, cmdlet이 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-107">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="8ea95-108">영역이 만들어지면 New-AzDnsRecordSet cmdlet을 사용 하 여 영역에서 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-108">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="8ea95-109">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8ea95-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8ea95-110">EXAMPLES</span></span>

### <span data-ttu-id="8ea95-111">예제 1: DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="8ea95-111">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8ea95-112">이 명령은 지정 된 리소스 그룹에 myzone.com 이라는 새 DNS 영역을 만든 다음이를 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-112">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="8ea95-113">변수</span><span class="sxs-lookup"><span data-stu-id="8ea95-113">PARAMETERS</span></span>

### <span data-ttu-id="8ea95-114">-이름</span><span class="sxs-lookup"><span data-stu-id="8ea95-114">-Name</span></span>
<span data-ttu-id="8ea95-115">만들려는 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-115">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="8ea95-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ea95-116">-ResourceGroupName</span></span>
<span data-ttu-id="8ea95-117">영역을 만들 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-117">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="8ea95-118">태그</span><span class="sxs-lookup"><span data-stu-id="8ea95-118">-Tag</span></span>
<span data-ttu-id="8ea95-119">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8ea95-120">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="8ea95-120">For example:</span></span>

<span data-ttu-id="8ea95-121">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8ea95-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea95-122">-확인</span><span class="sxs-lookup"><span data-stu-id="8ea95-122">-Confirm</span></span>
<span data-ttu-id="8ea95-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea95-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ea95-124">-WhatIf</span></span>
<span data-ttu-id="8ea95-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ea95-126">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ea95-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea95-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea95-128">CommonParameters</span></span>
<span data-ttu-id="8ea95-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea95-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea95-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea95-131">입력</span><span class="sxs-lookup"><span data-stu-id="8ea95-131">INPUTS</span></span>

### <span data-ttu-id="8ea95-132">않아야</span><span class="sxs-lookup"><span data-stu-id="8ea95-132">None</span></span>

<span data-ttu-id="8ea95-133">이 cmdlet에는 입력을 파이프가 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-133">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="8ea95-134">출력</span><span class="sxs-lookup"><span data-stu-id="8ea95-134">OUTPUTS</span></span>

### <span data-ttu-id="8ea95-135">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="8ea95-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

<span data-ttu-id="8ea95-136">이 cmdlet은 새 DNS 영역을 나타내는 DnsZone 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-136">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="8ea95-137">상속자</span><span class="sxs-lookup"><span data-stu-id="8ea95-137">NOTES</span></span>
<span data-ttu-id="8ea95-138">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-138">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8ea95-139">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-139">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="8ea95-140">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-140">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="8ea95-141">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ea95-141">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8ea95-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ea95-142">RELATED LINKS</span></span>

[<span data-ttu-id="8ea95-143">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8ea95-143">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="8ea95-144">새로운 AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8ea95-144">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="8ea95-145">제거-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8ea95-145">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)