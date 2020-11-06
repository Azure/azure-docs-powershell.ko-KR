---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: d479c66b899637f2dc12061b7499fc65b7d59d66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531150"
---
# <span data-ttu-id="b3186-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b3186-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="b3186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3186-102">SYNOPSIS</span></span>
<span data-ttu-id="b3186-103">네트워크 인터페이스의 효과적인 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3186-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3186-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3186-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3186-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b3186-105">DESCRIPTION</span></span>
<span data-ttu-id="b3186-106">**AzureRmEffectiveNetworkSecurityGroup** cmdlet은 네트워크 인터페이스에 적용 되는 유효한 네트워크 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3186-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="b3186-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b3186-107">EXAMPLES</span></span>

### <span data-ttu-id="b3186-108">예제 1: 네트워크 인터페이스에서 효과적인 네트워크 보안 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="b3186-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="b3186-109">이 명령은 myResourceGroup 이라는 리소스 그룹의 MyNetworkInterface 이라는 네트워크 인터페이스에 연결 된 모든 유효 네트워크 보안 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3186-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="b3186-110">변수</span><span class="sxs-lookup"><span data-stu-id="b3186-110">PARAMETERS</span></span>

### <span data-ttu-id="b3186-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="b3186-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="b3186-112">네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3186-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="b3186-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3186-113">-ResourceGroupName</span></span>
<span data-ttu-id="b3186-114">네트워크 인터페이스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3186-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="b3186-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3186-115">-DefaultProfile</span></span>
<span data-ttu-id="b3186-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3186-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3186-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3186-117">CommonParameters</span></span>
<span data-ttu-id="b3186-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3186-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3186-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3186-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3186-120">입력</span><span class="sxs-lookup"><span data-stu-id="b3186-120">INPUTS</span></span>

## <span data-ttu-id="b3186-121">출력</span><span class="sxs-lookup"><span data-stu-id="b3186-121">OUTPUTS</span></span>

### <span data-ttu-id="b3186-122">PSEffectiveNetworkSecurityGroup에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b3186-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="b3186-123">상속자</span><span class="sxs-lookup"><span data-stu-id="b3186-123">NOTES</span></span>

## <span data-ttu-id="b3186-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3186-124">RELATED LINKS</span></span>

[<span data-ttu-id="b3186-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3186-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


