---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044869"
---
# <span data-ttu-id="e31e7-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e31e7-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="e31e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e31e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e31e7-103">네트워크 인터페이스의 효과적인 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e31e7-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="e31e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e31e7-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e31e7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e31e7-105">DESCRIPTION</span></span>
<span data-ttu-id="e31e7-106">**AzEffectiveNetworkSecurityGroup** cmdlet은 네트워크 인터페이스에 적용 되는 유효한 네트워크 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e31e7-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="e31e7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e31e7-107">EXAMPLES</span></span>

### <span data-ttu-id="e31e7-108">예제 1: 네트워크 인터페이스에서 효과적인 네트워크 보안 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="e31e7-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="e31e7-109">이 명령은 myResourceGroup 이라는 리소스 그룹의 MyNetworkInterface 이라는 네트워크 인터페이스에 연결 된 모든 유효 네트워크 보안 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e31e7-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="e31e7-110">변수</span><span class="sxs-lookup"><span data-stu-id="e31e7-110">PARAMETERS</span></span>

### <span data-ttu-id="e31e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e31e7-111">-DefaultProfile</span></span>
<span data-ttu-id="e31e7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e31e7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e31e7-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="e31e7-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="e31e7-114">네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e31e7-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="e31e7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e31e7-115">-ResourceGroupName</span></span>
<span data-ttu-id="e31e7-116">네트워크 인터페이스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e31e7-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="e31e7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e31e7-117">CommonParameters</span></span>
<span data-ttu-id="e31e7-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e31e7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e31e7-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e31e7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e31e7-120">입력</span><span class="sxs-lookup"><span data-stu-id="e31e7-120">INPUTS</span></span>

### <span data-ttu-id="e31e7-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e31e7-121">System.String</span></span>

## <span data-ttu-id="e31e7-122">출력</span><span class="sxs-lookup"><span data-stu-id="e31e7-122">OUTPUTS</span></span>

### <span data-ttu-id="e31e7-123">PSEffectiveNetworkSecurityGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e31e7-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="e31e7-124">상속자</span><span class="sxs-lookup"><span data-stu-id="e31e7-124">NOTES</span></span>

## <span data-ttu-id="e31e7-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e31e7-125">RELATED LINKS</span></span>

[<span data-ttu-id="e31e7-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e31e7-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


