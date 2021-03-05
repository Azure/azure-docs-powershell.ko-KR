---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 5f63ee4d1c55211b13eb525a76547064e61cba48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001280"
---
# <span data-ttu-id="27416-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="27416-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="27416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27416-102">SYNOPSIS</span></span>
<span data-ttu-id="27416-103">네트워크 규칙 설정을 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27416-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="27416-104">구문</span><span class="sxs-lookup"><span data-stu-id="27416-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27416-105">설명</span><span class="sxs-lookup"><span data-stu-id="27416-105">DESCRIPTION</span></span>
<span data-ttu-id="27416-106">자격 증명 모음을 만들 때 사용할 수 있는 네트워크 규칙 설정을 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27416-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="27416-107">예제</span><span class="sxs-lookup"><span data-stu-id="27416-107">EXAMPLES</span></span>

### <span data-ttu-id="27416-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="27416-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="27416-109">새 자격 증명 모음을 만들고 네트워크 규칙을 지정하여 해당 자격 증명 모음으로 식별된 가상 네트워크에서 지정된 IP 주소에 $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="27416-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="27416-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27416-110">PARAMETERS</span></span>

### <span data-ttu-id="27416-111">-Bypass</span><span class="sxs-lookup"><span data-stu-id="27416-111">-Bypass</span></span>
<span data-ttu-id="27416-112">네트워크 규칙의 우회를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27416-112">Specifies bypass of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27416-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="27416-113">-DefaultAction</span></span>
<span data-ttu-id="27416-114">네트워크 규칙의 기본 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27416-114">Specifies default action of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27416-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27416-115">-DefaultProfile</span></span>
<span data-ttu-id="27416-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27416-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27416-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="27416-117">-IpAddressRange</span></span>
<span data-ttu-id="27416-118">허용되는 네트워크 IP 주소 범위의 네트워크 규칙을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27416-118">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27416-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="27416-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="27416-120">네트워크 규칙의 허용된 가상 네트워크 리소스 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27416-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27416-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27416-121">CommonParameters</span></span>
<span data-ttu-id="27416-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27416-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27416-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27416-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27416-124">입력</span><span class="sxs-lookup"><span data-stu-id="27416-124">INPUTS</span></span>

### <span data-ttu-id="27416-125">없음</span><span class="sxs-lookup"><span data-stu-id="27416-125">None</span></span>

## <span data-ttu-id="27416-126">출력</span><span class="sxs-lookup"><span data-stu-id="27416-126">OUTPUTS</span></span>

### <span data-ttu-id="27416-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="27416-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="27416-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27416-128">NOTES</span></span>

## <span data-ttu-id="27416-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27416-129">RELATED LINKS</span></span>
