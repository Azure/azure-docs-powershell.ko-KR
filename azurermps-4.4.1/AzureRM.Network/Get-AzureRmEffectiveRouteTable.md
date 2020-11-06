---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: f42e378bb0bb5202f9f955dea1b844e343a0e037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531151"
---
# <span data-ttu-id="b1d03-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="b1d03-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="b1d03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1d03-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d03-103">네트워크 인터페이스의 유효한 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1d03-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1d03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1d03-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1d03-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1d03-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d03-106">**AzureRmEffectiveRouteTable** cmdlet은 네트워크 인터페이스에 적용 되는 유효한 경로 테이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d03-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="b1d03-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b1d03-107">EXAMPLES</span></span>

### <span data-ttu-id="b1d03-108">예제 1: 네트워크 인터페이스에서 유효한 경로 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1d03-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b1d03-109">이 명령은 MyResourceGroup 이라는 리소스 그룹의 MyNetworkInterface 이라는 네트워크 인터페이스와 연결 된 유효 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1d03-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="b1d03-110">변수</span><span class="sxs-lookup"><span data-stu-id="b1d03-110">PARAMETERS</span></span>

### <span data-ttu-id="b1d03-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="b1d03-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="b1d03-112">네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d03-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="b1d03-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d03-113">-ResourceGroupName</span></span>
<span data-ttu-id="b1d03-114">네트워크 인터페이스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d03-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="b1d03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d03-115">-DefaultProfile</span></span>
<span data-ttu-id="b1d03-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1d03-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1d03-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d03-117">CommonParameters</span></span>
<span data-ttu-id="b1d03-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d03-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d03-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d03-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d03-120">입력</span><span class="sxs-lookup"><span data-stu-id="b1d03-120">INPUTS</span></span>

## <span data-ttu-id="b1d03-121">출력</span><span class="sxs-lookup"><span data-stu-id="b1d03-121">OUTPUTS</span></span>

### <span data-ttu-id="b1d03-122">PSEffectiveRoute에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b1d03-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="b1d03-123">상속자</span><span class="sxs-lookup"><span data-stu-id="b1d03-123">NOTES</span></span>

## <span data-ttu-id="b1d03-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1d03-124">RELATED LINKS</span></span>

[<span data-ttu-id="b1d03-125">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1d03-125">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


