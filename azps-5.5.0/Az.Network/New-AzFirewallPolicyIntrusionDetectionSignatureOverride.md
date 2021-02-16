---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: d2389a8d4880b576e51cda41ac3c15bd091257c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184468"
---
# <span data-ttu-id="e9878-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="e9878-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="e9878-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9878-102">SYNOPSIS</span></span>
<span data-ttu-id="e9878-103">새 Azure Firewall 정책 침입 감지 서명 오버라이드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9878-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="e9878-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9878-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9878-105">설명</span><span class="sxs-lookup"><span data-stu-id="e9878-105">DESCRIPTION</span></span>
<span data-ttu-id="e9878-106">**New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet은 Azure Firewall Policy Signature Override 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9878-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="e9878-107">예제</span><span class="sxs-lookup"><span data-stu-id="e9878-107">EXAMPLES</span></span>

### <span data-ttu-id="e9878-108">예제 1: 1.</span><span class="sxs-lookup"><span data-stu-id="e9878-108">Example 1: 1.</span></span> <span data-ttu-id="e9878-109">서명 오버라이드를 사용하여 침입 감지 만들기</span><span class="sxs-lookup"><span data-stu-id="e9878-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="e9878-110">이 예제에서는 거부 모드로 특정 서명을 오버라이드하여 침입 감지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9878-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="e9878-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9878-111">PARAMETERS</span></span>

### <span data-ttu-id="e9878-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9878-112">-DefaultProfile</span></span>
<span data-ttu-id="e9878-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9878-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9878-114">-Id</span><span class="sxs-lookup"><span data-stu-id="e9878-114">-Id</span></span>
<span data-ttu-id="e9878-115">서명 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e9878-115">Signature id.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9878-116">-Mode</span><span class="sxs-lookup"><span data-stu-id="e9878-116">-Mode</span></span>
<span data-ttu-id="e9878-117">서명 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e9878-117">Signature state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9878-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9878-118">-Confirm</span></span>
<span data-ttu-id="e9878-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9878-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9878-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9878-120">-WhatIf</span></span>
<span data-ttu-id="e9878-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e9878-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9878-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9878-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9878-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9878-123">CommonParameters</span></span>
<span data-ttu-id="e9878-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9878-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9878-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9878-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9878-126">입력</span><span class="sxs-lookup"><span data-stu-id="e9878-126">INPUTS</span></span>

### <span data-ttu-id="e9878-127">없음</span><span class="sxs-lookup"><span data-stu-id="e9878-127">None</span></span>

## <span data-ttu-id="e9878-128">출력</span><span class="sxs-lookup"><span data-stu-id="e9878-128">OUTPUTS</span></span>

### <span data-ttu-id="e9878-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="e9878-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="e9878-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9878-130">NOTES</span></span>

## <span data-ttu-id="e9878-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9878-131">RELATED LINKS</span></span>
