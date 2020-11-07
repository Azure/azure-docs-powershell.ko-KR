---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 5c432224891de6c2fcadc42ae308e9607bc3e432
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877268"
---
# <span data-ttu-id="d8d26-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d8d26-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="d8d26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d26-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d26-103">새 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="d8d26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8d26-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8d26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8d26-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d26-106">**새 AzFirewallPolicy** Cmdlet은 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="d8d26-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d8d26-107">EXAMPLES</span></span>

### <span data-ttu-id="d8d26-108">1. 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="d8d26-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="d8d26-109">이 예제에서는 azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-109">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="d8d26-110">2. ThreatIntel 모드를 사용 하 여 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="d8d26-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="d8d26-111">이 예제에서는 위협 intel 모드를 사용 하 여 azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-111">This example creates an azure firewall policy with a threat intel mode</span></span>

## <span data-ttu-id="d8d26-112">변수</span><span class="sxs-lookup"><span data-stu-id="d8d26-112">PARAMETERS</span></span>

### <span data-ttu-id="d8d26-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8d26-113">-AsJob</span></span>
<span data-ttu-id="d8d26-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d8d26-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8d26-115">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="d8d26-115">-BasePolicy</span></span>
<span data-ttu-id="d8d26-116">위협 인텔리전스의 작동 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-116">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="d8d26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d26-117">-DefaultProfile</span></span>
<span data-ttu-id="d8d26-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8d26-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d8d26-119">-Force</span></span>
<span data-ttu-id="d8d26-120">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="d8d26-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d8d26-121">-위치</span><span class="sxs-lookup"><span data-stu-id="d8d26-121">-Location</span></span>
<span data-ttu-id="d8d26-122">location.</span><span class="sxs-lookup"><span data-stu-id="d8d26-122">location.</span></span>

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

### <span data-ttu-id="d8d26-123">-이름</span><span class="sxs-lookup"><span data-stu-id="d8d26-123">-Name</span></span>
<span data-ttu-id="d8d26-124">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-124">The resource name.</span></span>

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

### <span data-ttu-id="d8d26-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d26-125">-ResourceGroupName</span></span>
<span data-ttu-id="d8d26-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-126">The resource group name.</span></span>

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

### <span data-ttu-id="d8d26-127">태그</span><span class="sxs-lookup"><span data-stu-id="d8d26-127">-Tag</span></span>
<span data-ttu-id="d8d26-128">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d8d26-129">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="d8d26-129">-ThreatIntelMode</span></span>
<span data-ttu-id="d8d26-130">위협 인텔리전스의 작동 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-130">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="d8d26-131">-확인</span><span class="sxs-lookup"><span data-stu-id="d8d26-131">-Confirm</span></span>
<span data-ttu-id="d8d26-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d26-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d26-133">-WhatIf</span></span>
<span data-ttu-id="d8d26-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d26-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d26-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d26-136">CommonParameters</span></span>
<span data-ttu-id="d8d26-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d26-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d26-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8d26-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d26-139">입력</span><span class="sxs-lookup"><span data-stu-id="d8d26-139">INPUTS</span></span>

### <span data-ttu-id="d8d26-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d8d26-140">System.String</span></span>

### <span data-ttu-id="d8d26-141">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="d8d26-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d8d26-142">출력</span><span class="sxs-lookup"><span data-stu-id="d8d26-142">OUTPUTS</span></span>

### <span data-ttu-id="d8d26-143">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="d8d26-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="d8d26-144">상속자</span><span class="sxs-lookup"><span data-stu-id="d8d26-144">NOTES</span></span>

## <span data-ttu-id="d8d26-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8d26-145">RELATED LINKS</span></span>
