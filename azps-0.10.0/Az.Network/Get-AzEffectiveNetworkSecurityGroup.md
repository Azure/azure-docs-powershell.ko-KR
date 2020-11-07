---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a960d5b2f6daf19fc4e46eb253b596eb88e6bd71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875604"
---
# <span data-ttu-id="5db20-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5db20-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5db20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5db20-102">SYNOPSIS</span></span>
<span data-ttu-id="5db20-103">네트워크 인터페이스의 효과적인 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5db20-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="5db20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5db20-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5db20-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5db20-105">DESCRIPTION</span></span>
<span data-ttu-id="5db20-106">**AzEffectiveNetworkSecurityGroup** cmdlet은 네트워크 인터페이스에 적용 되는 유효한 네트워크 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db20-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="5db20-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5db20-107">EXAMPLES</span></span>

### <span data-ttu-id="5db20-108">예제 1: 네트워크 인터페이스에서 효과적인 네트워크 보안 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="5db20-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="5db20-109">이 명령은 myResourceGroup 이라는 리소스 그룹의 MyNetworkInterface 이라는 네트워크 인터페이스에 연결 된 모든 유효 네트워크 보안 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5db20-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="5db20-110">변수</span><span class="sxs-lookup"><span data-stu-id="5db20-110">PARAMETERS</span></span>

### <span data-ttu-id="5db20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db20-111">-DefaultProfile</span></span>
<span data-ttu-id="5db20-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5db20-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db20-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5db20-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="5db20-114">네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db20-114">Specified the name of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5db20-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db20-115">-ResourceGroupName</span></span>
<span data-ttu-id="5db20-116">네트워크 인터페이스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db20-116">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5db20-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db20-117">CommonParameters</span></span>
<span data-ttu-id="5db20-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5db20-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db20-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5db20-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db20-120">입력</span><span class="sxs-lookup"><span data-stu-id="5db20-120">INPUTS</span></span>

## <span data-ttu-id="5db20-121">출력</span><span class="sxs-lookup"><span data-stu-id="5db20-121">OUTPUTS</span></span>

### <span data-ttu-id="5db20-122">PSEffectiveNetworkSecurityGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5db20-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5db20-123">상속자</span><span class="sxs-lookup"><span data-stu-id="5db20-123">NOTES</span></span>

## <span data-ttu-id="5db20-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5db20-124">RELATED LINKS</span></span>

[<span data-ttu-id="5db20-125">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5db20-125">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


