---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310274"
---
# <span data-ttu-id="9a08f-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="9a08f-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="9a08f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a08f-102">SYNOPSIS</span></span>
<span data-ttu-id="9a08f-103">방화벽 정책에 대 한 정책 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="9a08f-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="9a08f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a08f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a08f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9a08f-105">DESCRIPTION</span></span>
<span data-ttu-id="9a08f-106">**AzApplicationGatewayFirewallPolicySetting** 는 방화벽 정책에 대 한 정책 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a08f-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="9a08f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9a08f-107">EXAMPLES</span></span>

### <span data-ttu-id="9a08f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a08f-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="9a08f-109">명령이 상태가 $enabledState로 설정 되 고, mode가 $enabledMode FileUploadLimitInMb RequestBodyCheck false로, MaxRequestBodySizeInKb에서는 $ $maxRequestBodySizeInKb으로 $fileUploadLimitInMb와</span><span class="sxs-lookup"><span data-stu-id="9a08f-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="9a08f-110">새 policySettings $condition에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a08f-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="9a08f-111">변수</span><span class="sxs-lookup"><span data-stu-id="9a08f-111">PARAMETERS</span></span>

### <span data-ttu-id="9a08f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a08f-112">-DefaultProfile</span></span>
<span data-ttu-id="9a08f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a08f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a08f-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="9a08f-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="9a08f-115">방화벽 정책의 정책 설정에서 requestBodyCheck을 가능 하 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a08f-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="9a08f-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="9a08f-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="9a08f-117">최대 fileUpload 크기 (MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="9a08f-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="9a08f-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="9a08f-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="9a08f-119">방화벽 정책의 정책 설정 MaxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="9a08f-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="9a08f-120">-모드</span><span class="sxs-lookup"><span data-stu-id="9a08f-120">-Mode</span></span>
<span data-ttu-id="9a08f-121">방화벽 정책의 정책 설정에 있는 방화벽 모드</span><span class="sxs-lookup"><span data-stu-id="9a08f-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="9a08f-122">-상태</span><span class="sxs-lookup"><span data-stu-id="9a08f-122">-State</span></span>
<span data-ttu-id="9a08f-123">방화벽 정책의 정책 설정에 있는 상태 변수</span><span class="sxs-lookup"><span data-stu-id="9a08f-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="9a08f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a08f-124">CommonParameters</span></span>
<span data-ttu-id="9a08f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a08f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a08f-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a08f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a08f-127">입력</span><span class="sxs-lookup"><span data-stu-id="9a08f-127">INPUTS</span></span>

### <span data-ttu-id="9a08f-128">않아야</span><span class="sxs-lookup"><span data-stu-id="9a08f-128">None</span></span>

## <span data-ttu-id="9a08f-129">출력</span><span class="sxs-lookup"><span data-stu-id="9a08f-129">OUTPUTS</span></span>

### <span data-ttu-id="9a08f-130">PSApplicationGatewayFirewallPolicySettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9a08f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="9a08f-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9a08f-131">NOTES</span></span>

## <span data-ttu-id="9a08f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a08f-132">RELATED LINKS</span></span>
