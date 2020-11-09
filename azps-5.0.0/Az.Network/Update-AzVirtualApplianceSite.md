---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310730"
---
# <span data-ttu-id="69ab5-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="69ab5-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="69ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="69ab5-103">네트워크 가상 기기 리소스에 연결 된 가상 기기 사이트를 변경 하거나 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="69ab5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69ab5-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69ab5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69ab5-105">DESCRIPTION</span></span>
<span data-ttu-id="69ab5-106">Update-AzVirtualApplianceSite 명령은 가상 기기 사이트 리소스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="69ab5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69ab5-107">EXAMPLES</span></span>

### <span data-ttu-id="69ab5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="69ab5-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="69ab5-109">가상 기기 사이트 리소스에 대 한 주소 접두사를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="69ab5-110">변수</span><span class="sxs-lookup"><span data-stu-id="69ab5-110">PARAMETERS</span></span>

### <span data-ttu-id="69ab5-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="69ab5-111">-AddresssPrefix</span></span>
<span data-ttu-id="69ab5-112">사이트의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-112">The address prefix for the site.</span></span>

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

### <span data-ttu-id="69ab5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69ab5-113">-AsJob</span></span>
<span data-ttu-id="69ab5-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="69ab5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69ab5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ab5-115">-DefaultProfile</span></span>
<span data-ttu-id="69ab5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69ab5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="69ab5-117">-Force</span></span>
<span data-ttu-id="69ab5-118">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="69ab5-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="69ab5-119">-이름</span><span class="sxs-lookup"><span data-stu-id="69ab5-119">-Name</span></span>
<span data-ttu-id="69ab5-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-120">The resource name.</span></span>

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

### <span data-ttu-id="69ab5-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="69ab5-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="69ab5-122">이 사이트가 연결 된 네트워크 가상 어플라이언스입니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="69ab5-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="69ab5-123">-O365Policy</span></span>
<span data-ttu-id="69ab5-124">Office 365 브레이크 아웃 정책.</span><span class="sxs-lookup"><span data-stu-id="69ab5-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ab5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ab5-125">-ResourceGroupName</span></span>
<span data-ttu-id="69ab5-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-126">The resource group name.</span></span>

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

### <span data-ttu-id="69ab5-127">태그</span><span class="sxs-lookup"><span data-stu-id="69ab5-127">-Tag</span></span>
<span data-ttu-id="69ab5-128">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="69ab5-129">-확인</span><span class="sxs-lookup"><span data-stu-id="69ab5-129">-Confirm</span></span>
<span data-ttu-id="69ab5-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69ab5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ab5-131">-WhatIf</span></span>
<span data-ttu-id="69ab5-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69ab5-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69ab5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ab5-134">CommonParameters</span></span>
<span data-ttu-id="69ab5-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69ab5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ab5-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69ab5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ab5-137">입력</span><span class="sxs-lookup"><span data-stu-id="69ab5-137">INPUTS</span></span>

### <span data-ttu-id="69ab5-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="69ab5-138">System.String</span></span>

### <span data-ttu-id="69ab5-139">PSOffice365PolicyProperties에 대 한.</span><span class="sxs-lookup"><span data-stu-id="69ab5-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="69ab5-140">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="69ab5-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="69ab5-141">출력</span><span class="sxs-lookup"><span data-stu-id="69ab5-141">OUTPUTS</span></span>

### <span data-ttu-id="69ab5-142">PSVirtualApplianceSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="69ab5-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="69ab5-143">상속자</span><span class="sxs-lookup"><span data-stu-id="69ab5-143">NOTES</span></span>

## <span data-ttu-id="69ab5-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69ab5-144">RELATED LINKS</span></span>
