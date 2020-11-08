---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204045"
---
# <span data-ttu-id="7e499-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7e499-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="7e499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e499-102">SYNOPSIS</span></span>
<span data-ttu-id="7e499-103">네트워크 인터페이스의 유효한 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="7e499-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e499-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e499-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7e499-105">DESCRIPTION</span></span>
<span data-ttu-id="7e499-106">**AzEffectiveRouteTable** cmdlet은 네트워크 인터페이스에 적용 되는 유효한 경로 테이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="7e499-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7e499-107">EXAMPLES</span></span>

### <span data-ttu-id="7e499-108">예제 1: 네트워크 인터페이스에서 유효한 경로 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e499-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7e499-109">이 명령은 MyResourceGroup 이라는 리소스 그룹의 MyNetworkInterface 이라는 네트워크 인터페이스와 연결 된 유효 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="7e499-110">변수</span><span class="sxs-lookup"><span data-stu-id="7e499-110">PARAMETERS</span></span>

### <span data-ttu-id="7e499-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e499-111">-AsJob</span></span>
<span data-ttu-id="7e499-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7e499-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e499-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e499-113">-DefaultProfile</span></span>
<span data-ttu-id="7e499-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e499-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="7e499-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="7e499-116">네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="7e499-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e499-117">-ResourceGroupName</span></span>
<span data-ttu-id="7e499-118">네트워크 인터페이스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="7e499-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e499-119">CommonParameters</span></span>
<span data-ttu-id="7e499-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e499-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e499-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e499-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e499-122">입력</span><span class="sxs-lookup"><span data-stu-id="7e499-122">INPUTS</span></span>

### <span data-ttu-id="7e499-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e499-123">System.String</span></span>

## <span data-ttu-id="7e499-124">출력</span><span class="sxs-lookup"><span data-stu-id="7e499-124">OUTPUTS</span></span>

### <span data-ttu-id="7e499-125">PSEffectiveRoute에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7e499-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="7e499-126">상속자</span><span class="sxs-lookup"><span data-stu-id="7e499-126">NOTES</span></span>

## <span data-ttu-id="7e499-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e499-127">RELATED LINKS</span></span>

[<span data-ttu-id="7e499-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7e499-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


