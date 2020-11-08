---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 1e5fbeba85431ab593d4daedff0f8b71af13ace4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042510"
---
# <span data-ttu-id="37a81-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="37a81-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="37a81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37a81-102">SYNOPSIS</span></span>
<span data-ttu-id="37a81-103">수정 된 azure 방화벽 정책 저장</span><span class="sxs-lookup"><span data-stu-id="37a81-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="37a81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37a81-104">SYNTAX</span></span>

### <span data-ttu-id="37a81-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="37a81-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37a81-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37a81-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37a81-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37a81-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>] [-BasePolicy <String>]
 -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37a81-108">설명은</span><span class="sxs-lookup"><span data-stu-id="37a81-108">DESCRIPTION</span></span>
<span data-ttu-id="37a81-109">**AzFirewallPolicy** Cmdlet은 Azure 방화벽 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="37a81-110">예제의</span><span class="sxs-lookup"><span data-stu-id="37a81-110">EXAMPLES</span></span>

### <span data-ttu-id="37a81-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="37a81-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="37a81-112">이 예제에서는 새 방화벽 정책 값을 사용 하 여 방화벽 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="37a81-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="37a81-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="37a81-114">이 예제에서는 새 위협 intel 모드를 사용 하 여 방화벽 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-114">This example sets the firewall policy with the new threat intel mode</span></span>

## <span data-ttu-id="37a81-115">변수</span><span class="sxs-lookup"><span data-stu-id="37a81-115">PARAMETERS</span></span>

### <span data-ttu-id="37a81-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37a81-116">-AsJob</span></span>
<span data-ttu-id="37a81-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="37a81-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37a81-118">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="37a81-118">-BasePolicy</span></span>
<span data-ttu-id="37a81-119">상속할 기본 정책</span><span class="sxs-lookup"><span data-stu-id="37a81-119">The base policy to inherit from</span></span>

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

### <span data-ttu-id="37a81-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a81-120">-DefaultProfile</span></span>
<span data-ttu-id="37a81-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37a81-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37a81-122">-InputObject</span></span>
<span data-ttu-id="37a81-123">AzureFirewall 정책</span><span class="sxs-lookup"><span data-stu-id="37a81-123">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37a81-124">-위치</span><span class="sxs-lookup"><span data-stu-id="37a81-124">-Location</span></span>
<span data-ttu-id="37a81-125">location.</span><span class="sxs-lookup"><span data-stu-id="37a81-125">location.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a81-126">-이름</span><span class="sxs-lookup"><span data-stu-id="37a81-126">-Name</span></span>
<span data-ttu-id="37a81-127">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a81-128">-ResourceGroupName</span></span>
<span data-ttu-id="37a81-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a81-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37a81-130">-ResourceId</span></span>
<span data-ttu-id="37a81-131">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-131">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a81-132">태그</span><span class="sxs-lookup"><span data-stu-id="37a81-132">-Tag</span></span>
<span data-ttu-id="37a81-133">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="37a81-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="37a81-134">-ThreatIntelMode</span></span>
<span data-ttu-id="37a81-135">위협 인텔리전스의 작동 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a81-136">-확인</span><span class="sxs-lookup"><span data-stu-id="37a81-136">-Confirm</span></span>
<span data-ttu-id="37a81-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37a81-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37a81-138">-WhatIf</span></span>
<span data-ttu-id="37a81-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37a81-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37a81-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a81-141">CommonParameters</span></span>
<span data-ttu-id="37a81-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37a81-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a81-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="37a81-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a81-144">입력</span><span class="sxs-lookup"><span data-stu-id="37a81-144">INPUTS</span></span>

### <span data-ttu-id="37a81-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="37a81-145">System.String</span></span>

### <span data-ttu-id="37a81-146">PSAzureFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="37a81-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="37a81-147">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="37a81-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="37a81-148">출력</span><span class="sxs-lookup"><span data-stu-id="37a81-148">OUTPUTS</span></span>

### <span data-ttu-id="37a81-149">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="37a81-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="37a81-150">상속자</span><span class="sxs-lookup"><span data-stu-id="37a81-150">NOTES</span></span>

## <span data-ttu-id="37a81-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37a81-151">RELATED LINKS</span></span>
