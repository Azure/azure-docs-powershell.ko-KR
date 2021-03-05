---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 38f7d6780b598606d0a0938178309ed67e602315
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967920"
---
# <span data-ttu-id="c68b7-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c68b7-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="c68b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c68b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c68b7-103">네트워크 인터페이스의 효과적인 네트워크 보안 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c68b7-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="c68b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="c68b7-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c68b7-105">설명</span><span class="sxs-lookup"><span data-stu-id="c68b7-105">DESCRIPTION</span></span>
<span data-ttu-id="c68b7-106">**Get-AzEffectiveNetworkSecurityGroup** cmdlet은 네트워크 인터페이스에 적용되는 효과적인 네트워크 보안 그룹을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c68b7-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="c68b7-107">예제</span><span class="sxs-lookup"><span data-stu-id="c68b7-107">EXAMPLES</span></span>

### <span data-ttu-id="c68b7-108">예제 1: 네트워크 인터페이스에서 효과적인 네트워크 보안 그룹 사용</span><span class="sxs-lookup"><span data-stu-id="c68b7-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="c68b7-109">이 명령은 myResourceGroup이라는 리소스 그룹의 MyNetworkInterface라는 네트워크 인터페이스와 연결된 모든 효과적인 네트워크 보안 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c68b7-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="c68b7-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c68b7-110">PARAMETERS</span></span>

### <span data-ttu-id="c68b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68b7-111">-DefaultProfile</span></span>
<span data-ttu-id="c68b7-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c68b7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c68b7-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="c68b7-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="c68b7-114">네트워크 인터페이스의 이름을 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="c68b7-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="c68b7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c68b7-115">-ResourceGroupName</span></span>
<span data-ttu-id="c68b7-116">네트워크 인터페이스의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c68b7-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="c68b7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68b7-117">CommonParameters</span></span>
<span data-ttu-id="c68b7-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c68b7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68b7-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c68b7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68b7-120">입력</span><span class="sxs-lookup"><span data-stu-id="c68b7-120">INPUTS</span></span>

### <span data-ttu-id="c68b7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c68b7-121">System.String</span></span>

## <span data-ttu-id="c68b7-122">출력</span><span class="sxs-lookup"><span data-stu-id="c68b7-122">OUTPUTS</span></span>

### <span data-ttu-id="c68b7-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c68b7-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="c68b7-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c68b7-124">NOTES</span></span>

## <span data-ttu-id="c68b7-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c68b7-125">RELATED LINKS</span></span>

[<span data-ttu-id="c68b7-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="c68b7-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


