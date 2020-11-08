---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211558"
---
# <span data-ttu-id="ab3cd-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="ab3cd-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="ab3cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab3cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3cd-103">네트워크 가상 기기에 연결 된 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="ab3cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab3cd-104">SYNTAX</span></span>

### <span data-ttu-id="ab3cd-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ab3cd-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab3cd-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab3cd-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab3cd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ab3cd-107">DESCRIPTION</span></span>
<span data-ttu-id="ab3cd-108">New-AzVirtualApplianceSite 명령은 네트워크 가상 기기 리소스에 연결 된 가상 기기 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ab3cd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ab3cd-109">EXAMPLES</span></span>

### <span data-ttu-id="ab3cd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab3cd-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="ab3cd-111">리소스 그룹: testrg에서 새 가상 기기 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="ab3cd-112">변수</span><span class="sxs-lookup"><span data-stu-id="ab3cd-112">PARAMETERS</span></span>

### <span data-ttu-id="ab3cd-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ab3cd-113">-AddressPrefix</span></span>
<span data-ttu-id="ab3cd-114">사이트의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="ab3cd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab3cd-115">-AsJob</span></span>
<span data-ttu-id="ab3cd-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ab3cd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab3cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab3cd-117">-DefaultProfile</span></span>
<span data-ttu-id="ab3cd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab3cd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ab3cd-119">-Force</span></span>
<span data-ttu-id="ab3cd-120">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="ab3cd-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ab3cd-121">-이름</span><span class="sxs-lookup"><span data-stu-id="ab3cd-121">-Name</span></span>
<span data-ttu-id="ab3cd-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-122">The resource name.</span></span>

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

### <span data-ttu-id="ab3cd-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="ab3cd-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="ab3cd-124">이 사이트가 연결 된 네트워크 가상 어플라이언스입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="ab3cd-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="ab3cd-125">-O365Policy</span></span>
<span data-ttu-id="ab3cd-126">Office 365 브레이크 아웃 정책.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3cd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab3cd-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab3cd-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-128">The resource group name.</span></span>

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

### <span data-ttu-id="ab3cd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab3cd-129">-ResourceId</span></span>
<span data-ttu-id="ab3cd-130">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-130">The resource id.</span></span>

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

### <span data-ttu-id="ab3cd-131">태그</span><span class="sxs-lookup"><span data-stu-id="ab3cd-131">-Tag</span></span>
<span data-ttu-id="ab3cd-132">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ab3cd-133">-확인</span><span class="sxs-lookup"><span data-stu-id="ab3cd-133">-Confirm</span></span>
<span data-ttu-id="ab3cd-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab3cd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab3cd-135">-WhatIf</span></span>
<span data-ttu-id="ab3cd-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab3cd-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab3cd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3cd-138">CommonParameters</span></span>
<span data-ttu-id="ab3cd-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3cd-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3cd-141">입력</span><span class="sxs-lookup"><span data-stu-id="ab3cd-141">INPUTS</span></span>

### <span data-ttu-id="ab3cd-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab3cd-142">System.String</span></span>

### <span data-ttu-id="ab3cd-143">PSOffice365PolicyProperties에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="ab3cd-144">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ab3cd-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ab3cd-145">출력</span><span class="sxs-lookup"><span data-stu-id="ab3cd-145">OUTPUTS</span></span>

### <span data-ttu-id="ab3cd-146">PSVirtualApplianceSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ab3cd-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="ab3cd-147">상속자</span><span class="sxs-lookup"><span data-stu-id="ab3cd-147">NOTES</span></span>

## <span data-ttu-id="ab3cd-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab3cd-148">RELATED LINKS</span></span>
