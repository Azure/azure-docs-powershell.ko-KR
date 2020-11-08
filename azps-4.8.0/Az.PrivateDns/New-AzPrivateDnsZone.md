---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 98830e2dbcfc115cd026c33782030bc40fa6763f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214708"
---
# <span data-ttu-id="0d145-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="0d145-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="0d145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d145-102">SYNOPSIS</span></span>
<span data-ttu-id="0d145-103">새 개인 DNS 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="0d145-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d145-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d145-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0d145-105">DESCRIPTION</span></span>
<span data-ttu-id="0d145-106">**AzPrivateDnsZone** cmdlet은 지정 된 리소스 그룹에 새 DNS (개인 도메인 이름 시스템) 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="0d145-107">*Name* 매개 변수에 고유한 개인 DNS 영역 이름을 지정 해야 하며 그렇지 않으면 cmdlet이 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="0d145-108">영역이 만들어지면 New-AzPrivateDnsRecordSet cmdlet을 사용 하 여 영역에서 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="0d145-109">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="0d145-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0d145-110">EXAMPLES</span></span>

### <span data-ttu-id="0d145-111">예제 1: 개인 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="0d145-111">Example 1: Create a Private DNS zone</span></span>
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

## <span data-ttu-id="0d145-112">변수</span><span class="sxs-lookup"><span data-stu-id="0d145-112">PARAMETERS</span></span>

### <span data-ttu-id="0d145-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d145-113">-DefaultProfile</span></span>
<span data-ttu-id="0d145-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0d145-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d145-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0d145-115">-Name</span></span>
<span data-ttu-id="0d145-116">만들 개인 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="0d145-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d145-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d145-118">영역을 만들 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="0d145-119">태그</span><span class="sxs-lookup"><span data-stu-id="0d145-119">-Tag</span></span>
<span data-ttu-id="0d145-120">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-120">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="0d145-121">-확인</span><span class="sxs-lookup"><span data-stu-id="0d145-121">-Confirm</span></span>
<span data-ttu-id="0d145-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d145-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d145-123">-WhatIf</span></span>
<span data-ttu-id="0d145-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d145-125">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d145-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d145-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d145-127">CommonParameters</span></span>
<span data-ttu-id="0d145-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d145-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d145-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d145-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d145-130">입력</span><span class="sxs-lookup"><span data-stu-id="0d145-130">INPUTS</span></span>

### <span data-ttu-id="0d145-131">않아야</span><span class="sxs-lookup"><span data-stu-id="0d145-131">None</span></span>

## <span data-ttu-id="0d145-132">출력</span><span class="sxs-lookup"><span data-stu-id="0d145-132">OUTPUTS</span></span>

### <span data-ttu-id="0d145-133">PrivateDns. PSPrivateDnsZone/.</span><span class="sxs-lookup"><span data-stu-id="0d145-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="0d145-134">상속자</span><span class="sxs-lookup"><span data-stu-id="0d145-134">NOTES</span></span>

## <span data-ttu-id="0d145-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d145-135">RELATED LINKS</span></span>

[<span data-ttu-id="0d145-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="0d145-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="0d145-137">새로운 AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="0d145-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="0d145-138">제거-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="0d145-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
