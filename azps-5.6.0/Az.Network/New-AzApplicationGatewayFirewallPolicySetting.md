---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: 256509a42b844b196728b89b30abcdb6c5b9b386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962736"
---
# <span data-ttu-id="8fda2-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="8fda2-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="8fda2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fda2-102">SYNOPSIS</span></span>
<span data-ttu-id="8fda2-103">방화벽 정책에 대한 정책 설정 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8fda2-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="8fda2-104">구문</span><span class="sxs-lookup"><span data-stu-id="8fda2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fda2-105">설명</span><span class="sxs-lookup"><span data-stu-id="8fda2-105">DESCRIPTION</span></span>
<span data-ttu-id="8fda2-106">**New-AzApplicationGatewayFirewallPolicySetting은** 방화벽 정책에 대한 정책 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8fda2-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="8fda2-107">예제</span><span class="sxs-lookup"><span data-stu-id="8fda2-107">EXAMPLES</span></span>

### <span data-ttu-id="8fda2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8fda2-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="8fda2-109">명령은 상태와 정책 설정을 $enabledState 모드로, requestBodyCheck를 false로 $enabledMode FileUploadLimitInMb를 $fileUploadLimitInMb 및 MaxRequestBodySizeInKb를 $$maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="8fda2-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="8fda2-110">새 정책Settings는 새 정책에 $condition.</span><span class="sxs-lookup"><span data-stu-id="8fda2-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="8fda2-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8fda2-111">PARAMETERS</span></span>

### <span data-ttu-id="8fda2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fda2-112">-DefaultProfile</span></span>
<span data-ttu-id="8fda2-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fda2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fda2-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="8fda2-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="8fda2-115">방화벽 정책의 정책 설정에서 RequestBodyCheck을 Diables합니다.</span><span class="sxs-lookup"><span data-stu-id="8fda2-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="8fda2-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="8fda2-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="8fda2-117">최대 fileUpload 크기(MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="8fda2-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="8fda2-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="8fda2-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="8fda2-119">방화벽 정책의 정책 설정에서 MaxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="8fda2-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="8fda2-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="8fda2-120">-Mode</span></span>
<span data-ttu-id="8fda2-121">방화벽 정책의 정책 설정의 방화벽 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="8fda2-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="8fda2-122">-State</span><span class="sxs-lookup"><span data-stu-id="8fda2-122">-State</span></span>
<span data-ttu-id="8fda2-123">방화벽 정책의 정책 설정의 상태 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="8fda2-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="8fda2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fda2-124">CommonParameters</span></span>
<span data-ttu-id="8fda2-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8fda2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fda2-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fda2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fda2-127">입력</span><span class="sxs-lookup"><span data-stu-id="8fda2-127">INPUTS</span></span>

### <span data-ttu-id="8fda2-128">없음</span><span class="sxs-lookup"><span data-stu-id="8fda2-128">None</span></span>

## <span data-ttu-id="8fda2-129">출력</span><span class="sxs-lookup"><span data-stu-id="8fda2-129">OUTPUTS</span></span>

### <span data-ttu-id="8fda2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="8fda2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="8fda2-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8fda2-131">NOTES</span></span>

## <span data-ttu-id="8fda2-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fda2-132">RELATED LINKS</span></span>
