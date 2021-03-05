---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: d135cc72a9830535d6b67ce80f29725a569894e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977787"
---
# <span data-ttu-id="b6d18-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b6d18-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="b6d18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6d18-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d18-103">새 개인 DNS 영역 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="b6d18-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6d18-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6d18-105">설명</span><span class="sxs-lookup"><span data-stu-id="b6d18-105">DESCRIPTION</span></span>
<span data-ttu-id="b6d18-106">**New-AzPrivateDnsZone cmdlet은** 지정된 리소스 그룹에 새 DNS(개인 도메인 이름 시스템) 지역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="b6d18-107">이름 매개 변수에 대한 고유한  개인 DNS 영역 이름을 지정해야 합니다. 또는 cmdlet에서 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="b6d18-108">영역이 만들어진 후 New-AzPrivateDnsRecordSet cmdlet을 사용하여 영역의 레코드 집합을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="b6d18-109">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="b6d18-110">예제</span><span class="sxs-lookup"><span data-stu-id="b6d18-110">EXAMPLES</span></span>

### <span data-ttu-id="b6d18-111">예제 1: 개인 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="b6d18-111">Example 1: Create a Private DNS zone</span></span>
```
PS C:\>$Zone = New-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"


This command creates a new private DNS zone named myzone.com in the specified resource group, and then
stores it in the $Zone variable. $Zone object looks something like this,

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="b6d18-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6d18-112">PARAMETERS</span></span>

### <span data-ttu-id="b6d18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d18-113">-DefaultProfile</span></span>
<span data-ttu-id="b6d18-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b6d18-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6d18-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b6d18-115">-Name</span></span>
<span data-ttu-id="b6d18-116">만들 개인 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-116">Specifies the name of the private DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6d18-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6d18-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6d18-118">영역 만들기를 위한 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-118">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6d18-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6d18-119">-Tag</span></span>
<span data-ttu-id="b6d18-120">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-120">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6d18-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b6d18-121">-Confirm</span></span>
<span data-ttu-id="b6d18-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6d18-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6d18-123">-WhatIf</span></span>
<span data-ttu-id="b6d18-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6d18-125">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6d18-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6d18-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d18-127">CommonParameters</span></span>
<span data-ttu-id="b6d18-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d18-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d18-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b6d18-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d18-130">입력</span><span class="sxs-lookup"><span data-stu-id="b6d18-130">INPUTS</span></span>

### <span data-ttu-id="b6d18-131">없음</span><span class="sxs-lookup"><span data-stu-id="b6d18-131">None</span></span>

## <span data-ttu-id="b6d18-132">출력</span><span class="sxs-lookup"><span data-stu-id="b6d18-132">OUTPUTS</span></span>

### <span data-ttu-id="b6d18-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b6d18-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="b6d18-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6d18-134">NOTES</span></span>

## <span data-ttu-id="b6d18-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6d18-135">RELATED LINKS</span></span>

[<span data-ttu-id="b6d18-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b6d18-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="b6d18-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b6d18-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="b6d18-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b6d18-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
