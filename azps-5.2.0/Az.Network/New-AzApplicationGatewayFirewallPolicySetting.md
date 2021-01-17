---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340214"
---
# <span data-ttu-id="8ed1b-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="8ed1b-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="8ed1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ed1b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed1b-103">방화벽 정책에 대한 정책 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ed1b-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="8ed1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="8ed1b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ed1b-105">설명</span><span class="sxs-lookup"><span data-stu-id="8ed1b-105">DESCRIPTION</span></span>
<span data-ttu-id="8ed1b-106">**New-AzApplicationGatewayFirewallPolicySetting은** 방화벽 정책에 대한 정책 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ed1b-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="8ed1b-107">예제</span><span class="sxs-lookup"><span data-stu-id="8ed1b-107">EXAMPLES</span></span>

### <span data-ttu-id="8ed1b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ed1b-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="8ed1b-109">이 명령은 $enabledState 모드, $enabledMode RequestBodyCheck을 false로, FileUploadLimitInMb를 $fileUploadLimitInMb $ $fileUploadLimitInMb MaxRequestBodySizeInKb와 같은 상태로 정책 설정을 $maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="8ed1b-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="8ed1b-110">새 policySettings는 새 정책에 $condition.</span><span class="sxs-lookup"><span data-stu-id="8ed1b-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="8ed1b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ed1b-111">PARAMETERS</span></span>

### <span data-ttu-id="8ed1b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed1b-112">-DefaultProfile</span></span>
<span data-ttu-id="8ed1b-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ed1b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ed1b-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="8ed1b-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="8ed1b-115">방화벽 정책의 정책 설정에서 requestBodyCheck을 Diables합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed1b-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="8ed1b-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="8ed1b-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="8ed1b-117">최대 fileUpload 크기(MB)</span><span class="sxs-lookup"><span data-stu-id="8ed1b-117">Maximum fileUpload size in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ed1b-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="8ed1b-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="8ed1b-119">방화벽 정책의 정책 설정에 있는 MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="8ed1b-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 128
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ed1b-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="8ed1b-120">-Mode</span></span>
<span data-ttu-id="8ed1b-121">방화벽 정책의 정책 설정에 있는 방화벽 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="8ed1b-121">Firewall Mode in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: Detection
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ed1b-122">-State</span><span class="sxs-lookup"><span data-stu-id="8ed1b-122">-State</span></span>
<span data-ttu-id="8ed1b-123">방화벽 정책의 정책 설정에 있는 상태 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="8ed1b-123">State variable in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ed1b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed1b-124">CommonParameters</span></span>
<span data-ttu-id="8ed1b-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8ed1b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed1b-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8ed1b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed1b-127">입력</span><span class="sxs-lookup"><span data-stu-id="8ed1b-127">INPUTS</span></span>

### <span data-ttu-id="8ed1b-128">없음</span><span class="sxs-lookup"><span data-stu-id="8ed1b-128">None</span></span>

## <span data-ttu-id="8ed1b-129">출력</span><span class="sxs-lookup"><span data-stu-id="8ed1b-129">OUTPUTS</span></span>

### <span data-ttu-id="8ed1b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="8ed1b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="8ed1b-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8ed1b-131">NOTES</span></span>

## <span data-ttu-id="8ed1b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ed1b-132">RELATED LINKS</span></span>
