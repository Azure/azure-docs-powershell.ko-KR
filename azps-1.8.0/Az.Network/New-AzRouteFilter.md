---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: b89772c1afe621e456dfb269fe869b6cd3fa8a8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700281"
---
# <span data-ttu-id="04045-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="04045-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="04045-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04045-102">SYNOPSIS</span></span>
<span data-ttu-id="04045-103">경로 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04045-103">Creates a route filter.</span></span>

## <span data-ttu-id="04045-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04045-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04045-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04045-105">DESCRIPTION</span></span>
<span data-ttu-id="04045-106">New-AzRouteFilter cmdlet은 Azure 경로 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04045-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="04045-107">예제의</span><span class="sxs-lookup"><span data-stu-id="04045-107">EXAMPLES</span></span>

### <span data-ttu-id="04045-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="04045-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="04045-109">명령이 새 경로 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04045-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="04045-110">변수</span><span class="sxs-lookup"><span data-stu-id="04045-110">PARAMETERS</span></span>

### <span data-ttu-id="04045-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04045-111">-AsJob</span></span>
<span data-ttu-id="04045-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="04045-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04045-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04045-113">-DefaultProfile</span></span>
<span data-ttu-id="04045-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04045-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04045-115">-Force</span><span class="sxs-lookup"><span data-stu-id="04045-115">-Force</span></span>
<span data-ttu-id="04045-116">이름이 같은 경로 필터가 이미 있는 경우에도이 cmdlet이 경로 테이블을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="04045-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="04045-117">-위치</span><span class="sxs-lookup"><span data-stu-id="04045-117">-Location</span></span>
<span data-ttu-id="04045-118">이 cmdlet이 경로 필터를 만드는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04045-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="04045-119">-이름</span><span class="sxs-lookup"><span data-stu-id="04045-119">-Name</span></span>
<span data-ttu-id="04045-120">경로 필터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04045-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="04045-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04045-121">-ResourceGroupName</span></span>
<span data-ttu-id="04045-122">이 cmdlet이 경로 필터를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04045-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="04045-123">-규칙</span><span class="sxs-lookup"><span data-stu-id="04045-123">-Rule</span></span>
<span data-ttu-id="04045-124">경로 필터와 연결할 경로 필터 규칙 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04045-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04045-125">태그</span><span class="sxs-lookup"><span data-stu-id="04045-125">-Tag</span></span>
<span data-ttu-id="04045-126">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="04045-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="04045-127">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="04045-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="04045-128">-확인</span><span class="sxs-lookup"><span data-stu-id="04045-128">-Confirm</span></span>
<span data-ttu-id="04045-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04045-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04045-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04045-130">-WhatIf</span></span>
<span data-ttu-id="04045-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04045-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04045-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04045-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04045-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04045-133">CommonParameters</span></span>
<span data-ttu-id="04045-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04045-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04045-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04045-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04045-136">입력</span><span class="sxs-lookup"><span data-stu-id="04045-136">INPUTS</span></span>

### <span data-ttu-id="04045-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="04045-137">System.String</span></span>

### <span data-ttu-id="04045-138">PSRouteFilterRule [] (으)로</span><span class="sxs-lookup"><span data-stu-id="04045-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="04045-139">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="04045-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="04045-140">출력</span><span class="sxs-lookup"><span data-stu-id="04045-140">OUTPUTS</span></span>

### <span data-ttu-id="04045-141">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="04045-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="04045-142">상속자</span><span class="sxs-lookup"><span data-stu-id="04045-142">NOTES</span></span>
<span data-ttu-id="04045-143">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="04045-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="04045-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04045-144">RELATED LINKS</span></span>

[<span data-ttu-id="04045-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="04045-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="04045-146">제거-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="04045-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="04045-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="04045-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="04045-148">추가-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04045-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="04045-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04045-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="04045-150">새로운 AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04045-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="04045-151">제거-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04045-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="04045-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="04045-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
